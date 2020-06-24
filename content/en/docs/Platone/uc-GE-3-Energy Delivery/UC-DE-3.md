# 1. Description of the Use Case

## 1.1. Name of the Use Case

*Use case identification*

| ID  | Area /Domain(s)/Zone(s)| Name of the Use Case |
| --- | ---                    | ---                  |
| UC-DE-3| **Area:** Energy system </br> **Domain:** Distribution, Customer Premise, Field, DER </br> **Zones:** Operation, Enterprise, Process, Field | Flex Provision: </br> Energy Delivery |

***Notes:***

* **ID** - uniqe identification label: DE-1/GR-3/IT-2

* **Area /Domain(s)/Zone(s)** - placement of the use case in the SGAM domains and zones. It can be left blank if you are not sure.

## 1.2. Version Management

*Version management*

|Version No.|Date     |Name of author(s)|Changes|Approval status|
|---        |---      |---              |---    |---            |
|0.1|1st April 2020|Thorsten Gross|Initial creation|Draft|
|0.2|2nd June 2020|Katarzyna Zawadzka|Initial creation in Github|Draft|
|0.3|24th June 2020|Benjamin Petters|Extended description and added technical part|Draft|



## 1.3. Scope and Objectives of Use Case

*Scope and objectives of use case*

|||
| --- | --- |
| **Scope** | Energy communities with a high proportion of self-generation and flexible consumers and storage will maximize the self-consumption of locally generated energy. The communities will not be able to fully meet their own needs with locally generated energy. Energy deficits must be compensated by the supplying distribution network. Energy deficits occurring shall not be balanced via a load exchange with the distribution grid in real time, but be forecasted and provided as discrete package ahead at fixed time slots and be stored in local storages until demand arises. . <br/> Networks: LV <br/> Markets: None|
| **Objective(s)** |Forecasting of residual energy demand of an energy community, Calculation of required energy packages serving energy deficits, Determination of power exchange schedule for the energy community for the grid connection point LV/MV (time and power of load exchange) , Determination of a setpoint schedule for individual local asset to meet energy, community setpoint schedule, Execution of defined power exchange between energy community and the distribution network|
| **Related business case(s)** | Integration of local energy communities in network management strategies for the stabilization and uniform utilization of the network|

***Notes:***

* **Scope** - describes the aims and boundaries of the use case in a short, precise text.

* **Objective(s)** - goals of the use case, in form of bullet points and a short headline.

* **Realted business case(s)** - optional

## 1.4. Narrative of Use Case


**Short description**

Local energy communities (LEC, CEC) are likely to emerge in Europe in the near future but will most likely retain an interconnection to the distribution grid. These communities will require a large share of flexibility to enable their primary use case (islanding).
In the absence of sufficient generation and storage, the community will not be able to be self-sufficient all time. Occurring energy deficites must be provided by the distribution network. Instead of a real time energy supply by the connected distribution network, energy deficits should be forecast and supplied as an energy package with a defined time, duration and power value for the load exchange at the LV/ MV-grid connection point that connects the community with the distribution grid. The energy package shall be stored in local storages within the community and available for use, when the demand is rising. Outside of the defined periods of energy provision, no power exchange shall all the grid connection point shall take place, according to DE-UC1.

**Complete description**

add text - longer narrative from user viewpoint about *what* happens *how*, *where*, *when*, *why* and *under which assumptions*. It has to be written in a way that it can also be understood by non-experts.


## 1.5. Key Performance Indicatiors (KPI)

|ID   |Name   | Description   | Reference to mentioned use case objectives|
|-----|-------|---------------|-------------------------------------------|
| KPI3-01 | will follow... | |
| KPI3-02 | will follow... | |
| KPI3-03 | will follow... | |

***Notes:***

Can be left blank now

## 1.6. Use case conditions

|Assumptions| Prerequisites|
|-----------|-------------|
| Formation of energy communities in future distribution grid  | Content of the Clean Energy Packages have to be implemented by national regulation and legislations enabling energy community formation with a central EMS. Additional incentive mechanisms for formation will have to be implemented by regulation and legislation. |
| Integration of battery storage in control mechanisms of the DSO | Rules must be implemented that enables the DSO to control battery storage for network-related purposes. |

