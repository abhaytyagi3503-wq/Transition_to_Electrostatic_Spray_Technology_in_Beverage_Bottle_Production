
# Transition to Electrostatic Spray Technology in Beverage Bottle Production

## Project Overview

This project focuses on analyzing the transition from a conventional **air-spray beverage bottle coating process** to an automated **electrostatic spray coating system**. The main objective was to improve production throughput, reduce paint consumption, improve coating quality, reduce downtime, and evaluate the financial feasibility of implementing the new system at production scale.

The project was completed as a transition-to-production and smart manufacturing study. It does not focus on physically building the equipment. Instead, it uses a systems engineering approach to evaluate how the proposed electrostatic spray technology can be introduced into a real beverage bottle production line.

The study includes customer requirements, system requirements, baseline process analysis, proposed system architecture, discrete-event simulation planning, predictive maintenance analysis, cost-benefit evaluation, risk analysis, and implementation planning.

---

## Objectives

- Analyze the current air-spray beverage bottle coating process.
- Identify operational issues such as paint waste, defects, refill interruptions, and downtime.
- Propose an automated electrostatic spray coating system.
- Translate customer needs into measurable system requirements.
- Compare baseline and proposed production performance.
- Use JaamSim-based discrete-event simulation planning for process evaluation.
- Estimate predictive maintenance benefits.
- Perform cost-benefit and ROI analysis.
- Develop a phased implementation plan for production deployment.

---

## Tools and Techniques Used

- Systems Engineering
- Transition-to-Production Analysis
- Electrostatic Spray Technology
- Discrete-Event Simulation Planning
- JaamSim
- Predictive Maintenance Analysis
- Cost-Benefit Analysis
- ROI and Payback Calculation
- OEE Analysis
- MTBF and MTTR Reliability Metrics
- Risk Analysis
- Asset Management Planning
- Process Flow Mapping

---

## Current Production System

The existing beverage bottle coating line uses conventional air-spray guns mounted near a conveyor-based bottle/can production line. The current production flow includes in-house production, furnace operation, paint booths, quality inspection, and packaging.

### Baseline Process Flow

```text
Bottle Generator
        ↓
Spray Queue
        ↓
Spray Booth
        ↓
Curing Oven
        ↓
Inspection
        ↓
Packaging
````

The baseline process has several operational limitations:

* High paint consumption
* Overspray waste
* Manual refill interruptions
* Daily cleaning downtime
* Periodic deep cleaning
* Coating quality variation
* Higher defect rate
* Maintenance-related stoppages

---

## Proposed Electrostatic Spray System

The proposed system replaces the conventional air-spray guns with automated electrostatic spray guns and continuous paint-feed support.

### Proposed Process Flow

```text
Bottle Generator
        ↓
Electrostatic Spray Queue
        ↓
Electrostatic Spray Booth
        ↓
Curing Oven
        ↓
Inspection
        ↓
