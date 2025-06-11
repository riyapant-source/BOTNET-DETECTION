#README
This is a Python implementation of Network Traffic Flow Generator and Feature Extractor. The main functionality of this code is : <br>
1. To identify the flows in the network traffic <br>
2. To extract features to characterize the Flows
<br>
<a> Please Have a look at <a href = "https://github.com/hmishra2250/BTP/blob/master/Custom%20Flow%20Generator/FlowBasedFeatures.txt">Flow Feature file </a> in this directory for understanding the Flows and the Features in network traffic</a>
## PREREQUISITES
1. <a href="https://github.com/turi-code/SFrame">SFrame</a> should be installed.
2. CSV Input file having the packets captured and the columns mentioned should be available using Wireshark.<br>
## INPUT
A CSV File of Network Traffic capture. It can be easily done using Wireshark, an Open Source tool. The following columns must be there in the CSV: <br>
     'Source',<br>
     'Source Port',<br>
     'Answer RRs',<br>
     'Destination',<br>
     'Destination Port',<br>
     'Protocol',<br>
     'Protocols in frame',<br>
     'Time',<br>
     'IP_Flags',<br>
     'Length',<br>
     'Next sequence number',<br>
     'No.',<br>
     'Sequence number',<br>
     'TCP Segment Len',<br>
     'tcp_Flags',<br>
     'udp_Length'
     
 ## ARGUMENTS
 It takes command line argument - the path of the CSV Input file described above.
 ## OUTPUT
 <p>A CSV File having all the flows and Flow based Features. </p>
 <p>This file can be further used to analyze properties and characteristics of the Network Traffic Captured</p>
 <p>List of Features Generated per flow: 
Source IP<br>
Destination IP<br>
Source port<br>
Destination port<br>
Protocol<br>
NumPackets(Total number of packets ex-changed)<br>
NPEx(Number of null packets ex-changed)<br>
IOPR (ratio between the number of incoming packets over the number of outgoing packets)<br>
Reconnect (number of reconnects)<br>
Duration (flow duration)<br>
FPL (length of the first packet)<br>
Total number of bytes<br>
APL(Average payload packet length)<br>
SameLenPktRatio(Total number of packets with the same length over the total num-ber of packets)<br>
Standard deviation of payload packet length<br>
Average bits-per-second<br>
IAT(Average inter arrival time of packets)<br>
Average packets-per-second<br>
 </p>
 ## FUTURE WORK
 The Future work will be to make this Custom Flow Generator implementation as a user-friendly tool.<br>
 1. Automatically extract the CSV File from the pcap File of the captured traffic with the required columns.<br>
 2. Give Option For choosing the features to be generated. <br>
 3. Merge the implentation for Unidirectional Flows and give an option to choose For Unidirectional or Bidirectional FLows.<br>
 
 
 
 
