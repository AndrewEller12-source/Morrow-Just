# Shared interfaces

Proposed contracts to agree before implementation. Add machine-readable schemas and validation after choosing the existing software baseline.

| Contract | Minimum information | Failure or boundary |
| --- | --- | --- |
| HUD card | Stable ID, revision, text, position, size, visibility | Latest revision wins; clamp placement and size to viewport |
| Display | Card revision, submitted timestamp, rendering/transport result | Distinguish host render from device confirmation; no invented presented acknowledgment |
| Orientation | Device ID, timestamp, quaternion, recenter event | Connected/calibrating/streaming/stale/disconnected; orientation only |
| Input | Engage, release, cancel, recenter | Disconnect/tracking loss cancels active manipulation; fresh engagement required |
| Assistant task | Request ID, status, result/error | Submitted/running/completed/failed/cancelled; bounded retries and deduplication |

Before coding, agree timestamp units, coordinate origin/units, size limits, text limits, recenter behavior, and supported transport. Tap and held engagement are different actions; final gesture mapping is unresolved. Keep camera coordinates separate from orientation.