Packaging
```

The electrostatic spray system charges paint particles before deposition. This improves paint transfer efficiency, reduces overspray, and creates more uniform coating coverage. Automated guns are mounted around the conveyor to provide consistent 360-degree coating coverage.

---

## Customer Requirements and System Requirements

| Customer Requirement            | System Requirement                                           |
| ------------------------------- | ------------------------------------------------------------ |
| Reduce paint consumption        | Achieve approximately 19–20% paint savings                   |
| Improve coating quality         | Reduce defect rate from 3% to approximately 1%               |
| Increase throughput             | Increase daily output from 90,000 to 108,000 bottles/day     |
| Reduce downtime                 | Reduce unplanned downtime from 500 to 300 hours/year         |
| Improve reliability             | Increase MTBF from 4,000 hours to 6,000 hours                |
| Reduce repair time              | Reduce MTTR from 20 hours to 12 hours                        |
| Improve sustainability          | Reduce overspray, paint waste, and VOC-related material loss |
| Improve production control      | Integrate OEE monitoring and maintenance tracking            |
| Maintain conveyor compatibility | Keep conveyor speed approximately 35 mm/s                    |
| Achieve fast payback            | Recover capital cost in less than 2 months                   |

---

## Methodology and Project Execution

The project was completed through a structured transition-to-production framework. The execution focused on understanding the existing system, defining measurable requirements, modeling the baseline and proposed system, evaluating performance, and justifying the transition financially.

### 1. Baseline Study

The first step was to study the existing beverage bottle coating process. Production data was collected for throughput, paint usage, service time, downtime, defect rate, refill delay, and equipment reliability.

The baseline line produced approximately **90,000 bottles per day** and consumed approximately **15,000 liters of paint per month**.

### 2. Requirements Translation

Customer needs were translated into measurable system requirements. These requirements were used to evaluate whether the proposed electrostatic system could improve quality, throughput, reliability, sustainability, and cost performance.

### 3. Process Flow Comparison

The current air-spray process and proposed electrostatic process were compared. The major change was the replacement of conventional spray guns with automated electrostatic spray guns and continuous paint-feed support.

### 4. Simulation Planning Using JaamSim

A discrete-event simulation model was proposed using JaamSim to compare the baseline air-spray line against the electrostatic spray line.

The simulation entities were bottles, and the main process objects included:

* Entity generator
* Spray queue
* Spray booth
* Curing oven
* Maintenance logic
* Entity sink

The simulation was designed to compare throughput, cycle time, equipment utilization, downtime, and OEE.

### 5. Predictive Maintenance Analysis

Predictive maintenance was included to reduce unplanned downtime and improve equipment availability. The analysis compared baseline downtime against the expected downtime after implementing improved monitoring and condition-based maintenance.

### 6. Cost-Benefit and ROI Analysis

The project evaluated paint savings, predictive maintenance production gains, installed capital cost, annual benefit, ROI, and payback period. Currency values were converted using:

```text
1 USD = ₹94.61
```

### 7. Risk and Implementation Planning

A risk analysis was completed to identify technical, operational, financial, and safety-related risks. Mitigation actions were proposed for inconsistent data, incorrect MTBF/MTTR assumptions, integration issues, operator resistance, maintenance issues, and safety compliance.

---

## Simulation Parameters

| Parameter                 |  Baseline Air-Spray | Electrostatic Spray | Unit           |
| ------------------------- | ------------------: | ------------------: | -------------- |
| Production Rate           |              90,000 |             108,000 | bottles/day    |
| Inter-arrival Time        |                0.96 |                0.80 | seconds        |
| Service Time              |                0.90 |                0.72 | seconds/bottle |
| Conveyor Speed            |                  35 |                  35 | mm/s           |
| MTBF                      |               4,000 |               6,000 | hours          |
| MTTR                      |                  20 |                  12 | hours          |
| Downtime                  |                 500 |                 300 | hours/year     |
| Paint Transfer Efficiency |                  70 |                  88 | %              |
| Paint Used per Day        |                 600 |                 480 | L/day          |
| Paint Used per Month      |              15,000 |              12,000 | L/month        |
| Defect Rate               |                   3 |                   1 | %              |
| Refill Delay              | 30 sec/1000 bottles |                None | -              |
| OEE                       |                  80 |                  91 | %              |

---

## JaamSim Model Structure

```text
Baseline Model:
BottleGenerator → SprayQueue → SprayBooth → CuringOven → Inspection → Packaging → BottleSink

Electrostatic Model:
BottleGenerator → ES_SprayQueue → Electrostatic_SprayBooth → CuringOven → Inspection → Packaging → BottleSink
```

### Simulation Metrics

| Metric                | Formula / Description                            |
| --------------------- | ------------------------------------------------ |
| Throughput            | Completed bottles / simulated days               |
| Cycle Time            | Average completion time - arrival time           |
| Equipment Utilization | Busy time / available time                       |
| Downtime              | Annual unavailable production hours              |
| OEE                   | Availability × Performance × Quality             |
| Bottleneck            | Station with highest utilization or queue length |

---

## Results and Outcomes

The proposed electrostatic spray system showed strong technical and financial benefits.

| Metric                |           Baseline |       Electrostatic | Improvement |
| --------------------- | -----------------: | ------------------: | ----------: |
| Throughput            | 90,000 bottles/day | 108,000 bottles/day |        +20% |
| Average Cycle Time    |             0.96 s |              0.80 s |        -17% |
| Service Time          |             0.90 s |              0.72 s |        -20% |
| Equipment Utilization |                82% |                 90% |         +8% |
| Downtime              |        500 hr/year |         300 hr/year |        -40% |
| Transfer Efficiency   |                70% |                 88% |  +18 points |
| Paint Consumption     |     15,000 L/month |      12,000 L/month |        -20% |
| Defect Rate           |                 3% |                  1% |      -66.7% |
| OEE                   |                80% |                 91% |  +11 points |

The study showed that the electrostatic system can increase output from **90,000 to 108,000 bottles/day**, reduce paint use from **15,000 L/month to 12,000 L/month**, and improve OEE from **80% to 91%**. 

---

## Key Calculations

### Throughput Increase

```text
Throughput Increase = 108,000 - 90,000

Throughput Increase = 18,000 bottles/day
```

```text
Percentage Increase = (18,000 / 90,000) × 100