***Notes:***
* **Assumptions** - general presumptions about conditions or system configurations (e.g. customer's consent required for some steps; simulation of TSO)
* **Prerequisites** - specify which requirements have to be met so that the basis scenario use case can be successfully accomplished.


## 1.7. Further information to the use case for classification/mapping

OPTIONAL - you can leave it blank

|Relation to other use cases|
|---------------------------|
| UC 3 requires UC 1 as a prerequisite|
|**Level of depth**|
|Primary Use Case|
|**Prioritisation**|
| very important |
|**Generic, regional or national relation**|
|Germany|
|**Nature of the use cases**|
| technical |
|**Further keywords for classification**|
|Medium Voltage Grid, Low Voltage Grid, Monitoring, Reporting, Steering|

***Notes:***

* **Relation to other use cases** - relation to other use cases in the same project or thematic area. Possible relation types are for instance include, extend, invoke, or associate.

* **Level of depth** - reflects the degree of specialisation of the use case. Although no common notation is settled, descriptions like high level use case, generic, detailed, or specialised use case are often used.

* **Prioritisation** - helps to rate the use cases in a project from very important to nice-to-have with labels like obligatory/mandatory or optional which have to be agreed upon beforehand.

* **Generic, regional or national relation** - for the purpose of generalisation if use case is applied to areas where restictions by law or silimiar issues occur.

* **Nature of the use cases** - describes the viewpoint and field of attention like *technical, political, business/market, test*, etc.


## 1.8. General remarks

|General remarks|
|---|
|-	Use case 1 is anticipated to emerge as a result of the Clean Energy Package, driven by the bottom-up demand of customers and local communities.|
|-	It is a prerequisite for the advanced use 2 - 4|

***Notes:***

Add any remarks which do not fit in any other category

# 2. Diagrams of Use Case

![Diagram of Use Case](UC2_2_Diagram_of_Use_Case.png)

# 3. Technical Details

## 3.1. Actors

| **Actor Name** | **Actor Type** | **Actor Description** | **Further information specific to this Use Case** |
| --- | --- | --- | --- |
| Standard Household | System | Household with a standard load profile energy consumption of a single household. | No direct measurement of energy consumption, demand not controllable (passive consumer). | 
| Agricultural Buildings | System | Energy consumer with a standard load profile of an agricultural building. | No direct measurement of energy consumption, demand not controllable. | 
| Street light | System | Household with a standard load profile energy consumption of a street light. | No direct measurement of energy consumption, demand not controllable. | 
| Roof Top Photovoltaic System | System | Power generation directly correlated with solar radiation at location. | Limited controllability (can be curtailed in extreme cases). Located on customers premise and can be operated in combination with a battery storage system, for optimization of own consumption. | 
| Integrated Controller | Device | Summarises all controllers that are already installed in local flexible loads. | |
| Retrofit Controller | Device | Summarises all controllers that a installed as a retrofit solution to make flexible loads, controllable. | |  
| Current Sensor | Device | Summarises all sensors that measure the current and delivers values as input for the EMS for load flow monitoring. | PMU |
| Voltage Sensor | Device | Summarises all sensors that measure the voltage and delivers values as input for the EMS for load flow monitoring. | PMU |
| Temperature Sensor | Device | Summarises all sensors that measure the temperature of the heat storage be used as input for the EMS SOC calculation of flexible heaters (head pumps, night storage heaters). | Retrofit or integrated in existing system of customers heater. |
| SOC/SOE Sensor | Device | Summarises all sensors that measure the SOC/SOE of storages. | Integrated in BESS and household battery storages |
| Battery Energy Storage System (BESS) | System | Stores electrical energy | 300 kW/600 kWh, fully integrated in EMS and full time available for UC. |
| Household Energy Storage | System | Stores electrical energy | Integrated in EMS and full time available for UC. |
| Storage Heater | Device | Electrical Heater with a large-scale water storage, able to store electrical generated heat. Heater is used by household for generation of domestic heat. | Could be provided by customer households. |
| Heat pump | Device | Electrical Heater able to store electrical generated heat for 1 -2 hours. Heater is used by household for generation of domestic heat. | At least one is targeted to be integrated in UC. |
| Weather Forecast Service Provider | External System | Provides weather forecasts for the next 24h of wind, solar radiation, cloudiness and temperature. | |
| ALF-C Controller | System | -	Monitors local generation and demand </br> - monitors available flexibility and storages </br> -	forecasts generation, demand and available flexibility via historic data and weather forecasts </br> -receives “Islanding” -Trigger from ALF-C Use Case Modul and determines and dispatches setpoints for individual assets | In a productive environment operator can could be DSO, retailers, storage system operators or any other energy service provider. |
| ALF-C Use Case Modul | System | Calculated the setpoint or setpoint schedule for the ALF-C Controller | |
| DSO (Avacon) | Person | Local grid operator | In future done by DSO, TSO, marketer or energy service providers |




***Notes:***

* **Actor Type** - Device/ Sytem/ Person

## 3.2. References

OPTIONAL - you can leave it blank

| **No.** | **References Type** | **Reference** | **Status** | **Impact on Use Case** | **Organistaor / Organisation** | **Link** |
| --- | --- | --- | --- | --- | --- | --- |
|add text|add text|add text|add text|add text|add text|


# 4. Step by Step Analysis of Use Case

## 4.1. Overview of Scenarios

| **No.** | **Scenario Name** | **Primary Actor** | **Triggering Event** | **Pre-Condition** | **Post-Condition** |
| --- | --- | --- | --- | --- | --- |
| 1 |Energy Delivery| •	ALF-C </br> •	Energy Storage </br> • Flexible Load </br> • Sensors| •Forecast of an energy deficit | •UC 1 - is applied </br> •	Sensors and actuators are connected  with  ALF-C </br> • Enough flexible loads and storages capacity are available for balancing |  </br>  • User has triggered UC 3 and provided necessary time and duration |
| 2 | See UC DE-1| •	See UC DE-1| See UC DE-1 | •See UC DE-1 ||



***Notes***

This part describes the possible scenarios of the use case. The scenarios should comply with the sequence diagrams in Sect. 2 of the template, so that every step describes one part of a communication or action. Apart from a normal success scenario, different failure scenarios or alternatives can be included to describe situations where preconditions are not satisfied or unwanted states are attained.

* **Primary Actor** - the first actor appearing in the scenario at the incident causing the scenario to begin.

* **Triggering Event** - the incident causing the scenario to begin.

* **Pre-Condition** - indicates which terms have to be fulfilled for the scenario to be executed.

* **Post-Condition** - indicates which terms should be valid after the scenario. TIt can also specify whether a scenario has been successfully completed or not.

## 4.2. Steps – Scenarios

**Scenario Name: No. 1 - Energy Delivery**

| **Step No.** | **Event.** | **Name of Process/ Activity** | **Description of Process/ Activity.** | **Service** | **Information Producer (Actor)** | **Information Receiver (Actor)** | **Information Exchanged** | **Requirements, R-ID** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Initiating of UC 3 ||Operator sets ALF-C mode of operation to UC 3 and sets via a GUI duration of UC 3 application as well as times (t) and time slots (dt) for the delivery of packages | REPORT | USER | ALF-C | I - 01 | |
| 2 | ALF-C requests data of total generation/ consumption | Data-Aquisition | The ALF-C request measurement values from the sensor located at the secondary substation to provide measurement data (P_Breaker) of the power exchange along the MV/LV grid connection point. </br> Then data will be pushed by sensor every 10 seconds. | GET | ALF-C | Sensor | I-04 |   |
| 3 | Sensor (grid connection point) provides values | Transmitting data | The local measurement device (PMU) located at the grid connection point measures the residual power export and sends data to the ALF-C (PBreaker). </br> Step will be repeated every 10 seconds. | CHANGE | Sensor| ALF-C|  I-05 |
| 4 | ALF-C requests data of current of demand/SOC of local flex | Data-Aquisition | The ALF-C sends request to sensors to provide load demand and SOC values of local customer flexible loads, customer storages and the BESS. Then data will be pushed by PMU every 15 minutes. | GET | ALF-C | Sensors | I-04 | |
| 5 | Local sensors provide data | Transmitting data | Local sensors provide measurements values and data to the ALF-C. </br> Step will be repeated every 15 minutes. | CHANGE | Sensor, | ALF-C | I-05 | |
| 6 | All data is collected | Evaluation and determination of control strategy and setpoints | Based on provided measurement data, asset key data. ALF-C calculates the power bandwith and/or SOC of each asset available for steering (PFlex, available). </br> The ALF-C determines for each asset a setpoint to reach Ptarget. The determination of setpoint is repeated every 10 seconds for BESS and every 15 minutes for flexible loads and storages located at customer premise. | Create | ALF-C | ALF-C | | |
| 7 | Individual setpoints determined | Transmitting setpoints to actuators | The ALF-C sends setpoints to actuators located in the field to increase their consumption. </br> This signal is sent each ten seconds to the BESS and every 15 minutes to actuators located at customer premise and replaces the default signal until the ALF-C calculates a setpoint. | EXECUTE | ALF-C | Actuators | I-06 | |
| 8 | Setpoint send to actuators | Verification of setpoint execution Comparison of target and measured values | The ALF-C compares measured values from the grid connection P_Breaker point with the target values (P'_Breaker). In case of deviation the setpoint are redefined by walking through step numbers 2 to 8. The process is continuously cycled until the end of use case. | CREATE | Sensor| ALF-C | | |
| 9 | End of Use Case 2 | End of Use Case 2 | The use case ends, when a user triggers another use case, or in a case of lack of flexibility to reach Ptarget. | REPORT | USER | ALF-C | I-01 |


**Scenario Name: No.  - Decreasing Residual Energy Demand **

| **Step No.** | **Event.** | **Name of Process/ Activity** | **Description of Process/ Activity.** | **Service** | **Information Producer (Actor)** | **Information Receiver (Actor)** | **Information Exchanged** | **Requirements, R-ID** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Initiating of UC 2 ||Operator sets ALF-C mode of operation to UC 2 and set via a GUI the target setpoint for load exchange aalong the grid connection point MV/LV P'_Breaker and duration (t) | REPORT | USER | ALF-C | I - 01 | |
| 2 | ALF-C requests data of total generation/ consumption | Data-Aquisition | The ALF-C request measurement values from the sensor located at the secondary substation to provide measurement data (P_Breaker) of the power exchange along the MV/LV grid connection point. </br> Then data will be pushed by sensor every 10 seconds. | GET | ALF-C | Sensor | I-04 |   |
| 3 | Sensor (grid connection point) provides values | Transmitting data | The local measurement device (PMU) located at the grid connection point measures the residual power export and sends data to the ALF-C (PBreaker). </br> Step will be repeated every 10 seconds. | CHANGE | Sensor| ALF-C|  I-05 |
| 4 | ALF-C requests data of current of demand/SOC of local flex | Data-Aquisition | The ALF-C sends request to sensors to provide load demand and SOC values of local customer flexible loads, customer storages and the BESS. Then data will be pushed by PMU every 15 minutes. | GET | ALF-C | Sensors | I-04 | |
| 5 | Local sensors provide data | Transmitting data | Local sensors provide measurements values and data to the ALF-C. </br> Step will be repeated every 15 minutes. | CHANGE | Sensor, | ALF-C | I-05 | |
| 6 | All data is collected | Evaluation and determination of control strategy and setpoints | Based on provided measurement data, asset key data. ALF-C calculates the power bandwith and/or SOC of each asset available for steering (PFlex, available). </br> The ALF-C determines for each asset a setpoint to reach P'_Breaker. The determination of setpoint is repeated every 10 seconds for BESS and every 15 minutes for flexible loads and storages located at customer premise. | Create | ALF-C | ALF-C | | |
| 7 | Individual setpoints determined | Transmitting setpoints to actuators | The ALF-C sends setpoints to actuators located in the field to decrease their consumption. </br> This signal is sent each ten seconds to the BESS and every 15 minutes to actuators located at customer premise and replaces the default signal until the ALF-C calculates a setpoint. | EXECUTE | ALF-C | Actuators | I-06 | |
| 8 | Setpoint send to actuators | Verification of setpoint execution Comparison of target and measured values | The ALF-C compares measured values from the grid connection P_Breaker point with the target values (P'_Breaker). In case of deviation the setpoint are redefined by walking through step numbers 2 to 8. The process is continuously cycled until the end of use case. | CREATE | Sensor| ALF-C | | |
| 9 | End of Use Case 2 | End of Use Case 2 | The use case ends, when a user triggers another use case, or in a case of lack of flexibility to reach Ptarget. | REPORT | USER | ALF-C | I-01 |



***Notes***

This part describes the possible scenarios of the use case. The scenarios should comply with the sequence diagrams in Sect. 2 of the template, so that every step describes one part of a communication or action. Apart from a normal success scenario, different failure scenarios or alternatives can be included to describe situations where preconditions are not satisfied or unwanted states are attained.

* **Event** - Event triggering a step, specific for that use case.

* **Name of Process/ Activity** - general classification of process/activity (e.g. data aquisition).

* **Description of Process/ Activity** - more detailed description of the step.

* **Service** - addresses the nature of the information flow. Possible: GET (The information receiver obtains information from the
information producer after an implicit request.), CREATE (The information producer creates an information object.), CHANGE (The information producer performs an update of the information at the information receiver’s.), DELETE (The information producer deletes information of the receiver.), CANCEL/CLOSE (A process is terminated.), EXECUTE (An action or service is performed.), REPORT (The information producer supplies information of its own account.), TIMER (The actor which represents both information producer
and receiver has to enforce a waiting period.), REPEAT (A number of steps has to be repeated until a break condition (stated in the field Event) is satisfied. The contemplated steps have to be added in parentheses.).

* **Information Producer and Receiver (Actor)** - actors from actor list in section 3.1

* **Information exchanged (IDs)** - ID of the information defined further in section 5

# 5. Information Exchanged

|**Information exchanged ID**|**Name of Information** | **Description of Information Exchanged** | **Requirements to information data** |
| --- | --- | --- | --- |
| I-01 | Signal from user via GUI | A user triggers the use case via an GUI to the ALF-C to apply islanding. The trigger signal is: </br> 0 = stop current use case </br> 1 = application of UC 1 </br> 2 = application of UC 2 </br> 3 = application of UC 3 </br> 4 = application of UC 4 <br/> Based on the UC 2 trigger the ALF-C sets the target setpoint for the load - exchange along the grid connection point accoring to user input (Target Setpoint P'_Breaker). | |
| I-02| Signal from ALF-C to External System | Trigger to provide weather forecast data | |
| I-03| Weather forecasts | -	Solar radiation (t + 24h) </br> -	Cloudiness (t + 24 h) </br> -	Temperature (t + 24 h) </br> -	Humidity (t + 24 h) </br> - Windspeed (t + 24 h) | |
| I-04| Signal from the ALF-C to sensor at secondary substation | The ALF-C sends a signal to sensors to get current measurements. | |
| I-05| Signal from sensor | The sensor sends measurement values containing:
voltage (U), current (I) and angle of phase (Phi) values for all 3 phases | |
| I-06| Signal from integrated sensors | The measurement of PMU contains voltage (U), current (I) and angle of phase (Phi) values, SOC, SOE and/or temperature | |

***Notes***

* **Information exchanged ID** - unique number (I-01,I-02...) for identification

* **Requirements to information data** - optional, defined in section 6

# 6. Requirements (optional)

# 7. Common Terms and Definitions

| **Term** | **Definition** |
| --- | --- |
|||


# 8. Custom Information (optional)

| **Key** | **Value** | **Refers to Section** |
| --- | --- | --- |
|||
