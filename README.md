# Replication Package: Operationalization of equity through quantitative analysis of stakeholder salience

This repository contains the replication datasets for the paper **"Operationalization of equity through quantitative analysis of stakeholder salience"** by Isabel M. del Águila and José del Sagrado (Department of Informatics, University of Almería).

## Overview

## Overview

The dataset provides the experimental data used to evaluate the proposed operationalization method for identifying stakeholder salience based on three core attributes: **Urgency (`urg`)**, **Legitimacy (`leg`)**, and **Power (`pow`)**. 

The source metrics are derived from the original RALIC project dataset, which is publicly available at [Sooling Lim's Dataset Repository](https://soolinglim.com/Datasets.html). To evaluate effectiveness in maintaining equality and diversity, the arrangement model is systematically evaluated by mapping these stakeholder attributes into **two and three intervals** per dimension, producing distinct stakeholder **subgroups**.


## Repository Structure

The repository includes the four primary `.csv` files corresponding exactly to the partition methods and dimension intervals evaluated in the case study:

1. `stks_grouped_mid_points.csv`  
   * **Subgroups:** 2 intervals (low, high) per dimension.
   * **Partition Criteria:** Divides the range of each dimension into two halves of equal amplitude (Same range width).

2. `stks_grouped_q2s.csv`  
   * **Subgroups:** 2 intervals (low, high) per dimension.
   * **Partition Criteria:** Divides the range of each dimension into two subintervals using the median (Same stakeholders number), balancing the distribution.

3. `stks_grouped_three_subintervals.csv`  
   * **Subgroups:** 3 intervals (low, moderate, high) per dimension.
   * **Partition Criteria:** Divides the range of each dimension into three subintervals of equal amplitude (Same range width).

4. `stks_grouped_terciles.csv`  
   * **Subgroups:** 3 intervals (low, moderate, high) per dimension.
   * **Partition Criteria:** Divides the range of each dimension into three subintervals using terciles (Same stakeholders number), optimizing balance and diversity.

## Data Format & Schema

Each CSV file uses a semicolon (`;`) as a separator and follows this structure:

| Column | Type | Description |
| :--- | :--- | :--- |
| `class` | String | The assigned stakeholder salience subgroup combination (e.g., `"low.low.low"`, `"low.mod.high"`) based on interval mappings. |
| `key` | Integer | Unique tracking row identifier. |
| `id` | Integer | Anonymous stakeholder identification number from the recommendation network (RALIC project). |
| `urg` | Numeric | Quantitative metric representing the **Urgency** attribute (number of requirements voted). |
| `leg` | Numeric | Quantitative metric representing the **Legitimacy** attribute (total recommendations received). |
| `pow` | Numeric | Quantitative metric representing the **Power** attribute (status or role significance). |

### Data Example
```csv
"class";"key";"id";"urg";"leg";"pow"
"low.low.low";4;4;0;1;0.0
"high.high.high";31;31;25;142;88.5
```

### Citation
If you use this replication package or find the methodology useful in your research, please cite our paper:

```
@article{delaguila2026operationalization,
  title={Operationalization of equity through quantitative analysis of stakeholder salience},
  author={del {\'A}guila, Isabel M. and del Sagrado, Jos{\'e}},
  journal={Software},
  year={2026}
}
```

License: 
  - This dataset is made available for academic and replication purposes.
