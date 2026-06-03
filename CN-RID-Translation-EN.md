Here is the English translation of the provided Chinese national standard document **GB 46750—2025**:

---

**National Standard of the People's Republic of China** GB 46750—2025

# Specification for civil unmanned aircraft system operational identification

---

[Page 2 & 4 & 6, 29-31 are blank or page numbers only]

---

## Contents

Foreword
1 Scope
2 Normative References
3 Terms and Definitions
4 Abbreviations
5 Operational Identification Transmitting Segment
    5.1 Civil Unmanned Aircraft System
    5.2 Operational Identification Information and Protocol
6 Operational Identification Communication Link Segment
    6.1 Broadcast Mode Operational Identification Link
    6.2 Network Mode Operational Identification Link
7 Operational Identification Receiving Segment
    7.1 Broadcast Mode Operational Identification Receiving and Processing System
    7.2 Network Mode Operational Identification Receiving and Processing System
8 Compliance Assessment Methods
    8.1 Document Inspection
    8.2 Functional Verification
9 Implementation of the Standard
References

Figure 1 – Schematic diagram of broadcast mode operational identification
Figure 2 – Schematic diagram of network mode operational identification
Figure 3 – Data packet format

Table 1 – Data packet content
Table 2 – Data type and identifier
Table 3 – Data content items and coding value requirements

---

## Foreword

This document was drafted in accordance with the rules of GB/T 1.1—2020 "Directives for standardization – Part 1: Rules for the structure and drafting of standardizing documents".

Please note that certain contents of this document may involve patents. The issuing authority of this document is not responsible for identifying patents.

This document was proposed and is under the jurisdiction of the Civil Aviation Administration of China.

---

## Specification for civil unmanned aircraft system operational identification

### 1 Scope

This document specifies the information content, information format, transmission, communication link, reception and processing, and related system functional and performance requirements for civil unmanned aircraft system (UAS) operational identification, and describes the corresponding compliance assessment methods.

This document is applicable to the design, production, manufacturing, testing, inspection, approval, and operation of civil UAS, broadcast and network mode operational identification dedicated receiving and processing systems, as well as network equipment and communication links for civil UAS operational identification.

This document does not apply to large civil UAS that operate only within controlled airspace and meet airspace准入 communication, navigation, and surveillance capability requirements, nor to civil UAS operating only indoors.

### 2 Normative References

The following referenced documents are indispensable for the application of this document. For dated references, only the edition cited applies. For undated references, the latest edition (including any amendments) applies.

GB/T 41300 Civil unmanned aircraft – Unique product identification code

### 3 Terms and Definitions

For the purposes of this document, the following terms and definitions apply.

**3.1 unmanned aircraft**
Aircraft without an onboard pilot, powered by its own propulsion system.
[Source: GB42590—2023, 3.1.1]

**3.2 unmanned aircraft system**
A set of equipment centered on an unmanned aircraft, including associated remote control stations, required command and control links, and any other components specified in the design, capable of completing specific tasks.
[Source: GB/T38152—2019, 2.1.2]

**3.3 micro unmanned aircraft**
Unmanned aircraft with an empty weight less than 0.25 kg, maximum true flight altitude not exceeding 50 m, maximum level flight speed not exceeding 40 km/h, radio transmission equipment complying with micro-power short-distance technical requirements, and capable of manual intervention at any time during operation.
[Source: GB42590—2023, 3.1.2]

**3.4 light unmanned aircraft**
Unmanned aircraft with an empty weight not exceeding 4 kg, maximum takeoff weight not exceeding 7 kg, maximum level flight speed not exceeding 100 km/h, equipped with airspace retention capability and reliable surveillance capability meeting airspace management requirements, and capable of manual intervention at any time during operation.
Note: Excluding micro unmanned aircraft.
[Source: GB42590—2023, 3.1.3]

