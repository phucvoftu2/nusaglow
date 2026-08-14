# SCMission 2026

## Next-Generation Supply Chain — Round 3 Case

## 1. Background

NusaGlow is an Indonesian beauty and personal care company founded in 2007 and headquartered in Tangerang, currently ranked among the top 5 domestic brands in the industry. The company manufactures its full product range at its Tangerang production facility and targets the mid-to-premium consumer segment.

NusaGlow's stated strategic priority is service level and delivery speed first, followed by cost efficiency.

NusaGlow reaches the market through two distinct channels:

- **B2B:** The company sells through a network of regional distributors supplying modern trade chains, pharmacy networks, and general trade outlets nationwide.
- **B2C e-commerce:** NusaGlow operates branded storefronts directly on Shopee, Tokopedia, and TikTok Shop.

When a consumer places a B2C order, the platform's courier network, including SPX, J&T, JNE, AnterAja, Gojek, Grab, and others collects from NusaGlow's nearest stocked location and delivers to the buyer's address. Last-mile delivery fees are charged by the platform directly to the end consumer and are not a cost borne by NusaGlow. However, on-time delivery performance directly affects NusaGlow's seller rating and algorithmic visibility on each platform. The closer NusaGlow's stock to the buyer, the faster the courier can deliver, and the better the measured delivery performance.

NusaGlow's distribution network is structured across the following tiers:

For B2B, all goods flow from the factory through the National Distribution Center (NDC) in Tangerang before reaching customers. From the NDC, stock is distributed through two paths: via Regional Distribution Centers (RDCs) down to DC Satellites and Depots serving local B2B customers, or via DC Directs connected to Depots for markets served without a regional warehousing layer.

For B2C, NusaGlow operates one Fulfillment Center (FC) pilot in Bekasi, opened in mid-2025, receiving stock directly from the NDC and serving Greater Jakarta via platform couriers. All B2C orders outside Greater Jakarta are currently fulfilled from FC Bekasi.

NusaGlow's distribution network currently includes:

- 1 NDC in Tangerang
- 9 RDCs
- 8 DC Directs
- 18 DC Satellites
- 18 Depots
- 1 FC pilot in Bekasi

One customer is exclusively served by one designated Distribution Center.

### Distribution network structure

```text
Factory
  |
  v
NDC
  |-------------------------------> FC ----------------> B2C Customers
  |
  +--> RDC --> DC Satellite --> Depot --> B2B Customers
  |        \-----------------------> B2B Customers
  |
  +--> DC Direct --> Depot -------> B2B Customers
             \--------------------> B2B Customers
```

## 2. Current situation

### Product portfolio

NusaGlow offers a range of beauty and personal care products across **7 categories** and **150 active SKUs**, each with distinct demand characteristics and supply chain requirements. Full details of each SKU are provided in the **Product Master** sheet of the data file.

### Channel dynamics

In recent years, NusaGlow's revenue mix and demand characteristics have shifted materially across channels and geographies. The historical sales data in the attached file reflects these changes and contains the information needed to form a complete picture of current and future demand patterns.

NusaGlow serves the market through the following channels:

| Channel | Sub-Channel | Type |
|---|---|---|
| General Trade | General Trade, Cosmetic Stores,... | B2B |
| Modern Trade | HABA, Dept.Store, Hyper/Super,... | B2B |
| E-Commerce | National E-commerce | B2C |
| Others | Emerging Channel,... | B2B |

### Supply chain costs

NusaGlow's distribution costs are structured as follows:

- **Supply Cost:** Costs from the factory to the NDC.
- **First Mile Cost:** Transportation costs from the NDC to RDCs, DC Directs or FCs.
- **Mid-mile Cost:** Transportation costs from DC to DC (eg RDC to DC Satellite...).
- **Last Mile Cost:** Transportation costs for delivering stock to the end destination. For B2B, this covers delivery from DCs or Depots to retail and trade customers.
- **Handling Cost:** Costs related to managing inbound and outbound volumes at each facility. For B2B, handling is estimated per pallet processed. For B2C, handling covers both manpower for picking and packing and packaging materials, estimated per piece fulfilled.
- **Storage Cost:** Costs related to storing stock at each facility, comprising two components:
  - **Fixed Storage Cost:** The recurring annual cost paid to maintain storage capacity at a facility.
  - **Penalty Storage Cost:** The additional cost incurred when stock volume exceeds the facility's allocated capacity.

### Cost flow

