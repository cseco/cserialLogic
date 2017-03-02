# cserialLogic
Cserial Logic is a multiplexing techniques that has been in development for 6 years now, although only exising in paper. We will in this work introduce the concepts of cserial logic, simulate an implementation of cserial logic in software and show how it can be implemented in hardware.


## 1. Concepts
Considering the equation for channel capacity
```dart
	C = B log2(1+S/N)
```
Where
```dart
	C is channel capacity
	B is channel Bandwidth
	S is received Signal power
	N is Noise power
```

The received power S can be considered to be coming from n different sources.
```dart
	S = Sum(Si,1,n)
	And For constant Si
	S = n * Si
```
Each signal has its own sub channel of bandwidth B having a capacity given by
```dart
	Ci = B log2(1+Si/N)
	Ci = B log2(1+S/(n N))
```
In this setup the overall channel capacity is then
```dart
	Cs = Sum(Ci, 1, n)
	Cs = B Sum(log2(1+S/(n N)))
```	
It is an important observation that ``` Cs > C ```. The challenge then is to find ways of having n sub channels sharing the same bandwidth and transmitting data simultaneously to a single receiver in such a way that the transmitted and received power is the sum of the power of the individual signals and the received noise power for a single signal is the same as for the combined signal.
## 2. Comparing with Existing Systems
The concept of cserial logic has some things in common with some existing systems like OFDM and QPSK/QAM. OFDM has a single channel divided into overlapping channels which are orthogonal so that they do not interfere with one another.
Some of the similarities are
```dart
 i. creation of subchannels
 ii. multiplexing of the signals in the subchannels.
 iii. No interference created in a sub channel from signals in other subchannels 
```
In order to achieve condition (iii) above, the signals in the different sub channels are not modulated at exactly the same time but there is a small time delay between the start of the modulation in successive sub channels. The time delay is selected in such a way as to enable continuous phase modulation. This introduces also some concepts used in MSK.
## 3. Cserial Logic in Theory

## References