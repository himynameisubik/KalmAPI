# KalmAPI
### Kalm (minimum version 1.4.0) offers an API to get the current color of Kalm.

The color will change after the user switches his wallpaper or adjusting his settings, so you will need to call the method again. For that case you can use `didColorChange`. The boolean will be `FALSE` after a respring and your call of the method `getColor`. It will be `TRUE` after the user changes his wallpaper or adjusting the Kalm settings.

#### Tweak.h
```objectivec
@interface KalmAPI
+ (UIColor *)getColor;
+ (BOOL)didColorChange;
@end
```

#### Tweak.x(m)
```objectivec
- (void)yourInit {
	UIColor *kalmColor = [%c(KalmAPI) getColor];
	
	yourUILabel.textColor = kalmColor;
	yourUIView.backgroundColor = kalmColor;
}

- (void)yourUpdate {
	if ([%c(KalmAPI) didColorChange]) {
		UIColor *kalmColor = [%c(KalmAPI) getColor];
		
		yourUILabel.textColor = kalmColor;
		yourUIView.backgroundColor = kalmColor;
	}
}
```
