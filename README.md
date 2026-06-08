# EE 470 Final Project: A* vs RRT* Path Planning

## Overview

MATLAB project comparing **A\*** and **RRT\*** path planning for autonomous vehicle navigation.

The script:

- Creates a driving scenario
- Converts the scenario into a binary occupancy map
- Runs A* and RRT*
- Checks for collision-free paths
- Computes planner performance metrics
- Plots path and metric comparisons

## Scenarios

The project supports three scenarios:

```matlab
scenarioID = 1; % Straight Road
scenarioID = 2; % Curved Road
scenarioID = 3; % Multi-Street Intersection
```

Change `scenarioID` near the top of `EE470_FinalProject.m` to select the scenario.

## Requirements

MATLAB with:

- Automated Driving Toolbox
- Navigation Toolbox

## Files

- `EE470_FinalProject.m`  
  Main script for scenario creation, occupancy map generation, A* planning, RRT* planning, metric calculation, and plotting.

## Setup

1. Download or clone the repository.
2. Open MATLAB.
3. Open `EE470_FinalProject.m`.
4. Confirm the required toolboxes are installed.
5. Select a scenario by changing `scenarioID`.

## Usage

Run the script in MATLAB:

```matlab
EE470_FinalProject
```

or open the file and click **Run**.

## Outputs

The script displays:

- Driving scenario plot
- Occupancy map
- A* path on the occupancy map
- RRT* path on the occupancy map
- A* and RRT* paths on the driving scenario
- Computation time comparison
- Path length comparison
- Path smoothness comparison
- Results table in the MATLAB command window

## Metrics

The planners are compared using:

- Success
- Collision-free result
- Computation time
- Path length
- Smoothness / total turning angle

## Notes

RRT* is sampling-based, so its path and metrics may change slightly between runs.

A* is grid-based and typically gives more repeatable results for the same occupancy map.
