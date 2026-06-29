# Practical 118-Node Distribution System Dataset

Processed topology, impedance, and load data for a practical 118-node distribution system modeled from two feeders in a city in Zhejiang Province, China.

## GitHub About

Processed practical 118-node distribution-system dataset from two feeders in Zhejiang, China, with confidential load and impedance data sanitized for public research use.

## Repository URL

https://github.com/your-account/practical-118-node-distribution-system

Replace `your-account` with the final GitHub owner name after the repository is created.

## Data Disclosure

The system topology is based on two practical distribution feeders from a city in Zhejiang Province, China. For security and confidentiality, the released load and line-impedance values are processed versions of the original field data rather than direct disclosure of operational measurements.

## Files

- `matlab/bus_118.mat`: original MATLAB MAT file containing the `bus` matrix.
- `matlab/branch_118.mat`: original MATLAB MAT file containing the `branch` matrix.
- `matlab/practical_118_node_system_data.m`: MATLAB function returning all processed data and metadata.
- `matlab/practical_118_node_system_data.py`: Python module returning the same data as NumPy arrays.

## Data Summary

- Nodes: 118
- Branches: 117
- Feeders selected from root bus 1 to buses 2, 49
- Total processed active load: 27.82 MW
- Total processed reactive load: 13.06 MVAr
- Line-resistance range: 0.1137-1.9968 ohm
- Line-reactance range: 0.0799-6.3531 ohm

## Matrix Format

The released matrices follow a MATPOWER-style layout.

### Bus Columns

`bus_i`, `type`, `Pd_kW`, `Qd_kVAr`, `Gs`, `Bs`, `area`, `Vm`, `Va_deg`, `baseKV`, `zone`, `Vmax`, `Vmin`

### Branch Columns

`fbus`, `tbus`, `r_ohm`, `x_ohm`, `b`, `rateA`, `rateB`, `rateC`, `ratio`, `angle_deg`, `status`, `angmin_deg`, `angmax_deg`

## MATLAB Usage

```matlab
data = practical_118_node_system_data();
bus = data.bus;
branch = data.branch;
topology = data.topology;
line_impedance = data.line_impedance_ohm;
load_data = data.load_kW_kVAr;
```

## Python Usage

```python
from matlab.practical_118_node_system_data import load_case

case = load_case()
bus = case.bus
branch = case.branch
topology = case.topology
line_impedance = case.line_impedance_ohm
load_data = case.load_kW_kVAr
```

## Citation Note

When using this dataset, please cite the associated paper and this repository. The repository link in the manuscript should be updated after the final GitHub URL is available.
