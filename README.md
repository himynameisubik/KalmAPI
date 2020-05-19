# KalmAPI
### Kalm (minimum version 1.4.0) offers an API to get the current color of Kalm.

#### Tweak.h
```objectivec
@interface KalmAPI
+ (UIColor *)getColor;
@end
```

#### Tweak.x(m)
```objectivec
- (void)yourMethod {
	UIColor *kalmColor = [%c(KalmAPI) getColor];
	
	yourUILabel.textColor = kalmColor;
	yourUIView.backgroundColor = kalmColor;
}
```
