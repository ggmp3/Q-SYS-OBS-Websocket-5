# Q-SYS-OBS-Websocket-5

- OBS Websocket 5.x.x Q-Sys User Component (obs-websocket 5.x.x Protocol)
- OBS Protocol URL: https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md
- Written by Glen Gorton
- Tested with OBS Version: 30.1.2
- Developed and tested using Q-SYS Designer v9.10.0

## NOTES:
- A Recording cannot be paused if the recording quality is set to "Same as stream" in OBS.
- Reply Buffer needs to be enabled in OBS (Settings->Output->Reply Buffer) and a recording needs to be active in order to use Reply Buffer controls.


### 13th June 2024 - Glen Gorton
- Added additional error code response (err == "Timed out waiting server reply") to ws.Error = function(ws, err).
