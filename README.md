# Replication Package: Operationalization of equity through quantitative analysis of stakeholder salience

This repository contains the replication datasets for the paper **"Operationalization of equity through quantitative analysis of stakeholder salience"** by Isabel M. del Águila and José del Sagrado (Department of Informatics, University of Almería).

## Overview


The dataset provides the experimental data used to evaluate the proposed operationalization method for identifying stakeholder salience based on three core attributes: **Urgency (`urg`)**, **Legitimacy (`leg`)**, and **Power (`pow`)**. 

To analyze the performance and fairness metrics, data partitions were generated using two different partition styles across two and three cuts (thresholds) per dimension.

## Repository Structure

The repository includes four primary `.csv` files representing the combinations of partition types and cut numbers evaluated in the study:

1. `data_partition_2cuts_methodA.csv` - Dataset using 2 cuts (low/high) per dimension.
2. `data_partition_3cuts_methodA.csv` - Dataset using 3 cuts (low/mid/high) per dimension.
3. `data_partition_2cuts_methodB.csv` - Alternative partition strategy with 2 cuts.
4. `data_partition_3cuts_methodB.csv` - Alternative partition strategy with 3 cuts.

*(Note: Please rename the placeholders above to match your exact file naming convention, e.g., using `mid_points` or specific algorithm names).*

## Data Format & Schema

Each CSV file uses a semicolon (`;`) as a separator and follows this structure:

| Column | Type | Description |
| :--- | :--- | :--- |
| `class` | String | The assigned stakeholder salience class combination (e.g., `"low.low.low"`, `"low.low.high"`) based on the partition thresholds. |
| `key` | Integer | Unique row tracking identifier. |
| `id` | Integer | Anonymous stakeholder identification number. |
| `urg` | Numeric | Normalized score/metric for the **Urgency** attribute. |
| `leg` | Numeric | Normalized score/metric for the **Legitimacy** attribute. |
| `pow` | Numeric | Normalized score/metric for the **Power** attribute. |

### Data Example
```csv
"class";"key";"id";"urg";"leg";"pow"
"low.low.low";1;1;8;31;24.75
"low.low.high";52;52;19;110;49.325
