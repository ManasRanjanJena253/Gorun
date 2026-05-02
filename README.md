# Gorun

Gorun is a distributed ML training orchestrator built in Go and Python.
A Go-native scheduler handles job queuing, dynamic worker registration,
work-stealing dispatch, fault detection, and gRPC-based coordination —
while Python PyTorch workers register at runtime, receive training jobs,
stream metrics back over gRPC, and checkpoint on reassignment. Designed
for resilience: when a worker dies mid-training, Gorun detects it within
seconds and reassigns the job automatically. Benchmarked against sequential
and multiprocessing baselines on throughput, scheduling latency, and fault
recovery time.

> Status: Active development — June 2026