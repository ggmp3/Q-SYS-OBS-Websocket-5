# Q-SYS-OBS-Websocket-5

- OBS Websocket 5.x.x Q-Sys User Component (obs-websocket 5.x.x Protocol)
- OBS Protocol URL: https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md
- Written by Glen Gorton
- Built with OBS Version: 30.1.2
- Developed and tested using Q-SYS Designer v9.10.0

## NOTES:
- A Recording cannot be paused if the recording quality is set to "Same as stream" in OBS.
- Reply Buffer needs to be enabled in OBS (Settings->Output->Reply Buffer) and a recording needs to be active in order to use Reply Buffer controls.

### 17th October 2024 (v1.3)
- Tested with OBS Studio v30.2.3
- During ws.Error event, if err == "closed before established" the script would set the Status to a Fault and return end. Updated this to attempt a reconnect (Connect() function) after 30secs.

### 29th July 2024
- Tested with OBS Studio v30.2.2
- IP Address field was not changing to Red when IP address was empty. Updated Initialize() function.
- Added further check for a valid IP address during Connect() function.
- Added further details for status when err == "conn fail: errno 10014" is received -> this can also be a result of OBS being closed on the PC.
- Within the ws.Closed eventhandler, commented out where Controls['Connect'].Boolean is set to false/true.

### 13th June 2024 - Glen Gorton
- Added additional error code response (err == "Timed out waiting server reply") to ws.Error = function(ws, err).