```text
Factory
  |
  | Supply cost
  v
NDC
  |
  +-- First mile cost --> FC --------------------> B2C Customers
  |                        B2C last-mile cost
  |
  +-- First mile cost --> DC Direct
  |                        |
  |                        +-- Mid-mile cost --> Depot
  |                        |                    |
  |                        |                    +-- B2B last-mile cost --> B2B Customers
  |                        |
  |                        +-- B2B last-mile cost ----------------------> B2B Customers
  |
  +-- First mile cost --> RDC
                           |
                           +-- Mid-mile cost --> DC Satellite
                                                |
                                                +-- Mid-mile cost --> Depot
                                                |                    |
                                                |                    +-- B2B last-mile cost --> B2B Customers
                                                |
                                                +-- B2B last-mile cost ----------------------> B2B Customers
```

> **Important:** Supply Cost from factory to NDC is excluded from this analysis as the focus of this study is on distribution, not manufacturing. Last Mile Cost for B2C is excluded from this analysis as delivery fees are charged directly to the end consumer by the platform, not to NusaGlow. B2B cost-to-serve, by contrast, is transport-driven, with first, mid, and last mile transportation as the primary cost components. This structural difference is significant when evaluating how each channel scales and what drives profitability.

## 3. Objective

### Commitment to B2C Transformation: The NusaGlow Next Initiative

NusaGlow has built one of Indonesia's most reliable B2B distribution networks over the past two decades. Yet the market is shifting faster than the network was designed to accommodate. E-commerce now represents a significant and rapidly growing share of total revenue, driven by platforms where delivery speed and on-time performance are the primary determinants of seller visibility and revenue access.

The root cause of the current B2C challenge is structural. NusaGlow's existing DCs were designed for B2B logic, moving pallets to distributors and trade customers, and are not configured to support B2C fulfillment at the order level. The FC pilot in Bekasi, opened in mid-2025, was NusaGlow's first step toward dedicated B2C infrastructure and currently serves as the primary fulfillment point for all B2C orders nationwide. For buyers in Greater Jakarta, this works reasonably well. For buyers in Sumatra, Kalimantan, Sulawesi, and the outer islands, orders shipped from Bekasi take considerably longer to arrive, and the FC regularly runs out of stock under demand surges, forcing NusaGlow to rely on platform warehouses where only limited inventory has been pre-positioned. The result is a fulfillment model that is stretched beyond what a single facility in West Java was ever designed to support.

The consequence of the current setup is immediate. Shopee has issued a formal performance notice to NusaGlow, citing on-time delivery rates below the Preferred Seller threshold of **95% of orders delivered within 3 days** across provinces outside Java. NusaGlow has **90 days** from the notice date to bring performance up to the required standard. Failure to do so will result in the loss of Preferred Seller status, with direct consequences for product visibility in search results and access to double-date campaigns that represent a disproportionate share of annual B2C revenue.

The network investment decision is therefore more complex than it first appears. Expanding Bekasi addresses one problem but not the other. Opening regional FCs closer to demand on other islands addresses delivery time but requires capital and operational commitment under uncertain future demand. NusaGlow's planning team must evaluate these options rigorously: projecting where B2C demand will be concentrated, assessing which facility configurations close both the stockout and the distance gap within the available investment envelope, and building a recommendation that holds up not just under today's demand map but across the range of plausible futures.

## 4. Mission

### 4.1. Demand projection and signal decomposition

Using the historical sales data provided, develop a volume forecast by product category, by channel (B2B/B2C), and by region through 2030.

As part of this task, briefly characterize the demand signal types relevant to B2C planning:

- Stable baseline growth
- Predictable seasonal events
- Platform promotion cycles
- Social commerce spikes

For each signal type, identify the lead time required to act before the demand window opens. This does not require quantitative modeling and can be presented as a short summary. It will serve as the analytical foundation for Task 4.

All data inconsistencies must be identified, documented, and resolved before forecasting begins. The output of this task is the demand foundation for Tasks 3 and 4.

### 4.2. Baseline analysis

Calculate NusaGlow's current operational and financial baseline using the most recent full year of available data.

The baseline must establish:

- Current cost-to-serve by channel and by region
- Warehouse utilization across the network
- Stockout frequency across the network, with particular attention to the Bekasi FC
- B2C on-time delivery performance versus Shopee's **95% within 3 days SLA** requirement by province

This baseline is the reference point against which all proposed configurations will be evaluated.

### 4.3. Fulfillment network strategy

#### Part A: Resolving the immediate constraint

NusaGlow has **90 days** to bring its B2C on-time delivery performance up to Shopee's Preferred Seller threshold.