**3.5 small unmanned aircraft**
Unmanned aircraft with an empty weight not exceeding 15 kg and maximum takeoff weight not exceeding 25 kg, equipped with airspace retention capability and reliable surveillance capability meeting airspace management requirements, and capable of manual intervention at any time during operation.
Note: Excluding micro and light unmanned aircraft.
[Source: GB42590—2023, 3.1.4]

**3.6 medium unmanned aircraft**
Unmanned aircraft with a maximum takeoff weight not exceeding 150 kg.
Note: Excluding micro, light, and small unmanned aircraft.

**3.7 large unmanned aircraft**
Unmanned aircraft with a maximum takeoff weight exceeding 150 kg.

**3.8 civil unmanned aircraft system operational identification**
The process during civil UAS operation where operational identification information (including UAS identity, system attributes, and operational data) is actively transmitted via compliant communication links, received by a receiving system, and sent to a data processing system for processing.
Note 1: The entire process generally includes the transmitting segment, communication link segment, and receiving segment.
Note 2: Hereinafter referred to as "operational identification".

**3.9 broadcast mode operational identification**
An operational identification mode where a civil unmanned aircraft broadcasts operational identification information via specific radio frequencies and transmission protocols in a non-targeted manner, which is then received and processed by corresponding receiving and processing systems.
Note: See Figure 1 for schematic diagram.

**3.10 network mode operational identification**
An operational identification mode where a civil UAS actively sends operational identification information to a corresponding receiving system via a network, which is then processed by a corresponding data processing system.
Note: See Figure 2 for schematic diagram.

**3.11 transmitting function of operational identification broadcast mode**
The ability of a civil unmanned aircraft to automatically broadcast operational identification information via specific radio frequencies and transmission protocols in a non-targeted manner.

**3.12 transmitting function of operational identification network mode**
When a civil UAS has established a network connection with a network mode operational identification receiving system via a network mode operational identification communication link, the ability of the civil UAS to automatically send operational identification information to the network mode receiving system via the network using specific transmission protocols.

**3.13 operational identification transmitting module**
Hardware and software components that implement broadcast mode and network mode operational identification transmitting functions.

**3.14 transmitting dysfunction of operational identification**
A situation where a failure of the operational identification transmitting module causes the loss of broadcast mode or network mode transmitting functions.

### 4 Abbreviations

ADS-B: Automatic Dependent Surveillance-Broadcast
EIRP: Equivalent Isotropic Radiated Power
GNSS: Global Navigation Satellite System
GVA: Geometric Vertical Accuracy
NACp: Navigation Accuracy Category - position
NACv: Navigation Accuracy Category - velocity
RTK: Real Time Kinematic

### 5 Operational Identification Transmitting Segment

#### 5.1 Civil Unmanned Aircraft System

**5.1.1** A civil UAS shall possess both broadcast mode and network mode operational identification transmitting functions simultaneously.

**5.1.2** A civil UAS shall maintain automatic continuous transmission of operational identification information throughout its entire period of self-powered movement, and shall not have the function to disable transmission.

**5.1.3** The update and transmission interval for operational identification information shall not exceed 1 second.

**5.1.4** The operational identification functional module of a civil UAS shall comply with electromagnetic compatibility requirements.

**5.1.5** During operation, a civil UAS shall perform self-check of the operational identification transmitting module function and notify the UAS operator of the check result via audible or visual means.

**5.1.6** A civil UAS shall have a functional design to prevent tampering or destruction of operational identification, meeting the following requirements:
    a) Effective prevention of tampering or destruction of operational identification information;
    b) Effective prevention of tampering or destruction of the operational identification transmitting module.

**5.1.7** The operational identification transmitting module shall be interconnected with the flight control functional module of the civil UAS. When the transmitting module fails, the requirements are:
    a) If the transmitting module fails before takeoff, the civil UAS shall not be able to take off;
    b) If the broadcast mode transmitting function fails during operation, an alert shall be provided to the operator, and the UAS shall possess one or more handling capabilities such as hover/loiter, return-to-home, landing, or parachute deployment.

