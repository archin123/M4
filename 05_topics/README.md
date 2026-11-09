# 05 — MQTT topics

Suggested topic namespace:
- `factory/carton_inspection/line1/detection`
- `factory/carton_inspection/line1/motor_score`
- `factory/carton_inspection/line1/status`

Use a versioned JSON payload with timestamp, device ID, model version and quality fields. The included demo prints messages locally; it does not publish to a broker.
