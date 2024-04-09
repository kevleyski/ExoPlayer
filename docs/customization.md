---
permalink: /customization.html
redirect_to:
  - https://developer.android.com/media/media3/exoplayer/customization
---
This documentation may be out-of-date. Please refer to the
[documentation for the latest ExoPlayer release][] on developer.android.com.
{:.info}

identical or related behavior. For example, if you want to override every 'play'
operation, you need to override both `ForwardingPlayer.play` and
`ForwardingPlayer.setPlayWhenReady`, because a caller will expect the behavior
of these methdods to be identical when `playWhenReady = true`. Similarly, if you
  `playWhenReady = true`.
want to change the seek-forward increment you need to override both
`ForwardingPlayer.seekForward` to perform a seek with your customized increment,
and `ForwardingPlayer.getSeekForwardIncrement` in order to report the correct
customized increment back to the caller.
* If you want to control what `Player.Commands` are advertised by a player
  instance, you must override `Player.getAvailableCommands()`,
  `Player.isCommandAvailable()` and also listen to the
  `Player.Listener.onAvailableCommandsChanged()` callback to get notified of
changes coming from the underlying player.
[documentation for the latest ExoPlayer release]: https://developer.android.com/guide/topics/media/exoplayer/customization
