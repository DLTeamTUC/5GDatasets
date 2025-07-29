The .mat file contains resource allocation telemetry generated from a 5G System Level Simulation (SLS) using Round Robin (RR) scheduling. The simulation was executed with 4 User Equipments (UEs) over 10 Monte Carlo runs in a 5 MHz channel.

Contents:
1. dtable – Summary table of simulation results (throughput, RB allocation, CQI, MCS per UE).
2. Detailed logs – Per-symbol time-series data capturing:
- Resource Block (RB) assignments for each UE.
- Modulation and Coding Scheme (MCS) values.
- Per-RB Channel Quality Indicator (CQI).
3. RB-pair allocations during every scheduling decision.
4. Metadata – Variable names, dimensions, and units for all recorded parameters.

Purpose:
This data allows researchers to analyze radio resource allocation behavior of Round Robin scheduling in 5G networks, compare it against other schedulers (Proportional Fair, Best CQI), and evaluate UE-level fairness and throughput trends.
