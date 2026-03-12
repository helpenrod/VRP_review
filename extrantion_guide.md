Below is a **coding guide for PRISMA data extraction table**. Each element includes:

* **What it means**
* **How to identify it in a paper**
* **Examples**
* **Notes for consistent coding**

---

# Data Extraction Guide for PRISMA Review

**Article:** *From Models and Algorithms to Decision Makers: A Review of Hybrid Augmented Intelligence in the Vehicle Routing Problem*

---

# Bibliographic Information

## DOI

**Description**
The Digital Object Identifier of the article. It uniquely identifies the publication.

**Where to find it**

* First page of the paper
* Scopus / publisher page

**Examples**

* `10.1016/j.cor.2021.105312`
* `10.1287/trsc.2019.0923`

**Notes**

* Always record the DOI exactly as written.
* Do not include URL prefixes such as `https://doi.org/`.


---

# Problem Context

## VRP Variant

**Description**
Type of vehicle routing problem addressed.

**Common categories**

| Variant        | Meaning                         |
| -------------- | ------------------------------- |
| CVRP           | Capacitated VRP                 |
| VRPTW          | VRP with Time Windows           |
| MDVRP          | Multi-Depot VRP                 |
| DVRP           | Dynamic VRP                     |
| PDVRP          | Pickup and Delivery VRP         |
| Stochastic VRP | Uncertain demand or travel time |

**Example**
Paper solving **vehicle routing with time windows**

→ `VRPTW`

**Notes**
Use the **main variant studied** in the paper.

---

## Application Context

**Description**
Real-world logistics or transportation domain addressed.

**Examples**

| Context             | Description               |
| ------------------- | ------------------------- |
| Urban delivery      | Last-mile parcel delivery |
| Waste collection    | Garbage truck routing     |
| Emergency logistics | Disaster response         |
| Ride sharing        | Passenger transportation  |
| Food delivery       | On-demand meal delivery   |

**Example**
Paper about routing **electric delivery vans in cities**

→ `Urban delivery`

**Notes**
If the paper is purely methodological, write:

`None / generic VRP`

---

## Data Type

**Description**
Type of dataset used for experiments.

**Categories**

| Category            | Meaning                           |
| ------------------- | --------------------------------- |
| Benchmark instances | Standard VRP datasets             |
| Real-world data     | Real logistics data               |
| Synthetic data      | Artificially generated data       |
| Mixed               | Combination of benchmark and real |

**Examples**

| Paper uses Solomon dataset | `Benchmark` |
| Paper uses company delivery data | `Real-world` |

---

# Algorithmic Characteristics

## Optimization Approach

**Description**
General optimization paradigm used.

**Typical categories**

| Approach      | Description                                      |
| ------------- | ------------------------------------------------ |
| Exact         | Mathematical optimization (MILP, branch-and-cut) |
| Heuristic     | Constructive heuristic                           |
| Metaheuristic | GA, ACO, SA, VNS                                 |
| Matheuristic  | Hybrid exact + heuristic                         |
| Hybrid        | Combination of multiple techniques               |

**Examples**

Genetic algorithm solving VRPTW

→ `Metaheuristic`

---

## Algorithms

**Description**
Specific algorithm(s) used.

**Examples**

| Algorithm                             | Example Entry |
| ------------------------------------- | ------------- |
| Genetic algorithm                     | `GA`          |
| Ant colony optimization               | `ACO`         |
| Tabu search                           | `TS`          |
| Variable neighborhood search          | `VNS`         |
| Reinforcement learning routing policy | `RL policy`   |

**Example**
Paper combining GA and local search

→ `GA + Local Search`

---

## AI / Learning Component

**Description**
Whether the system includes **machine learning or AI methods**.

**Categories**

| Type                   | Examples                    |
| ---------------------- | --------------------------- |
| None                   | Classical optimization only |
| Machine Learning       | Supervised learning         |
| Reinforcement Learning | Policy learning             |
| Deep Learning          | Neural networks             |
| Fuzzy Logic            | Fuzzy decision systems      |
| Knowledge-based        | Rule-based systems          |

**Example**

Paper uses neural networks to predict demand

→ `Deep Learning`

---

## Hybridization Type

**Description**
How different techniques are combined.

**Examples**

| Hybridization        | Description               |
| -------------------- | ------------------------- |
| ML + Metaheuristic   | ML guides search          |
| Exact + Heuristic    | Matheuristic              |
| Rules + Optimization | Knowledge-based routing   |
| ML + Simulation      | Learning-based simulation |

**Example**

Reinforcement learning used to guide tabu search

→ `RL + Tabu Search`

---

# Human–AI Interaction

## Human Involvement

**Description**
Type of knowledge or input provided by humans.

**Common categories**