**5.1.8** During operational identification, a civil UAS shall rollingly store operational identification information with an update interval not exceeding 10 seconds. Storage capacity shall support information storage for no less than 120 flight hours, and shall not be manually deletable.

**5.1.9** A civil UAS shall cache network mode operational identification information that was not successfully sent and, after network mode recovery, provide a resend function for network mode operational identification.

**5.1.10** Civil unmanned aircraft shall not use ADS-B as a means of operational identification.

#### 5.2 Operational Identification Information and Protocol

**5.2.1** The operational identification information data packet shall contain data type, version number, data length, data identifier, and data content items, constituting the data packet as specified in Figure 3. The data packet content shall comply with Table 1.

**Figure 3 – Data packet format**

| Data Type | Version Number | Data Length | Data Identifier | Data Content Item 1 | Data Content Item 2 | ... | Data Content Item N |

**Table 1 – Data packet content**

| Data Packet Content | Length | Description | Value |
| :--- | :--- | :--- | :--- |
| Data Type | 1 byte | Data type definition | 255 |
| Version Number | 1 byte | Version number of the current operational identification data packet | Bits 1-3: fixed as "001"; Bits 4-8: valid values 0-63. Example: When bits 4-8 value is "X", version is "V1.X" |
| Data Length | 1 byte | Byte length of data content items | 1～200 |
| Data Identifier | 3+N byte | Indicates whether the data represented by this bit is sent. Bits 1-7 are content flags corresponding to Table 2. Bit 8 is extension flag. | Bits 1-7: 0 = not send; 1 = send. Bit 8: 0 = end of data identifier field; 1 = next byte is data identifier field |
| Data Content Item | Variable length | Shall be sent according to 5.2.4 | |

**5.2.2** Extended content of the operational identification information data packet shall use protocols uniformly issued by the competent civil aviation industry authority.

**5.2.3** The transmission of data identifiers shall comply with Table 2.

**Table 2 – Data type and identifier**

| Byte | Bit | Data Identifier | Item No. | Mandatory/Optional | Name |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Byte 1 | 0x80 | 001 | M | Unique product identification code |
| | 0x40 | 002 | M | Real-name registration mark |
| | 0x20 | 003 | O | Civil UAS operation category |
| | 0x10 | 004 | M | Civil UAS classification |
| | 0x08 | 005 | M | Civil UAS remote control station location type |
| | 0x04 | 006 | M | Civil UAS remote control station location |
| | 0x02 | 007 | M | Civil UAS remote control station height |
| | 0x01 | | | Extension flag |
| Byte 2 | 0x80 | 008 | M | Civil UAS location |
| | 0x40 | 009 | M | Track angle |
| | 0x20 | 010 | M | Ground speed |
| | 0x10 | 011 | O | Relative height |
| | 0x08 | 012 | O | Vertical speed |
| | 0x04 | 013 | M | Geodetic height |
| | 0x02 | 014 | O | Barometric pressure altitude |
| | 0x01 | | | Extension flag |
| Byte 3 | 0x80 | 015 | M | Operational status |
| | 0x40 | 016 | M | Coordinate system type |
| | 0x20 | 017 | M | Horizontal accuracy |
| | 0x10 | 018 | M | Vertical accuracy |
| | 0x08 | 019 | M | Speed accuracy |
| | 0x04 | 020 | M | Timestamp |
| | 0x02 | 021 | M | Timestamp accuracy |
| | 0x01 | | | Extension flag |
| Byte N | ... | ... | ... | ... |
| Note: "M" = Mandatory, "O" = Optional |

**5.2.4** The data content items and coding value requirements for operational identification information shall comply with Table 3.

**Table 3 – Data content items and coding value requirements**

