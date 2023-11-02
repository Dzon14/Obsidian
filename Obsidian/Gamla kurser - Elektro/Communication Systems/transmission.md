---
tags: [komsys]
---
# Transmission
- Convert binary data to analog signals
		- Represent digital data in a continous world
- Binary modulation
- Analog transmission

## On-off keying (OOK)
- Send one bit during $T_{b}$ seconds and use two signals levels, "on" and "off", for 1 and 0. $$s(t) = A \cdot x, \ \ \ \ 0 \leq t \leq T_{b}$$
![[Pasted image 20230117163615.png|400]]
## Bipolar signalling
- Send one bit during $T_{b}$ seconds and use two signal amplitude levels, +A and -A, for 0 and 1 $$a(t) = A \cdot(-1)^{x}, \ \ \ \ 0 \leq t \leq T_{b}$$
![[Pasted image 20230117163636.png|400]]

## NRZ and RZ
Non-return to zero (NRZ):
- A pulse that spans the whole interval
![[Pasted image 20230117163834.png|150]]

Return to zero (RZ):
- A pulse where parts of the interval is zero
![[Pasted image 20230117163916.png|150]]


## [[manchester code]]

## M-PAM
![[Pasted image 20230117165158.png|400]]