Percentage Increase = 20%
```

### Cycle Time Reduction

```text
Cycle Time Reduction = ((0.96 - 0.80) / 0.96) × 100

Cycle Time Reduction = 16.67% ≈ 17%
```

### Defect Reduction

```text
Defect Reduction = ((3 - 1) / 3) × 100

Defect Reduction = 66.67%
```

### Downtime Reduction

```text
Downtime Reduction = 500 - 300

Downtime Reduction = 200 hours/year
```

```text
Downtime Reduction Percentage = (200 / 500) × 100

Downtime Reduction Percentage = 40%
```

### Recovered Annual Production

```text
Production Rate per Hour = 90,000 / 24

Production Rate per Hour = 3,750 bottles/hour
```

```text
Recovered Production = 200 × 3,750

Recovered Production = 750,000 bottles/year
```

---

## Predictive Maintenance Impact

Predictive maintenance was added to improve equipment reliability and reduce downtime.

| Metric                      |      Baseline |      New Line |            Impact |
| --------------------------- | ------------: | ------------: | ----------------: |
| Unplanned Downtime          |   500 hr/year |   300 hr/year |              -40% |
| Bottles Lost to Downtime    | 1.875 million | 1.125 million | 750,000 recovered |
| Additional Production Value |             - | ~$15,855/year |   Production gain |
| Availability                |           94% |           97% |         +3 points |
| MTBF                        |      4,000 hr |      6,000 hr |              +50% |
| MTTR                        |         20 hr |         12 hr |              -40% |

Predictive maintenance reduced annual downtime by 200 hours, recovering approximately **750,000 bottles/year** and adding about **$15,855/year** in production value. 

---

## Financial Analysis

The economic analysis used the following exchange rate:

```text
1 USD = ₹94.61
```

### Paint Cost

```text
Paint Price = ₹400/L

Paint Price in USD = 400 / 94.61

Paint Price in USD ≈ $4.23/L
```

### Monthly Paint Cost Before

```text
Baseline Monthly Paint Cost = 15,000 × ₹400

Baseline Monthly Paint Cost = ₹6,000,000

Baseline Monthly Paint Cost ≈ $63,418/month
```

### Monthly Paint Cost After

```text
New Monthly Paint Cost = 12,000 × ₹400

New Monthly Paint Cost = ₹4,800,000

New Monthly Paint Cost ≈ $50,735/month
```

### Monthly Material Savings

```text
Monthly Material Savings = ₹6,000,000 - ₹4,800,000

Monthly Material Savings = ₹1,200,000

Monthly Material Savings ≈ $12,684/month
```

### Annual Material Savings

```text
Annual Material Savings = ₹1,200,000 × 12

Annual Material Savings = ₹14,400,000

Annual Material Savings ≈ $152,204/year
```

### Installed Capital Cost

```text
Installed CAPEX = ₹2,100,000

Installed CAPEX = 2,100,000 / 94.61

Installed CAPEX ≈ $22,196
```

### Total Annual Benefit

```text
Total Annual Benefit = Material Savings + Predictive Maintenance Gain

Total Annual Benefit = ₹14,400,000 + ₹1,500,000

Total Annual Benefit = ₹15,900,000/year

Total Annual Benefit ≈ $168,058/year
```

### Payback Period

```text
Monthly Benefit = ₹15,900,000 / 12

Monthly Benefit = ₹1,325,000/month
```

```text
Payback Period = ₹2,100,000 / ₹1,325,000

Payback Period = 1.58 months ≈ 1.6 months
```

### Annual ROI

```text
ROI = (Total Annual Benefit / CAPEX) × 100

ROI = (₹15,900,000 / ₹2,100,000) × 100

ROI ≈ 757%
```

---

## Cost-Benefit Summary

| Category                               |          Value |
| -------------------------------------- | -------------: |
| Paint Price                            |       ~$4.23/L |
| Baseline Paint Cost                    | ~$63,418/month |
| New Paint Cost                         | ~$50,735/month |
| Monthly Material Savings               | ~$12,684/month |
| Annual Material Savings                | ~$152,204/year |
| Predictive Maintenance Production Gain |  ~$15,855/year |
| Total Annual Benefit                   | ~$168,058/year |
| Installed CAPEX                        |       ~$22,196 |
| Payback Period                         |    ~1.6 months |
| Annual ROI                             |          ~757% |

The project estimated an installed capital cost of about **$22,196**, total annual benefit of about **$168,058/year**, payback of about **1.6 months**, and annual ROI of about **757%**. 

---

## Measured Site Trial Check

A site trial compared the number of bottles coated using 2 liters of paint:

| System                  | Bottles Coated with 2 L Paint |
| ----------------------- | ----------------------------: |
| Existing Air-Spray Gun  |                   131 bottles |
| Electrostatic Spray Gun |                   156 bottles |

```text
Paint Efficiency Improvement = ((156 - 131) / 131) × 100

