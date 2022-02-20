# This is the list of different Flutter widgets that I know about.

## Animated CrossFade
A widget that cross-fades between two given children and animates itself between their sizes.

### Code Snippet
``` dart
AnimatedCrossFade(
  duration: const Duration(seconds: 3),
  firstChild: const FlutterLogo(style: FlutterLogoStyle.horizontal, size: 100.0),
  secondChild: const FlutterLogo(style: FlutterLogoStyle.stacked, size: 100.0),
  crossFadeState: _first ? CrossFadeState.showFirst : CrossFadeState.showSecond,
)
```