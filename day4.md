## QoS: Quality of Service

### Level 0: - at most once
This service level guarantees a best-effort delivery. There is no guarantee of delivery. The recipient does not acknowledge receipt of the message and the message is not stored and re-transmitted by the sender. QoS level 0 is often called “fire and forget” and provides the same guarantee as the underlying TCP protocol.

<li>continuous message

### Level 1: - at least once
QoS level 1 guarantees that a message is delivered at least one time to the receiver. The sender stores the message until it gets a  PUBACK packet from the receiver that acknowledges receipt of the message. It is possible for a message to be sent or delivered multiple times.
The sender uses the packet identifier in each packet to match the PUBLISH packet to the corresponding PUBACK packet. If the sender does not receive a PUBACK packet in a reasonable amount of time, the sender resends the PUBLISH packet. When a receiver gets a message with QoS 1, it can process it immediately. For example, if the receiver is a broker, the broker sends the message to all subscribing clients and then replies with a PUBACK packet.
If the publishing client sends the message again it sets a duplicate (DUP) flag. In QoS 1, this DUP flag is only used for internal purposes and is not processed by broker or client. The receiver of the message sends a PUBACK, regardless of the DUP flag. 

<li>order the message

### Level 2: - exactly once
This level guarantees that each message is received only once by the intended recipients. 
the safest and slowest quality of service level. The guarantee is provided by at least two request/response flows (a four-part handshake) between the sender and the receiver. The sender and receiver use the packet identifier of the original PUBLISH message to coordinate delivery of the message.
When a receiver gets a QoS 2 PUBLISH packet from a sender, it processes the publish message accordingly and replies to the sender with a PUBREC packet that acknowledges the PUBLISH packet. If the sender does not get a PUBREC packet from the receiver, it sends the PUBLISH packet again with a duplicate (DUP) flag until it receives an acknowledgement. 
Once the sender receives a PUBREC packet from the receiver, the sender can safely discard the initial PUBLISH packet. The sender stores the PUBREC packet from the receiver and responds with a  PUBREL packet.
After the receiver gets the PUBREL packet, it can discard all stored states and answer with a PUBCOMP packet (the same is true when the sender receives the PUBCOMP). Until the receiver completes processing and sends the PUBCOMP packet back to the sender, the receiver stores a reference to the packet identifier of the original PUBLISH packet. This step is important to avoid processing the message a second time. After the sender receives the PUBCOMP packet, the packet identifier of the published message becomes available for reuse.
When the QoS 2 flow is complete, both parties are sure that the message is delivered and the sender has confirmation of the delivery..
If a packet gets lost along the way, the sender is responsible to retransmit the message within a reasonable amount of time. This is equally true if the sender is an MQTT client or an MQTT broker. The recipient has the responsibility to respond to each command message accordingly.

<li>handle duplicate, ensure message reach destination


## [HTTP vs MQTT][1]

| |HTTP | MQTT|
|--|--|--|
|Model |request-response (protocol for client-server computing and not always optimized for mobile devices) |publish/subscribe (perfect for resource-constrained devices and help to save battery)|
|Package size |lengthy headers and messages (helps to eliminate troubles because it can be read by humans, but at the same time it’s needless for resource-constrained devices) |a very short message header and the smallest packet message size of 2 bytes |
|speed | |throughput of MQTT is 93 times faster than HTTP’s|
|cost| | |

[1]: https://medium.com/mqtt-buddy/mqtt-vs-http-which-one-is-the-best-for-iot-c868169b3105
|cost | | |
