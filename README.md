# Telemetry Analysis Notebook

A personal learning project focused on building a reproducible telemetry analysis workflow using Python and Jupyter notebooks.  

The goal of this project is to better understand vehicle dynamics, race engineering techniques, and data science by analyzing multiple channels of telemetry collected using a relatively low-cost, grassroots-oriented hardware stack.  

This repository is designed to evolve into a reusable toolkit for post-track-day analysis, lap comparisons, and driver/setup performance evaluation.
## Hardware and Software Stack (Telemetry Collection)

This project is something I am doing personally alongside my improvement as a grassroots driver, as such my pocket depth is limited. Because budget is an important consideration, commercial motorsport telemetry systems such as AiM, MoTeC, and similar professional-grade solutions are currently outside my price range.

- GPS / IMU - RaceBox Mini (~$220 USD)
- CAN / OBD-II - OBDLink MX+ (~$140 USD)
- Data Logging and Aggregation - RaceChrono Pro for IOS ($20 USD)

### Future Hardware Ideas  
  
In the future, this stack may be consolidated using a Raspberry Pi with a CAN interface to:  
  
- Read OBD-II/CAN data directly  
- Synchronize GPS and IMU data  
- Perform onboard logging  
- Reduce dependence on multiple commercial applications
## Data Sources

This project is primarily centered on RaceChrono CSV 3.0 based telemetry exports containing:

### Directly Recorded Channels

- GPS coordinates (lat, long, alt)
- Roll, pitch and yaw
- Vehicle Speed
- Longitudinal and lateral Acceleration
- Throttle percentage
- Brake percentage
- Steering angle
- Engine RPM (WIP)
- Gear position (WIP)
- Engine parameters (WIP)
- Individual wheel speeds (WIP)
- Tire pressure (WIP missing TPS sensors)

## Derived Channels and Metrics

In addition to recorded channels, the project aims to calculate engineering metrics that help to identify where time is lost or gained during a lap or session.

- Lap Times
- Sector times and Splits
- Distance along track
- Time delta to reference lap
- Front wheel angle
- Slip angle estimation
- Longitudinal and lateral g-force summaries
- Tire grip circle visualization (WIP)
- Croner entry, apex, and exit speeds

## Project Goals

- Reusable Python tools for telemetry processing
- Develop notebook-based race engineering workflows
- Compare laps and drive inputs
- Visualize track maps and racing lines
- Identify braking and throttle optimization opportunities 
- Improve driving and engineering performance
