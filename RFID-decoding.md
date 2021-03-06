# Math Model

1. Advanced Synchronisation and Decoding in RFID Reader Receivers

1. [RFID 2011] Maximum Likelihood Decoding for Non-Synchronized UHF RFID Tags

1. [TSP] Multipacket Reception of Passive UHF RFID Tags: A Communication Theoretic Approach

# Multiple Antenna for decoding

1. [ICMMT] An anti-collision algorithm based on smart antenna in RFID system

1. [ICASSP] Separation of overlapping RFID signals by antenna arrays

# Collision
## Encode

1. [RFID 2008] CDMA-based RFID systems in dense scenarios: Concepts and challenges
    
    >CDMA-based

1. [SIGCOMM 2012] Efficient and reliable low-power backscatter networks
    
    >BUZZ introduce a compressive sensing method. 

1. [INFOCOM 2014] A Parallel Identification Protocol for RFID Systems
    
    >Design a novel L-K code, which encodes the tag ID into a bit string with a specially designed pattern.

## PHY Recovery

1. [TCOM 2010] RFID Reader Receivers for Physical Layer Collision Recovery
    
    >Single Antenna Zero-Forcing (SAZF) Receiver. Single Antenna Ordered Successive Cancellation (SAOSUC) Receiver. Multiple Antenna Receivers(ZF and MMSE)

1. [ICT 2010] Single Antenna Physical Layer Collision Recovery Receivers for RFID Readers
    
    >Focus on the constellations in the Baseband of the Receiver and only limit the system with two collision. s(t) = aleak + h1a1(t) + h2a2(t) + n(t). Ultilize the channel estimation on the preamble where both tags are the same. Then a Zero-Forcing (ZF) receiver and a  Successive Interference Cancellation Receiver are implemented.

1. [MOBICOM 2010] Physical-layer Identification of UHF RFID Tags
    
    >The author notice the BLF, which resulted in Time Interval Error(TIE), and the average baseband power (the average power of an acquired RN16 preamble) are different for different tags. Also he investigated the use of additional timing features, such as the signal rise and fall times and the time from the reader’s transmission to the tag’s response. These timing features, however, performed poorly in both classification and identification.

1. [TOSP 2011] Multipacket reception of passive UHF RFID tags: A communication theoretic approach
    
    >A communication theoretic model for the design and analysis at the physical layer. The difference in delay, the channel fading, and the frequency of individual tags to separate the collided signals. The tags are synchronized to begin with, but differ later in the communication.

1. [TPDS 2012] DDC: A Novel Scheme to Directly Decode the Collisions in UHF RFID Systems

    >redesign the RN pattern to make the collided RNs decodable
    
1. [MOBICOM 2015] Come and Be Served: Parallel Decoding for COTS RFID Tags

    >Density based clustering algorithm. Different response delays and different bit durations. Different tags have different bit durations.(BLF)

1. [MOBICOM 2017] FlipTracer: Practical Parallel Decoding for Backscatter Communication

    >Although the collided signal is time-varying and irregular, transitions between signals’ combined states follow highly stable probabilities.




# FMCW in backscatter

1. MULTICHANNEL RADAR BACKSCATTER COMMUNICATION AND LOCALIZATION

    >Author provided the theoretical analysis for using FMCW waveforms for communication and localization of semi-passive RF nodes intended for long-term widearea deployment.

1. DESIGN AND IMPLEMENTATION OF AN FMCW RADAR SIGNAL PROCESSING MODULE FOR AUTOMOTIVE APPLICATIONS

    >FMCW Basic Knowledge.
