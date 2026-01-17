# What is QUIC Protocol?

- QUIC stands for Quick UDP Internet Connections.
- This protocol runs on UDP but implements TCP + TLS features itself.
- It is designed by Google.
- QUIC used UDP because UDP is:

  - Connectionless
  - No reliability
  - No congestion control
  - No ordering
 
> Quic uses UDP only as a transport shell. All intelligence lives inside QUIC.
