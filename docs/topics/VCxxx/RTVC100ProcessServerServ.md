RTVC100ProcessServerService
===========================

Overview
--------

RTVC100ProcessServerService is PC base service for VC100 or VC200 tracking device.

Multiple service instances can be used on single PC in order to arrange max four process per device.

RTVC100ProcessServerService installer is able to deploy all files needed also for multiple VC200 connected devices.

Usage
-----

Service is responsible to serve process queue of events. These events are described as Station.

This is a list of Station events to be served:

1. First Station is responsible to acquire digital signal from external device. Rising edge and falling edge signal record the state of timing and encoding position.
2. Acquire and Inspect Station is a sort of multiple digital output sync trigger to camera devices.  
In different places are served all firing triggers to take picture of parts.
3. Wakeup Station is time critical event invoke by a callback when process has to take handling decision.
4. Handling Stations are multiple point of interest. Wakeup moment will take a single decision from this list. Usually good or multiple point of rejection can handle part out of their process.
5. Check Stations are available to verify right placement of items during their route.

### Settings

Service must be manually configured editing RTVC100ProcessServer0 file.

This file is subdivided into sections. A part from a General one, each section describes a fully Process. 

| [GENERAL] | | | |
| --- | --- | --- | --- |
| VC100IP | 10.0.10.202 | 10.0.1<n>.202 | IP device |
| AlarmLines | 0 | 1,…n | Output alarm lines |
| AlarmValues | 0 | 0: OFF 1: ON | Output state due to alarm condition |
| Variable | Default | Range | Description |

| [PROCESS<XX>] | | | |
| --- | --- | --- | --- |
| FirstStationLine | 1 | <n> | Input Line - First Station |
| clockSel | 0 | 0: timer 1: encoder1 2: encoder2 |  |
| InputsNormalPolarity | 1 | 1: off2: on |  |
| InputWakeUpResultLine | 1 | <n> | Callback Line – Wakeup Station |
| OutputTriggerLines | 13,14,15,16 | <n><n> | Camera Port or general Output Line |
| NumOfTLCPerTriggerLines | 1,1,1,1 | <n><n> | Num of cameras per trigger signal |
| InputEndOfPartIdLine | 10 | <n> | Callback Line – End of tracking Station |
| OutputDataReadyLine | 2 | <n> | (optional) Output Line delayed First Station |
| OutputRejectLines | 9,10,11,12 | <n><n> | Handling reject Stations |
| OutputRejectLinesPriority | 3,2,1,4 | <n><n> | Handling priority (less is more) |
| OutputPassLines | 5 | <n> | Handling good Station |
| InputCheckLines | 2,3 | <n><n> | Check Stations |
| OutputCheckLines | 6,7 | <n><n> | Output Alarm Line for each Check Station |
| Variable | Default | Range | Description |

<XX\> = 1..4

| [OUTPUT<XX>] | | | |
| --- | --- | --- | --- |
| PositionOffset | 1063 | <n> tick | Relative delay position from First Station |
| PulseDuration | 5 | <n> msec | Relative pulse duration |
| Variable | Default | Range | Description |

Enter one section for each line used in Process section

| [CALLBACK<XX>] | | | |
| --- | --- | --- | --- |
| PositionOffset | 500 | <n> tick | Relative delay position from First Station |
| Variable | Default | Range | Description |

Enter one section for each line used in Process section