Evaluate the options available, including:

- Pre-positioning additional stock at platform warehouses
- Increasing inventory depth at the Bekasi FC
- Opening new regional FCs

For each option, provide a quantified assessment across two dimensions:

1. Service level improvement
2. Incremental cost-to-serve impact

Where the most appropriate structural solution requires more time than the notice window allows, identify specific interim actions that can demonstrate measurable improvement while the longer-term solution is being put in place.

The recommendation must explicitly acknowledge the trade-offs involved, as no single option is superior across all dimensions simultaneously.

#### Part B: Fulfillment network design under uncertainty

Using the demand projections from Task 1 and the cost baseline from Task 2, propose an optimal B2C fulfillment network configuration for NusaGlow through 2030.

The evaluation must address the Bekasi question directly: whether expanding the existing FC, opening additional regional FCs, or a combination of both represents the most robust path forward, given the structural gap between a single West Java facility and the geography of B2C demand across the archipelago.

NusaGlow's management has approved a total B2C infrastructure investment envelope of **50 billion IDR** for the **2026 to 2030** period, covering all CAPEX and cumulative OPEX for new FC openings.

The CAPEX envelope and monthly OPEX benchmarks by FC location tier are provided in the data file. FC locations closer to urban demand centers offer better SLA coverage but carry higher fixed costs, while locations in secondary or outer-island cities reduce OPEX and connect to broader regional volumes at the cost of longer delivery lead times.

The proposed configuration must:

- Make this trade-off explicit
- Defend the chosen locations against the inherent uncertainty of future B2C demand
- Remain within the approved investment envelope

For the proposed network, present:

- Projected cost-to-serve per unit by region
- Projected on-time delivery SLA coverage versus current state
- A payback estimate with sensitivity to key demand assumptions

### 4.4. Intelligent supply chain

The demand forecast in Task 1 and the network design in Task 3 rest on assumptions about a B2C environment that is inherently difficult to predict. Platform promotion calendars shift, social commerce spikes emerge without warning, and regional demand patterns evolve faster than annual planning cycles can accommodate.

The physical network NusaGlow builds must therefore be paired with a planning capability that can sense demand changes early, position stock ahead of the window, and support faster decisions across a more distributed fulfillment footprint.

Based on the operational gaps and demand patterns identified in the previous tasks, design **one AI-powered planning capability** that NusaGlow should develop to address its most critical planning challenge.

The proposal must specify:

- What problem it solves in the context of this case
- What data it requires
- What output it produces for the planning team
- At what time horizon it operates
- How human judgment remains part of the process

Teams are then encouraged to illustrate how this capability would be experienced in practice through a concept for a **unified weekly planning dashboard**:

- What a planner would see
- What risks and opportunities would be surfaced
- What decisions the interface is designed to support

A visual layout or brief outline is sufficient and will be treated as a strong complement to the analysis above.

## Final presentation requirement

Please prepare a PowerPoint deck, submitted in PDF format:

- In English
- Maximum **10 slides**
- Meant to be presented in the final round
- Concise and effective, considering the limited presentation time
- Designed for an audience that may not be familiar with all details and calculations
- Focused on key ideas and results

## Suggested formulas

```text
First Mile Cost / Mid-mile Cost = Cost Per Pallet × Volume In Pallet

Handling Cost (B2B) = Handling Cost Per Pallet × Volume In Pallets

Handling Cost (B2C) = Handling Cost Per PCS × Volume In PCS

Last Mile Cost (B2B) = Cost Per Pallet × Volume In Pallet

Last Mile Cost (B2C) = Cost Per PCS × Volume In PCS
```

## 5. Handover material

There are two attached files:

- **SCMission2026_Round3_Data** — zip files with the inputs for the analytical problem
- **Case_Answer** — the template to partially answer two questions

You will have to submit the **Case_Answer** file with the gray cells properly filled, without changing the tab layout or format, or adding any information, comment, or result outside the gray cells.

The **SCMission2026_Round 3_Data** file is not meant to be edited.

You must add any necessary tab with the exercise calculations in the same **Case_Answer** file.

Furthermore, you and your team are allowed to submit any supplemental material (Jupyter Notebook, Rmarkdown report, etc.), but this would not be the focus of the scoring process.*

The material will be evaluated based on the following parameters:

- Precision (over expected answer)
- Clarity (calculation tabs to support the answers)
- Accuracy

\* Any additional materials submitted by the team will be reviewed at the jury's discretion. However, due to the large amount of documentation provided, these materials may not be fully reviewed.
