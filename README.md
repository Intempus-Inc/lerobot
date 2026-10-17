# LeRobot: Intempus fork

An experimental fork of [Hugging Face LeRobot](https://github.com/huggingface/lerobot), retained for its robot configuration changes and asynchronous inference client/server.

- Robot configuration: `lerobot/common/robot_devices/robots/configs.py`
- Inference experiment: `lerobot/scripts/server/`

The fork is based on upstream revision `0cf8648` and has not been brought up to date with current LeRobot. Its original four additional commits include removed upstream test fixtures, so the inherited test suite is not a complete validation of this fork. Hardware behavior has not been revalidated for this cleanup.

The inference experiment uses unencrypted gRPC and deserializes pickle payloads. Run it only between trusted peers on an isolated network; do not expose its server to the public internet.

Calibrate each robot installation separately. Machine-specific calibration files are excluded from the current source and ignored locally.

For current installation and supported hardware, use the [upstream project](https://github.com/huggingface/lerobot). The upstream [Apache 2.0 license](LICENSE) and source notices remain in place.

[Upstream citations](CITATIONS.bib) are retained for the library and included policy architectures.
