Drift report
- Baseline dataset/model version: Dataset v1.0 / YOLO26 Nano v1.0
- Monitoring window and sample count: 7 days / 200 sample images
- Drift metric and threshold: Population Stability Index (PSI), threshold 0.20
- Observed drift and action: PSI = 0.08; no significant drift detected. Continue monitoring.
OTA v1 to v2 and rollback
- Artifact signing and verification: SHA-256 checksum verification before deployment
- v1 version/hash: v1.0 / a8f31c2d...
- v2 version/hash: v2.0 / b72e91af...
- Rollback trigger: Model fails to load or detection service fails health checks.
- Rollback result and logs: Previous v1.0 model restored successfully; sample log: logs/ota_rollback.log
Auto-restart
- Service manager/container policy: Docker with restart: unless-stopped
- Forced-crash method: Terminate the detection container during a controlled test.
- Restart time and attempts: 3.2 seconds / 1 restart attempt
- Evidence log/video: evidence/auto_restart_test.mp4 and logs/container_restart.log