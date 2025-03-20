Deregistration Flooding Attack
In the Deregistration Flooding attack, 70 UEs continuously sent deregistration requests to the AMF, leading to severe resource exhaustion. As a result, CPU usage spiked to nearly 100%, preventing legitimate signaling requests from being processed. Eventually, the AMF crashed, terminating all active sessions. The AMF logs (001g-benign-dereg_amf_log.png) reveal critical errors such as "Cannot receive SBI message" and assertion failures, ultimately forcing a shutdown and disconnecting all UEs.

Registration Flooding Attack
In the Registration Flooding attack, 2,000 registration messages and PDU session requests were replayed using 5Greplay, overwhelming the AMF. The AMF logs (009a_amf_log.png) recorded multiple "Registration Reject" errors and "Cannot receive SBI message" failures, indicating a breakdown in core network components. The attack persisted until assertion failures and a core dump led to a complete AMF crash. Similar SBI-related failures have been observed in other signaling overload attacks.

Fuzzing Attack
A Fuzzing attack using 5Greplay against the OAI core disrupted the registration process. The AMF logs (013_amf_log.png) captured a critical "NG_SETUP_FAILURE" caused by an "Unknown PLMN", resulting from malformed NAS messages. Repeated NG setup failures triggered assertion failures, ultimately leading to system termination. Packet analysis showed that only 215 out of 761 packets were successfully forwarded, confirming severe disruptions in the registration process.