| No. | Name | Description | Length (byte) | Value Requirements |
| :--- | :--- | :--- | :--- | :--- |
| 001 | Unique product identification code | Uniquely identifies the civil unmanned aircraft product identity | 20 | Big-endian representation, complies with GB/T 41300, encoded in ASCII. For UAS produced before 2024-01-01 without a unique product ID, send the UAS serial number, high bits padded with NULL |
| 002 | Real-name registration mark | Last 8 characters of the real-name registration number obtained after correctly filling the real-name registration system on the Civil UAS Integrated Management Platform | 8 | Big-endian representation, encoded in ASCII. Use NULL padding if not filled |
| 003 | Civil UAS operation category | Operation category, including certified, specific, open, and undefined | 1 | Value range: 0: undefined; 1: open; 2: specific; 3: certified; 4-15: reserved |
| 004 | Civil UAS classification | Classification including micro, light, small, medium, large | 1 | Value range: 0: micro; 1: light; 2: small; 3: medium; 4: large; 5-15: reserved |
| 005 | Civil UAS remote control station location type | Location type, including takeoff point or remote control station position | 1 | Value range: 0: takeoff point; 1: remote control station position; 2-15: reserved |
| 006 | Civil UAS remote control station location | Longitude and latitude of the remote control station | 8 | Little-endian representation. Encoded value = actual value × 10⁷, 32-bit longitude | 32-bit latitude. West longitude/south latitude as negative. Use "FFFFFFFF" when unknown/unavailable |
| 007 | Civil UAS remote control station height | Geodetic height of the remote control station based on current coordinate system | 2 | Little-endian representation. Encoded value = (actual value + 1000) × 2, resolution 0.5 m. Use "0" when unknown/unavailable |
| 008 | Civil UAS location | Longitude and latitude of the civil unmanned aircraft | 8 | Little-endian representation. Encoded value = actual value × 10⁷, 32-bit longitude | 32-bit latitude. West longitude/south latitude as negative. Use "FFFFFFFF" when unknown/unavailable |
| 009 | Track angle | Track angle measured clockwise from true north | 2 | Little-endian representation. Value = actual × 10, valid 0-3599, floor. Resolution 0.1°. Use "FFFF" when unknown/unavailable |
| 010 | Ground speed | Relative speed of the civil unmanned aircraft to the ground | 2 | Little-endian representation. Value = actual × 10, floor, resolution 0.1 m/s. Use "FFFF" when unknown/unavailable |
| 011 | Relative height | Height of the civil unmanned aircraft relative to takeoff point | 2 | Little-endian representation. Encoded value = (actual + 9000) × 2, resolution 0.5 m. Use "0" when unknown/unavailable |
| 012 | Vertical speed | Climb or descent rate based on current coordinate system | 1 | Bit 1 is sign (0: climb, 1: descent). Encoded value = (actual × 2), resolution 0.5 m/s. Use "FF" when unknown/unavailable |
| 013 | Geodetic height | Geodetic height of the civil unmanned aircraft based on current coordinate system | 2 | Little-endian representation. Encoded value = (actual + 1000) × 2, resolution 0.5 m. Use "0" when unknown/unavailable |
| 014 | Barometric pressure altitude | Standard pressure altitude referenced to 101.325 kPa | 2 | Little-endian representation. Encoded value = (actual + 1000) × 2, resolution 0.5 m. Use "0" when unknown/unavailable |
| 015 | Operational status | Operational status of the civil unmanned aircraft | 1 | Value range: 0: not reported; 1: ground; 2: airborne; 3: emergency state; 4: transmitting function failure (non-emergency); 5: transmitting function failure (emergency); 6-15: reserved |
| 016 | Coordinate system type | Coordinate system used for operational identification | 1 | Value range: 0: WGS-84; 1: CGCS2000; 2-15: reserved |
| 017 | Horizontal accuracy | Horizontal position accuracy (95% confidence) | 1 | 0: ≥18.52 km or unknown; 1: <18.52 km; 2: <7.41 km; 3: <3.70 km; 4: <1852 m; 5: <926 m; 6: <556 m; 7: <185 m; 8: <92.6 m; 9: <30 m; 10: <10 m; 11: <3 m; 12: <1 m; 13-15: reserved |
| 018 | Vertical accuracy | Vertical position accuracy (95% confidence) | 1 | 0: ≥150 m or unknown; 1: <150 m; 2: <45 m; 3: <25 m; 4: <10 m; 5: <3 m; 6: <1 m; 7-15: reserved |
| 019 | Speed accuracy | Speed accuracy (95% confidence) | 1 | 0: ≥10 m/s or unknown; 1: <10 m/s; 2: <3 m/s; 3: <1 m/s; 4: <0.3 m/s; 5-15: reserved |
| 020 | Timestamp | Unix time in milliseconds (ms) | 6 | Little-endian representation. Use "0" when unknown/unavailable |
| 021 | Timestamp accuracy | Accuracy range between encoded timestamp and real time | 1 | 0: >0.5 s or unknown; 1: ≤0.5 s; 2: ≤0.4 s; 3: ≤0.3 s; 4: ≤0.2 s; 5: ≤0.1 s; 6: ≤50 ms; 7: ≤20 ms; 8: ≤10 ms; 9-15: reserved |
| Note: Emergency status includes technical failures such as power system failure, navigation system anomaly, communication link interruption. a Based on GNSS NACp. b Based on GNSS GVA. c Based on GNSS NACv. |

