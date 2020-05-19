# KalmAPI
### Kalm (minimum version 1.4.0) offers an API to get the current color of Kalm.

The color of Kalm will change after the user switches his wallpaper or adjusting his settings, so you will need to call the method again and compare your previous color to the new color of Kalm and update your elements accordingly.

#### Tweak.h
```objectivec
@interface KalmAPI
+ (UIColor *)getColor;
@end
```

#### Tweak.x(m)
```objectivec
- (void)yourInit {
	UIColor *kalmColor = [%c(KalmAPI) getColor];
	
	yourUILabel.textColor = kalmColor;
	yourUIView.backgroundColor = kalmColor;
}
```
