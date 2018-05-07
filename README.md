# eos-helm

Helm charts for the EOS smart contracts platform.

## Charts

### eos-block-producer

The `eos-block-producer` Helm chart runs EOS block producers on
Kubernetes. This chart can be used for both testnet and production
nodes. See the `values.yaml` file for configuration instructions.

Features:
* HTTPS with Let's Encrypt
* Ingress support

TODO:
* Support custom genesis state
