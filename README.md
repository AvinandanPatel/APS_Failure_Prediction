# Air Pressure System Failures in Scania Trucks
## Problem Statement
- Scania is a Manufacturing Company which manufactures heavy trucks. Air Pressure System(APS) is used in these trucks which generates pressurized air that is utilized for various functions such as breaking and gear changes. The datasets' positive class consists of component failures for a specific component of the APS system. The negative class consists of trucks with failures for components not related to the APS.  
  
- The total cost of a prediction model is the sum of `Cost_1` multiplied by the number of Instances with type 1 failure and `Cost_2` with the number of instances with type 2 failure, resulting in a `Total_cost`.
- In this case `Cost_1` refers to the cost that an unnecessary check needs to be done by an mechanic at an workshop, while `Cost_2` refer to the cost of missing a faulty truck, which may cause a breakdown.   
- Cost-metric of miss-classification:

| True Class | pos | neg |
| --- | --- | --- |
| Predicted Class | | |
| pos | - | cost_1 |
| neg | cost_2 | - |

>`Cost_1 = 10 & Cost_2 = 500`    
>`Total_cost = Cost_1*No_Instances + Cost_2*No_Instances`   

- **Goal:**Minimize the Total_Cost. As Cost_2 is 50 times more than Cost_1 so we need to focus on False Negatives as compared to False Positives.