### 6 Operational Identification Communication Link Segment

#### 6.1 Broadcast Mode Operational Identification Link

**6.1.1** The broadcast mode operational identification link communication technology shall meet the requirement for single complete transmission of the message content.

**6.1.2** Broadcast mode operational identification information shall be transmitted using at least one of Bluetooth 5.0 (or higher) broadcast mode or Wireless Broadband Access (Wi-Fi) broadcast mode.

**6.1.3** The power for Bluetooth broadcast mode shall meet at least requirement a) or b):
    a) EIRP output on the horizontal plane 360°:
        1) For micro: not less than 1 dBm;
        2) For light, small, medium, large: not less than 4 dBm.
    b) Average EIRP on the horizontal plane:
        1) For micro: not less than 3 dBm, and the difference between max EIRP and average power on 360° not more than 4 dB;
        2) For light, small, medium, large: not less than 6 dBm, and difference not more than 4 dB.

**6.1.4** The power for Wireless Broadband Access broadcast mode shall meet at least requirement a) or b):
    a) EIRP output on the horizontal plane 360°:
        1) At 2.4 GHz: micro ≥ 1 dBm; light/small/medium/large ≥ 11 dBm;
        2) At 5.8 GHz: micro ≥ 9 dBm; light/small/medium/large ≥ 18 dBm.
    b) Average EIRP on the horizontal plane:
        1) At 2.4 GHz: micro ≥ 9 dBm (max-min ≤ 4 dB); light/small/medium/large ≥ 13 dBm (max-min ≤ 4 dB);
        2) At 5.8 GHz: micro ≥ 16 dBm (max-min ≤ 4 dB); light/small/medium/large ≥ 20 dBm (max-min ≤ 4 dB).

#### 6.2 Network Mode Operational Identification Link

**6.2.1** The network mode operational identification link shall maintain stable communication capability between the civil UAS and the network mode operational identification receiving system.

**6.2.2** The network mode operational identification link shall use at least one of cellular network, terrestrial wired network, or satellite communication network.

**6.2.3** The network mode operational identification link shall be protected by cybersecurity measures such as security protocols to prevent unauthorized access.

**6.2.4** When a civil UAS uses a cellular network as the network mode operational identification link, the frequency, power, and RF technical indicator requirements shall be consistent with those for other terrestrial mobile communication system terminals using the cellular network.

### 7 Operational Identification Receiving Segment

#### 7.1 Broadcast Mode Operational Identification Receiving and Processing System

**7.1.1** A single broadcast mode operational identification receiving and processing system shall be capable of receiving, parsing, and processing information from Bluetooth and Wireless Broadband Access broadcast links used for broadcast mode operational identification and outputting operational identification information.

