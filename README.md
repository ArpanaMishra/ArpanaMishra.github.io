FNU Arpana
sw2882
CS3590 Summer 2016
Selective Reject ARQ Simulation

This simulation project has been designed in Adobe Animate CC2015.2. There were not any known or detected bugs at the time of submission.

*************************************************************************************************************************************
The Simulation is divided into five scenarios as follows:

1.	 Perfect Communication: This demonstrates the communication of frames from sender to receiver and the acknowledgement in the form of RR from receiver to the sender when there are no issues.

2.	Damaged and Buffered Frame: In this part the frame 4 is lost or damaged before reaching the receiver. The frames 5 and 6 are successfully accepted by the receiver but they are stored in a buffer at its end. As soon as receiver receives frame 5 it notifies sender that frame 4 is missing by sending SREJ 4. The sender re-sends the frame 4 and the frame 5 & 6 are retrieved from buffer to be put in order after 4. 

3.	Damaged and Cumulative RR: This part of the simulation considers the case of missing/damaged RR. The acknowledgement sent from the Receiver upon accepting the frame/s gets lost. The receiver sends RR4 to the sender to confirm that it has received till Frame 3 and is now ready for Frame 4. The acknowledgment gets lost in the communication but the receiver sends the RR6 upon accepting frame 5 implying that it has successfully received all the frames till Frame 5. The receiver need not send RR's for any frame before frame 6.

4.	 Damaged RR and Timeout:  This part of the simulation also considers the case of missing/damaged RR but it does not receive a cumulative RR. The sender waits for a set time for acknowledgement from the receiver end. When it does not receive any acknowledgement till the set time then it sends RR P bit=1 to check the status of sent frames. In this simulation, the RR4 sent by the receiver gets lost. The sender waits for 5 seconds and then sends a RR P bit-1 request asking receiver to let it know which frame needs to be sent next. The receiver responds with RR6 as the cumulative RR. The sender sends frame 6 and the communication continues.

5.	Damaged Frame and Damaged REJ: This is an extension to Damaged and Buffered Frame scenario. The frame 4 is sent from sender but is lost. The receiver sends SREJ 4 notifying the same upon receiving frame 5 but this packet is also lost. The receiver buffers frame 5 and 6 and sender waits for acknowledgement of the sent frames. After waiting for 5 seconds it sends RR P bit=1 to the receiver. The Receiver responds by RR4. The sender sends the missing Frame 4 and in the meantime receiver sends RR7 as Frames 5 and 6 are already accepted. The sender gets to know that the receiver is now ready for frame 7. The sender then sends frame 7 to continue communication.

*************************************************************************************************************************************

Enjoy!