| Type                   | Meaning                          |
| ---------------------- | -------------------------------- |
| Preference input       | Decision maker sets weights      |
| Expert rules           | Domain rules encoded             |
| Interactive evaluation | Human evaluates solutions        |
| Parameter tuning       | Human adjusts parameters         |
| Feedback learning      | Human feedback used for learning |
| None                   | Fully automated system           |

**Example**

User sets priority for urgent deliveries

→ `Preference input`

---

## Interaction Stage

**Description**
At which stage of the optimization process the human interacts.

**Categories**

| Stage               | Meaning                       |
| ------------------- | ----------------------------- |
| Problem formulation | Define constraints/objectives |
| During optimization | Interactive search            |
| Solution selection  | Human selects solution        |
| Post-analysis       | Evaluation after optimization |

**Example**

Planner chooses a route among Pareto solutions

→ `Solution selection`

---

# Decision Support Characteristics

## Decision Support Aspect

**Description**
Indicates whether the paper explicitly supports **human decision making**, rather than only computing an optimal solution.

**Values**

* `Yes`
* `No`

**Example**

System generates multiple routing alternatives for planners

→ `Yes`

---

## Objectives

**Description**
Optimization objectives considered.

**Common objectives**

| Objective     | Meaning                        |
| ------------- | ------------------------------ |
| Distance      | Minimize travel distance       |
| Cost          | Minimize operational cost      |
| Time          | Minimize delivery time         |
| Service level | Maximize customer satisfaction |
| Emissions     | Reduce environmental impact    |

**Example**

Minimize travel cost and service delay

→ `Cost + Time`

---

# Evaluation and Results

## Evaluation Setting

**Description**
Environment where the algorithm was evaluated.

**Categories**

| Setting         | Description               |
| --------------- | ------------------------- |
| Simulation      | Computational experiments |
| Case study      | Real company scenario     |
| Real deployment | Implemented in operations |

**Example**

Paper tested on synthetic logistics simulation

→ `Simulation`

---

## Key Contribution

**Description**
Short summary of the **main contribution of the paper**.

**Examples**

* "Reinforcement learning policy for dynamic VRP"
* "Interactive multiobjective routing framework"
* "Preference-based route optimization model"

**Notes**
Write **one concise sentence**.

---

# System Characteristics

## Decision Support System

**Description**
Indicates whether the work proposes a **full decision-support system (DSS)** rather than only an algorithm.

**Values**

* `Yes`
* `No`

**Example**

Paper describes a routing interface used by planners

→ `Yes`

---

## Level of Automation

**Description**
Degree of autonomy of the system.

**Categories**

| Level           | Meaning                      |
| --------------- | ---------------------------- |
| Fully automated | No human interaction         |
| Human-guided    | Human provides inputs        |
| Interactive     | Continuous human interaction |

**Example**

Planner adjusts preferences during optimization

→ `Interactive`

---

# Evaluation Measures

## Evaluation Metrics

**Description**
Metrics used to evaluate performance.

**Examples**

| Metric           | Meaning               |
| ---------------- | --------------------- |
| Total distance   | Routing efficiency    |
| Computation time | Algorithm speed       |
| Optimality gap   | Distance from optimal |
| Service level    | Delivery reliability  |

**Example**

Distance reduction and runtime

→ `Distance, runtime`

---

# Screening Fields

## Relevance to Review

**Description**
Indicates how relevant the paper is for the research question.

**Categories**

| Level  | Meaning                                          |
| ------ | ------------------------------------------------ |
| High   | Directly studies hybrid human–AI VRP             |
| Medium | Related but indirect                             |
| Low    | Mostly algorithmic with little human involvement |

---

## Notes

**Description**
Free text observations made during screening.

**Examples**

* "Includes interactive visualization tool"
* "Human preferences modeled via fuzzy weights"
* "Mostly algorithmic, minimal decision support"

---

# Example of a Completed Entry

| Field                   | Example                                    |
| ----------------------- | ------------------------------------------ |
| DOI                     | 10.1016/j.cor.2021.105312                  |
| Authors                 | Chen et al.                                |
| Year                    | 2021                                       |
| Title                   | Interactive multiobjective vehicle routing |
| Venue                   | Computers & Operations Research            |
| VRP Variant             | VRPTW                                      |
| Application Context     | Urban delivery                             |
| Data Type               | Benchmark                                  |
| Optimization Approach   | Metaheuristic                              |
| Algorithms              | NSGA-II                                    |
| AI / Learning Component | None                                       |
| Hybridization Type      | Multiobjective + preference model          |
| Human Involvement       | Preference input                           |
| Interaction Stage       | Solution selection                         |
| Decision Support Aspect | Yes                                        |
| Objectives              | Cost + time                                |
| Evaluation Setting      | Simulation                                 |
| Key Contribution        | Interactive routing framework              |
| Decision Support System | Yes                                        |
| Level of Automation     | Human-guided                               |
| Evaluation Metrics      | Distance, runtime                          |
| Relevance to Review     | High                                       |
| Notes                   | Uses Pareto solution visualization         |

