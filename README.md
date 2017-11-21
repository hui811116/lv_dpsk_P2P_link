# lv_dpsk_P2P_link

A DPSK uncoded point-to-point packet-based transceiver
Teng-Hui Huang. GICE, National Taiwan University

## Quick start
1. Packet based transmission
     1. Connect USRPs to PCs/laptops
     2. Run "usrp_tx.vi"
     3. Run "usrp_rx.vi"
     4. Press "Send Text" in transmitter program
2. Streaming transmission
    1. Connect USRPs to PCs/laptops
    2. Run "usrp_stream_tx.vi"
    3. Run "usrp_stream_rx.vi"

## Software/ Hardware specification
1. Two USRPs (NI-2920, NI-2932, NI-2901) 
2. Two commercial PCs/ Laptops
3. NI Modulation toolkits
4. NI USRP toolkits
5. LabView 2014

## System Details
The three major features of the prototype are: 
* Synchronization algorithms, 
* Burst transmission mode, 
* Functional physical layer.

First, this prototype is able to address standard synchronization problems such as carrier synchronization and time recovery sampling problems. We address the former problem with standard costas loop and the latter with polyphase time recovery loop. With the two modules, two USRPs can communicate without hardware such as MIMO cable, GPS antenna or external clocks. Furthermore, we have tested our prototype in USRP burst transmission mode. The two example programs in the source code support different modes of USRPs and users can develop applications from either program based on their requirements.
Secondly, the prototype has already functional physical layer system that takes bytes in and out from transmitter to receiver. One can easily use LabVIEW built-in flatten modules and convert message to bytes and use this prototype to send packets to the air. The reverse process is similar. Currently, our prototype supports two transmission rate based on either DBPSK or DQPSK is chosen as the modulation scheme.


## References
1. U. Mengali. Synchronization Techniques for Digital Receivers. Applications of
Communications Theory. Springer US, 1997.
2. Rice, Michael. Digital Communications: A Discrete-Time Approach. Upper Saddle River, NJ: Prentice Hall, 2009. 
