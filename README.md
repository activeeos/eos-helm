# eos-helm

Kubernetes Helm charts for the EOS smart contracts platform.

## Charts

### eos-block-producer

This Helm chart runs a single EOS block producer on Kubernetes. This
chart can be used for both testnet and production nodes. This chart is
not for running block producers in high availability modes.

Features:
* Custom config.ini and genesis state support
* Automatic HTTPS through Let's Encrypt
* Kubernetes ingress support
* Persistent volume support

See the `eos-block-producer/values.yaml` file for configuration
instructions.

### eos-block-producer-with-failover

This Helm chart runs a block producers with configurable failover. Use
this Helm chart to create highly redundant block producer setups. This
chart is powered by the tool
[nodeos-monitor](https://github.com/activeeos/nodeos-monitor). In
order to use this Helm chart, an Etcd cluster must me accessible to
the Kubernetes cluster. This chart exposes neither an HTTPS API nor an
ingress. It does expose a service, however, for maximum
flexibility. This Helm chart must be installed in an individual
release for each block producer in the failover group.

Features:
* Failover between block producer nodes
* Persistent volume support

See the `eos-block-producer-with-failover/values.yaml` file for
configuration instructions.
