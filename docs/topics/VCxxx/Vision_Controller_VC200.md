Vision Controller VC200
=======================

Overview
--------

VC200 is a fixed logic controller used to synchronize PROINSPECT software environment to physical actuators used in automation project.

VC200 includes five different area of interest:

1. General I/O with PCL input and output
2. Four “Trigger – Strobe” camera sections
3. Dedicated power supply for special devices such as solenoids or valves
4. Four encoder quadrature input devices
5. Communication interface by a peer to peer Ethernet link.

VC200 is not a standalone product, but it must be used as a supervisor extension of RTVC100Service.  
RTVC100Service is installed on PC side and by ethernet port it is connected to VC200 external device

Usage
-----

VC200 is used to track each inspected part in a sequence of acquisitions and responsible of act some handling devices. Tracking is made possible by use of encoder or timing delay in order to fire trigger at right moment under camera places. Common area of interest is tracking inspected parts on linear belt or rounding table. Part is detected by an optical or electronic sensor: it triggers VC200 input line and displaces new events during the time or space distance requested. Camera pictures are usually triggered by hardware signal from Trigger-Strobe camera section. Each photo taken is now ready to be marked by id part code and it can be easily collected to be inspected. At the end of acquire and inspection phase VC200 acts as a standard PLC in order to notify by I/O or devices result of part inspection.

VC200 supports at maximum of four independent tracking processes ruled by the four encoders on board.

Multiple VC200 can be used at the same time. Each device has to be connected to a dedicate peer to peer ethernet port. VC100Service is able to serve a maximum number of four instances.

Configuration
-------------

Software to be installed:

1. RTVC100ServerService (one service per VC200 linked)
2. CPRTVC100UIS plugin extension, no registry configuration required
3. UvcIOPartIdSMemDevice - I/O device   
(multiple config. required in case of more than one VC200 device)
4. VC200 firmware 1.5 or compatible VC100 firmware Ed 3.4

(VC200 has to be setup according to number of services)