Paint Efficiency Improvement = 19.08% ≈ 19%
```

Using the measured **19% paint saving**, the material savings are approximately **$12,049/month** and **$144,594/year**. The measured trial payback is approximately **1.84 months**, while the target financial model gives approximately **1.6 months** after including predictive maintenance gains. 

---

## Risk Analysis and Mitigation

| Risk                                   | Mitigation Strategy                                                               |
| -------------------------------------- | --------------------------------------------------------------------------------- |
| Inconsistent baseline data             | Use standard data templates, Gemba observations, and cross-checks                 |
| Incorrect MTBF/MTTR assumptions        | Use historical downtime logs and monthly reliability updates                      |
| Integration issues                     | Validate gun mounting, grounding, safety interlocks, airflow, and paint feed      |
| Operator resistance                    | Provide training on safety, cleaning, startup, shutdown, and troubleshooting      |
| Post-implementation maintenance issues | Use preventive maintenance, vendor support, spare parts, and condition monitoring |
| Financial overestimation               | Report both measured 19% savings and target 20% savings                           |
| Safety and compliance                  | Verify grounding, overspray control, ventilation, and environmental compliance    |

---

## Asset Management Integration

The transition should be supported by a digital asset-management strategy:

* Predictive maintenance sensors for voltage, pressure, flow, spray hours, clogging, and compressor performance
* Centralized asset registry for spray guns, hoses, spare parts, service records, and calibration history
* Condition-based maintenance using real-time operating data
* OEE dashboard for availability, performance, quality, throughput, downtime, defect rate, and paint consumption
* Lifecycle cost tracking for paint usage, energy cost, maintenance cost, spare parts, and total cost of ownership

The project recommends predictive maintenance, asset registry tracking, condition-based maintenance, OEE dashboards, and lifecycle cost management to support full-scale deployment. 

---

## Implementation Plan

| Timeline  | Activity                                                                                        |
| --------- | ----------------------------------------------------------------------------------------------- |
| Weeks 1–2 | Baseline study: collect paint usage, throughput, downtime, defect, cleaning, and refill data    |
| Weeks 3–4 | Process modeling: build baseline and electrostatic models in JaamSim                            |
| Weeks 5–6 | Reliability analysis: estimate MTBF, MTTR, downtime reduction, and PdM benefits                 |
| Weeks 7–8 | Financial analysis: calculate savings, production gains, payback, and ROI                       |
| Week 9+   | Production planning: finalize documentation, review risks, train operators, and plan deployment |

---

## Project Workflow

```text
Identify Current Production Problem
        ↓
Collect Baseline Production Data
        ↓
Translate Customer Needs into System Requirements
        ↓
Map Baseline Air-Spray Process
        ↓
Design Proposed Electrostatic Spray Process
        ↓
Build Simulation Plan in JaamSim
        ↓
Compare Throughput, Cycle Time, Utilization, Downtime, and OEE
        ↓
Analyze Predictive Maintenance Benefit
        ↓
Calculate Paint Savings, ROI, and Payback
        ↓
Evaluate Risks and Mitigation Strategies
        ↓
Develop Implementation Plan
```

---

## Major Learnings

Through this project, I gained practical experience with:

* Transition-to-production planning
* Systems engineering requirement translation
* Manufacturing process analysis
* Smart manufacturing technology evaluation
* Electrostatic spray coating principles
* JaamSim discrete-event simulation planning
* Predictive maintenance and reliability improvement
* MTBF and MTTR analysis
* OEE-based performance evaluation
* Cost-benefit and ROI analysis
* Risk mitigation and implementation planning

---


## Conclusion

This project analyzed the transition from conventional air-spray coating to automated electrostatic spray technology for beverage bottle production. The proposed system improves throughput, coating quality, paint efficiency, equipment reliability, and cost performance.

The expected output increased from **90,000 to 108,000 bottles/day**, while paint consumption decreased from **15,000 L/month to 12,000 L/month** under the target model. Predictive maintenance reduced unplanned downtime by **40%**, improving production capacity and equipment availability.

Financially, the transition is strongly justified. With an installed system cost of approximately **$22,196** and an estimated total annual benefit of approximately **$168,058/year**, the payback period is about **1.6 months**, with an annual ROI of approximately **757%**.

Based on the technical performance, maintenance improvement, and financial return, the electrostatic spray transition is feasible, scalable, and suitable for full-scale production deployment.

```
```