**7.1.2** A single broadcast mode operational identification receiving and processing system shall be capable of simultaneously receiving, distinguishing, and parsing operational identification information from at least 50 different targets.

**7.1.3** The time from receiving operational identification information to completing data processing shall not exceed 50 ms.

**7.1.4** The receiving dynamic range of the broadcast mode operational identification receiving and processing system shall not be less than 74 dB.

**7.1.5** Under no interference or overlap, when the input level signal is between -86 dBm and the upper limit of the receiving system dynamic range, the probability of correct reception and decoding shall not be less than 99.9%.

**7.1.6** Under no interference or overlap, when the input level signal is -89 dBm, the probability of correct reception and decoding shall not be less than 95%.

**7.1.7** Under no interference or overlap, when the input level signal is -91 dBm, the probability of correct reception and decoding shall not be less than 90%.

**7.1.8** It shall have comprehensive system operation monitoring and alarm functions.

**7.1.9** It shall store operational identification data for at least 90 days.

#### 7.2 Network Mode Operational Identification Receiving and Processing System

**7.2.1** It shall have the capability to receive network mode operational identification information sent via cellular networks, terrestrial wired networks, and satellite communication networks simultaneously.

**7.2.2** It shall publish data reception transmission protocols, IP addresses, and interface specifications.

**7.2.3** It shall meet the processing capacity for all targets within the service area. The time from receiving operational identification information to completing data processing shall not exceed 1 second.

**7.2.4** It shall have an operational identification data processing output interface and the ability to edit the output format.

**7.2.5** It shall have comprehensive system operation monitoring and alarm functions.

**7.2.6** It shall store operational identification data for at least 90 days.

### 8 Compliance Assessment Methods

#### 8.1 Document Inspection

##### 8.1.1 Civil Unmanned Aircraft System

**8.1.1.1** Clauses to verify: 5.1.4, 5.1.6, 5.1.8, 5.1.10.
**8.1.1.2** Inspection content: Technical manuals, radio transmission equipment type approval certificate, and other related documents.
**8.1.1.3** Pass criteria: a) Valid radio transmission equipment type approval certificate; b) Documentation indicates storage time and location for operational identification transmission information; c) Documentation indicates anti-tampering/anti-destruction design for transmitting function; d) Documentation indicates ADS-B is not used.

##### 8.1.2 Broadcast Mode Operational Identification Link

**8.1.2.1** Clauses to verify: 6.1.1, 6.1.2.
**8.1.2.2** Inspection content: Technical manuals of UAS and corresponding broadcast link service provider.
**8.1.2.3** Pass criteria: Documentation indicates use of at least Bluetooth 5.0+ broadcast mode or Wi-Fi broadcast mode, capable of single complete transmission.

##### 8.1.3 Network Mode Operational Identification Link

**8.1.3.1** Clauses to verify: 6.2.1, 6.2.2, 6.2.3, 6.2.4.
**8.1.3.2** Inspection content: Technical manuals of UAS and corresponding network link service provider.
**8.1.3.3** Pass criteria: a) Documentation indicates use of at least one compliant network link; b) Link and required hardware meet requirements.

##### 8.1.4 Operational Identification Receiving and Processing System

**8.1.4.1** Clauses to verify: 7.1.9, 7.2.2, 7.2.6.
**8.1.4.2** Inspection content: Technical manuals.
**8.1.4.3** Pass criteria: a) Documentation includes data protocols, IP addresses, interface specs; b) Data retention time meets requirements.

#### 8.2 Functional Verification

##### 8.2.1 Unmanned Aircraft System

**8.2.1.1 Transmitting Function** (5.1.1)
*Method:* Deploy broadcast receiver, set network target to verification system, trigger operational identification.
*Pass:* Broadcast receiver receives signal; network receiver receives data or network抓包 tool captures data.

