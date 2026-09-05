# Home Assistant / Matter / Thread stack
Docker Compose file for the three containers running Home Assistant, the Matter
controller, and the OpenThread Border Router on this server.

## Usage

```bash
docker compose up -d
```

All three containers must run on `network_mode: host`. This is what lets Home
Assistant reach `matter-server`'s WebSocket API and OTBR's local REST API over
`localhost`.
