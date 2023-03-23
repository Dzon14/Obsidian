---
aliases: [SFD]
tags: [komsys]
---
# Start Frame Delimiter
The SFD (Start Frame Delimiter) is a specific field in the header of an Ethernet frame that follows the preamble and indicates the start of the frame. The SFD consists of a specific bit sequence that is used to synchronize the receiving end with the incoming data.

SFD stands for Start Frame Delimiter, which is a special sequence of bits that indicates the start of a frame in a data communication system. The SFD is part of the Ethernet frame header and is used to synchronize the receiver's clock with the sender's clock.

In Ethernet, the SFD follows the preamble, which is a sequence of alternating 0s and 1s that precedes the actual data in the frame. The SFD consists of a fixed pattern of 10101011 (binary) or AB (hexadecimal), which is immediately followed by the Ethernet frame header.

When a receiver detects the SFD, it knows that a new Ethernet frame is about to arrive and can synchronize its clock to the sender's clock. This helps ensure that the receiver can accurately decode the data being transmitted.

In summary, the SFD is a critical part of the Ethernet frame header that helps synchronize the sender and receiver's clocks and indicates the start of a new frame.

## Why both premble and SFD?
We need both the preamble and the SFD (Start Frame Delimiter) for synchronization and error detection purposes in data communication.

The preamble is a sequence of alternating 1's and 0's that is used to allow the receiver to synchronize its clock with that of the transmitter. The receiver can detect the start of the preamble and use it to adjust its clock so that it is synchronized with the transmitter. This ensures that the receiver is sampling the received signal at the correct times and can correctly interpret the data being transmitted.

The SFD is a unique bit sequence that immediately follows the preamble and indicates the start of the Ethernet frame. It is used to signal the start of the frame and to indicate the beginning of the frame delimiter. The SFD also serves as an error detection mechanism, as it allows the receiver to check if the transmitted frame is valid or not. If the SFD is not the expected value, then the receiver knows that there is an error in the frame.