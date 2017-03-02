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
	S = Sum(Si,n)
	And For constant Si
	S = n * Si
```
## References