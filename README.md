\# NoVa Data Center Carbon Emissions Calculator



A lightweight web-based dashboard for estimating and analyzing \*\*Scope 1 and Scope 2 carbon emissions\*\* from data center operations.



This project provides a simplified carbon accounting model that integrates operational parameters such as IT load, power usage effectiveness (PUE), grid carbon intensity, renewable electricity usage, and refrigerant leakage.



The tool allows users to quickly evaluate \*\*carbon performance, emissions intensity, and operational risk\*\* for a data center facility.



---



\# Features



\- Estimate \*\*annual Scope 1 and Scope 2 emissions\*\*

\- Interactive emissions \*\*dashboard\*\*

\- \*\*Scope 1 breakdown\*\* by emission source

\- \*\*Scope 2 performance matrix\*\* based on efficiency and grid intensity

\- Emissions \*\*intensity metrics\*\*

\- Visualizations using \*\*donut charts and stacked bars\*\*

\- Simple \*\*web-based calculator (no backend required)\*\*



---



\# Dashboard Outputs



The calculator generates several analytical outputs.



\## Overall Emissions Breakdown



A donut chart showing the proportion of:



\- Scope 1 emissions

\- Scope 2 emissions



This visualization highlights the typical pattern in data centers where \*\*Scope 2 emissions dominate total carbon output\*\*.



---



\## Scope 1 Emissions Breakdown



A stacked bar chart visualizing the contribution of different direct emission sources:



\- Diesel generators

\- Natural gas consumption

\- Refrigerant leakage



This allows users to identify \*\*which operational sources contribute most to direct emissions\*\*.



---



\## Scope 2 Emission Performance Matrix



Facilities are positioned in a \*\*2×2 performance matrix\*\* based on:



\- Power Usage Effectiveness (PUE)

\- Grid Carbon Intensity



Quadrant categories include:



| Quadrant | Description |

|--------|-------------|

| Efficient Asset | Low PUE and low grid carbon intensity |

| Efficiency Risk | High PUE but low grid carbon intensity |

| Location Risk | Low PUE but high grid carbon intensity |

| Dual Risk | High PUE and high grid carbon intensity |



Benchmark values used in the model:



Energy Efficiency Benchmark  

PUE = 1.35



Grid Carbon Intensity Benchmark  

367 kg CO₂e / MWh



---



\# Emissions Methodology



The calculator follows the \*\*Greenhouse Gas Protocol\*\* framework.



\## Scope 1 Emissions (Direct)



Scope 1 emissions represent \*\*direct emissions generated onsite\*\* from fuel combustion and refrigerant leakage.



Diesel emissions:



Diesel Emissions = Diesel Consumption × Diesel Emission Factor



Natural gas emissions:



Gas Emissions = Gas Consumption × Natural Gas Emission Factor



Refrigerant leakage emissions:



Refrigerant Emissions = Charge × Leak Rate × GWP



Where:



| Variable | Description |

|--------|-------------|

| Charge | Refrigerant quantity (kg) |

| Leak Rate | Annual refrigerant leakage (%) |

| GWP | Global Warming Potential |



Total Scope 1 emissions:



Scope1 = Diesel + Natural Gas + Refrigerant



Results are converted from \*\*kg CO₂e to tCO₂e per year\*\*.



---



\## Scope 2 Emissions (Electricity)



Scope 2 emissions represent \*\*indirect emissions from purchased electricity\*\* used to operate the data center.



Scope 2 calculation formula:



Scope2 = IT Load × 8760 × PUE × Grid EF × (1 − Renewable%)



Where:



| Variable | Description |

|--------|-------------|

| IT Load | IT power demand (MW) |

| 8760 | Hours per year |

| PUE | Power Usage Effectiveness |

| Grid EF | Grid emission factor (kg CO₂e / MWh) |

| Renewable % | Percentage of renewable electricity |



Final results are expressed as:



tCO₂e / year



---



\# Emissions Intensity Metrics



To enable comparison across different facilities, several normalized emissions indicators are included.



Facility energy intensity:



Total Emissions / Facility Energy (MWh)



IT capacity intensity:



Total Emissions / IT Load (MW)



Revenue normalized emissions:



Total Emissions / Revenue



Scope 1 intensity:



Scope1 Intensity = Scope1 (kg CO₂e) / IT Energy (MWh)



Scope 2 intensity:



Scope2 Intensity = PUE × Grid EF × (1 − Renewable%)



Units:



kg CO₂e / IT MWh



---



\# Project Structure

project/

│

├── index.html # Main dashboard interface

├── README.md # Project documentation



---



\# How to Run



This project runs entirely in the browser.



Step 1: Clone the repository



git clone https://github.com/tai0603/NoVa-Data-Center-Carbon-Calculator.git



Step 2: Navigate into the project folder.



Step 3: Open the dashboard by launching:



index.html



in any modern web browser.



No backend installation or additional dependencies are required.



---



\# Example Inputs



Typical testing values:



| Variable | Example |

|--------|--------|

| IT Load | 2 MW |

| PUE | 1.4 |

| Grid EF | 400 kg/MWh |

| Renewable Share | 20% |

| Diesel Consumption | 5000 gallons |

| Natural Gas Consumption | 20000 therms |



Expected approximate results:



\- Scope 1 ≈ 150–200 tCO₂e/year

\- Scope 2 ≈ 7000–8000 tCO₂e/year



---



\# Assumptions



This simplified model makes several assumptions:



\- IT systems operate \*\*continuously at full utilization\*\*

\- Annual operating hours = \*\*8760\*\*

\- Grid carbon intensity remains constant

\- Renewable electricity offsets Scope 2 proportionally

\- Refrigerant leakage rates are estimated using user input



These assumptions allow the model to capture \*\*the primary emission drivers of data center operations\*\* while keeping the calculator simple and easy to use.



---



\# Purpose of the Project



This project demonstrates how carbon accounting principles can be applied to \*\*data center sustainability analysis\*\*.



It highlights:



\- The dominance of Scope 2 emissions in data center operations

\- The impact of energy efficiency (PUE)

\- The role of grid carbon intensity

\- The usefulness of emissions intensity metrics for benchmarking



The calculator can serve as a starting point for:



\- sustainability dashboards

\- operational carbon analysis

\- energy efficiency benchmarking tools



---



\# License



This project is created for \*\*educational and analytical purposes\*\*.