**8.2.1.2 Full Process Operational Identification** (5.1.2)
*Method:* Trigger start and end conditions as per manufacturer.
*Pass:* Broadcast/network transmission starts when triggered, stops when trigger ends, consistent with operational identification operating range.

**8.2.1.3 Transmission Interval** (5.1.3)
*Pass:* Time difference between two consecutive operational identification messages ≤ 1s.

**8.2.1.4 Function Self-Check** (5.1.5)
*Pass:* No abnormal prompt when functioning normally; audible/visual/light prompt when transmitting function fails.

**8.2.1.5 Failure Handling** (5.1.7)
*Pass:* Cannot take off if transmitting function fails before takeoff; provides hover/loiter, RTH, landing, parachute capability during flight.

**8.2.1.6 Network Retransmission** (5.1.9)
*Pass:* Caches unsent messages; provides retransmission function after network recovery.

**8.2.1.7 Message Element and Protocol** (5.2.1, 5.2.2, 5.2.3)
*Pass:* Transmission interval ≤1s; messages correctly interpreted.

**8.2.1.8 Message Element Values** (5.2.4 except 017,018,019,021)
*Pass:* Messages correctly interpreted; values match reference or display; correct changes during failure/emergency.

**8.2.1.9 Message Element Accuracy Values** (5.2.4 items 017,018,019,021)
*Pass:* Calculated actual accuracy ≤ transmitted accuracy value for each test period.

##### 8.2.2 Operational Identification Communication Link

**8.2.2.1 Broadcast Link Transmit Power Verification** (6.1.3, 6.1.4)
*Pass:* EIRP meets requirements.

##### 8.2.3 Operational Identification Receiving and Processing System

**8.2.3.1 Broadcast Receive Function** (7.1.1)
*Pass:* Receives, parses, processes Bluetooth and Wi-Fi broadcast links.

**8.2.3.2 Broadcast Receive Capacity** (7.1.2)
*Pass:* Simultaneously processes ≥50 distinct targets.

**8.2.3.3 Broadcast Signal Processing Time** (7.1.3)
*Pass:* ≤ 50 ms.

**8.2.3.4 Broadcast Receiver Dynamic Range & Sensitivity** (7.1.4, 7.1.5, 7.1.6, 7.1.7)
*Pass:* Dynamic range >74 dB; correct decoding probability ≥99.9% (-86 dBm to上限), ≥95% (-89 dBm), ≥90% (-91 dBm).

**8.2.3.5 Broadcast Monitoring & Alarm** (7.1.8)
*Pass:* Alarm displayed on failure; alarm sent to verification platform.

**8.2.3.6 Network Receive Function** (7.2.1)
*Pass:* Capable of receiving via cellular, wired, satellite networks.

**8.2.3.7 Network Signal Processing Time** (7.2.3)
*Pass:* ≤ 1 s.

**8.2.3.8 Network Data Interface Editing** (7.2.4)
*Pass:* Has output interface and ability to edit output format.

**8.2.3.9 Network Monitoring & Alarm** (7.2.5)
*Pass:* Alarm displayed on failure; alarm sent to verification platform.

### 9 Implementation of the Standard

From the implementation date of this document, civil unmanned aircraft without operational identification transmission function shall not operate. For civil UAS already sold and in use, manufacturers must, within 12 months of the publication date of this document, retrofit the UAS with an operational identification module to meet the requirements of 5.1.1, 5.1.2, 5.1.3, 5.1.4, 5.1.6 a), 5.1.8, 5.1.9, 5.1.10, 5.2, 6.1, and 6.2. A 36-month transition period is granted for such retrofitted UAS to fully comply with all requirements of this document. After the transition period, all civil unmanned aircraft must fully comply with this document before operation.

### References

[1] GB/T 38152—2019 Unmanned aircraft system terminology
[2] GB 42590—2023 Safety requirements for civil unmanned aircraft system

---

This concludes the English translation of GB 46750—2025.
