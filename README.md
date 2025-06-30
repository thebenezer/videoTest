# Video Background Demo

A simple demonstration showing how to create a fullscreen video background that properly autoplays on iOS Safari, even when the device is in Low Power Mode.

## Problem

By default, iOS Safari shows a play button overlay on videos when:

- The device is in Low Power Mode
- Autoplay is restricted by browser settings
- The video doesn't have the proper attributes for mobile playback

This can break the seamless video background experience on mobile devices.

## Solution

This demo shows the correct HTML video attributes needed to ensure smooth autoplay on iOS Safari:

```html
<video autoplay muted loop playsinline preload="auto">
	<source src="your-video.mp4" type="video/mp4" />
</video>
```

### Key Attributes:

- **`autoplay`** - Starts the video automatically
- **`muted`** - Required for autoplay to work on most mobile browsers
- **`loop`** - Continuously loops the video
- **`playsinline`** - **Critical for iOS** - Prevents fullscreen mode and allows inline playback
- **`preload="auto"`** - Preloads video data to improve autoplay reliability

## Testing on iOS

To test the Low Power Mode functionality:

1. Enable Low Power Mode on your iOS device (Settings > Battery > Low Power Mode)
2. Open the page in Safari
3. The video should autoplay without showing a play button overlay

Created as a tutorial for handling video autoplay on mobile devices.
