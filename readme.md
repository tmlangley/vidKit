# VidKit

VidKit has two primary goals. 

- Allow developers to easily place videos as a background of another element.
- Provide a standard way to customize videos from various video services.

## Usage

```javascript
$(".vidWrapper").vidKit({
  videoUrl: 'https://www.youtube.com/watch?v=123456789',
  aspectRatio: 1.33333, // 16:9
  autoplay: 1,
  loop: 1,
  controls: 0,
  backgroundSize: 'cover', // Same as css background-size: cover;
  verticalAlign: 'middle' 
});
```

### Events

```javascript
$(".vidWrapper").on('vidKit.ready', function() {
  // Do something...
});
```

- `vidkit.ready` - Video is ready.
- `vidkit.playing` - Video has started playing.


### Methods

```javascript
$(".vidWrapper").on('vidKit.ready', function() {
  $(this).vidKit('seekTo', 22); // Go to 22 seconds on the timeline.
});
```

- `play` - Start the video playback.
- `pause` - Pause the video playback.
- `stop` - Stop the video.
- `seekTo` - Go to a specific place in the video. Useful for restarting the video.
