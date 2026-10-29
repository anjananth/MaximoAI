# IBM Bob + IBM Maximo. Hands-On Lab 1171 for TechXchange 2026 

**Audience:** Anyone curious about AI + Maximo.   
**Duration:** 30-45 minutes  
**Format:** Self-guided or facilitated. 
**Guiding rule:** Bob reads and explains first. Nothing changes in Maximo unless you explicitly say so.

---

## Before you start

Make sure Bob is connected to the Maximo MCP server. Ask:

--- ✂️ ---

Are you connected to a Maximo environment? What tools do you have available?

--- ✂️ ---

Bob should list available tools and confirm it can distinguish read-only tools from write tools. If it cannot connect, stop and ask your facilitator.

---

# Exercise 1: Predictive Maintenance Risk Analysis

### Objective

Evaluate Bob's ability to investigate maintenance risk using data from multiple Maximo sources and produce an evidence-based operational assessment.

**Prompt:**

--- ✂️ ---

Let's see if Bob knows Maximo as well as our best Maximo administrator.

Find all overdue PM work orders at site BEDFORD on safety-critical assets where the asset condition score has deteriorated by more than 20% during the last six months, and estimate the associated operational risk.

--- ✂️ ---

### Expected Output

The response should include:

- A list of all matching overdue PM work orders.
- The associated asset for each work order.
- Evidence that the asset is classified as safety-critical.
- Current and historical asset condition information showing the deterioration trend.
- An operational risk assessment for each asset or work order.
- Recommended maintenance actions and prioritization.
- Any assumptions, limitations, or missing data that affected the analysis.

---

# Exercise 2: AppPoints Consumption Report

### Objective

Evaluate Bob’s ability to design a complete Maximo reporting solution, identify the correct data sources, and generate the Automation Script and BIRT report components needed to report user-level AppPoints consumption.

**Prompt:**

--- ✂️ ---

Using Maximo’s Automation Script framework, create a solution that generates a BIRT report showing Maximo users and their respective AppPoints consumption.

Please:

- Determine the appropriate Maximo objects, relationships, and database tables required to identify users and their AppPoints usage.
- Create the Automation Script needed to gather the data.
- Design the BIRT report dataset, query, and report layout.
- Include the following fields where available:
  - User ID
  - Display Name
  - Person ID
  - Security Groups
  - User Status
  - AppPoints Consumed
  - Last Login Date/Time
- Explain any assumptions regarding how AppPoints consumption is calculated or stored in Maximo Application Suite.
- Provide deployment instructions for both the Automation Script and the BIRT report.

If AppPoints consumption is not directly available through standard Maximo objects, identify the alternative data source, API, or MAS component that should be queried instead, and adjust the solution accordingly.

Before generating code, first explain the proposed design, data sources, and architecture.

--- ✂️ ---

### Expected Output

The response should include:

- A proposed solution architecture and data flow.
- The Maximo objects, relationships, and database tables required to retrieve user information.
- The authoritative data source proposed for AppPoints consumption.
- Any required alternative API, MAS component, or integration method.
- The Automation Script needed to gather or prepare the data.
- The BIRT dataset and query design.
- A proposed BIRT report layout containing the requested fields where available.
- Assumptions about how AppPoints consumption is calculated, stored, or retrieved.
- Deployment instructions for the Automation Script and BIRT report.
- Any prerequisites, limitations, unavailable fields, or required configuration.

---

# Exercise 3: Automated Work Order Prioritization and Escalation

### Objective

Evaluate Bob’s ability to design a realistic and maintainable Maximo solution that automatically prioritizes and escalates work orders based on asset criticality, work order status, and elapsed time.

**Prompt:**

--- ✂️ ---

Act as a senior IBM Maximo Application Suite (MAS) 9.x developer specializing in Automation Scripts, Jython, MBO APIs, launch points, and maintenance workflows.

**Objective:** Design and develop an IBM Maximo Automation Script that automatically prioritizes and escalates work orders based on asset criticality, work order status, and elapsed time.

### Business requirements

- When a new work order is created, retrieve the associated asset’s criticality.
- If the asset is highly critical and the work order is corrective maintenance, automatically assign the highest priority.
- If a high-priority work order remains unassigned for more than 4 hours, flag it for supervisor attention.
- If the work order remains unresolved after 24 hours, trigger an escalation.
- Record automated actions in the work order’s work log.
- Prevent duplicate escalation notifications and unnecessary updates.
- Allow supervisors to override automatically assigned priorities.

### Technical requirements

- Target IBM Maximo Application Suite Manage 9.x.
- Use Jython and supported Maximo MBO APIs.
- Recommend the appropriate Object, Attribute, or Action launch points.
- Explain when an Escalation cron task is preferable to an Automation Script launch point.
- Use configurable thresholds rather than hardcoded business rules where practical.
- Handle null values, missing asset information, and unexpected conditions.
- Avoid infinite loops, recursive updates, and unnecessary database queries.
- Do not assume that custom attributes or relationships exist. Identify any required configuration first.
- Use supported Maximo functionality and avoid unsupported APIs.

### Deliverables

- Explain the proposed solution architecture.
- Identify the required launch points and escalation configuration.
- Generate complete, commented Jython Automation Scripts.
- Provide step-by-step implementation instructions in Maximo.
- Explain how to configure notifications and escalation conditions.
- Provide at least five test scenarios, including normal and exception cases.
- Explain how to troubleshoot and validate the solution.

**Important:** Before generating code, identify any assumptions, required Maximo configuration, and potential issues with the proposed design. Clearly separate functionality implemented through Automation Scripts from functionality requiring Maximo Escalations or other configuration.

Make the solution realistic, maintainable, and suitable for a demonstration in a Maximo Manage environment.

--- ✂️ ---

### Expected Output

The response should include:

1. A proposed solution architecture.
2. Any assumptions, prerequisites, and required Maximo configuration.
3. A clear division of responsibilities among Automation Scripts, Maximo Escalations, notifications, and other required configuration.
4. Recommended Object-, Attribute-, or Action-level launch points.
5. The required escalation conditions and scheduling approach。