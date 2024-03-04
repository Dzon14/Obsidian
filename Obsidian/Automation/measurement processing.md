---
tags:
  - automation
---
# Measurement processing
- How do we get the data into the computer? 
- How can we improve the quality of the data? 
- How can we select the important data?

## Why measurement processing?
- Control
- [[supervision]] of the process
- Reports
- etc.
"Garbage in - garbage out"

## Measurement processing
- Sampling
	- analog signals, alias
- Data screening
	- test of data, outliers, alarms, reconciliation
- Digital filtering
	- the linear filter, low and high pass filters, non-linear filters

## [[Sampling]]
- Multiplexing, A/D-converter, sample & hold
	- normally zero-order-hold
- Synchronized by a reference clock
- Shannon's sampling theorem
	- based on infinite time and periodic data
	- normally sample 2-10 times faster
- Time scale of the process fundamental
- There is also non-equidistant sampling which is an event driven sampling (used to decrease number of samples and only when status is changing)
- Watch out for alias (vikning), when things are created from the sampling that is not according to the original signal.

### Examples from the board
![[Pasted image 20240221175208.png|400]]
![[Pasted image 20240221175233.png|400]]

#### Sampling of measurements
![[Pasted image 20240221154219.png|400]]

## Avoiding alias frequencies
- Sample faster?!
	- More expensive, always noise on signals and does not solve the problem
- Filter the signal prior to sampling
	- Analog
	- Low-pass
	- Also called "Anti-alias"

## Data screening
- Visualization
- There is nothing like "common sense"
	- Does it look right? Average value, outliers, missing data, min&max of sensor output etc.
- Trend checks
	- Does it go the right way?
- Extrapolation checks

#### Data quality
- Noise
- Missing values
- Outliers
- Trends

## Outlier detection (Rosner's test)
![[Pasted image 20240221155821.png|500]]
- If periodic (cyclic) data, Rosner does not work. Other methods are needed

## Note
- For the rest of the filters, including digital filtering, linear causal (and non-casual) filter etc, look at lecture slides.
- Many skipped slides