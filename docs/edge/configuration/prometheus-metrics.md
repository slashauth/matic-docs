---
id: prometheus-metrics
title: Prometheus metrics
description: "How to enable Prometheus metrics for Polygon Edge."
keywords:
  - docs
  - polygon
  - edge
  - metrics
  - prometheus
---

## Overview

Polygon Edge can report and serve the Prometheus metrics, which in their turn can be consumed using Prometheus collector(s).

Prometheus metrics are disabled by default. It can be enabled by specifying the listener address using `--prometheus` flag or `Telemetry.prometheus` field in the config file. 
Metrics will be served under `/metrics` on the specified address.

## Available metrics

The following metrics are available:

| **Name**                                      | **Type**      | **Description**                                 |
|-----------------------------------------------|---------------|-------------------------------------------------|
| txpool_pending_transactions                   | Gauge         | Number of pending transactions in TxPool        |
| consensus_validators                          | Gauge         | Number of Validators                            |
| consensus_rounds                              | Gauge         | Number of Rounds                                |
| consensus_num_txs                             | Gauge         | Number of Transactions in the latest block      |
| consensus_block_interval                      | Gauge         | Time between this and last block in seconds     |
| network_peers                                 | Gauge         | Number of Connected peers                       |
| network_outbound_connections_count            | Gauge         | Number of outbound connections                  |
| network_inbound_connections_count             | Gauge         | Number of inbound connections                   |
| network_pending_outbound_connections_count    | Gauge         | Number of pending outbound connections          |
| network_pending_inbound_connections_count     | Gauge         | Number of pending inbound connections           |