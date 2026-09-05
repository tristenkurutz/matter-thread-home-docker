# Home Assistant / Matter / Thread stack
Docker Compose file for the three containers running Home Assistant, the Matter
controller, and the OpenThread Border Router on my server.

On my server, Thread runs on a Sonoff Dongle Lite MG21 USB radio, with
OTBR bridging onto the LAN so Home Assistant and the Matter controller can
reach Thread-based Matter devices without needing a Thread radio themselves.

## Usage

```bash
docker compose up -d
```

All three containers must run on `network_mode: host`. This is what lets Home
Assistant reach `matter-server`'s WebSocket API and OTBR's local REST API over
`localhost`.
