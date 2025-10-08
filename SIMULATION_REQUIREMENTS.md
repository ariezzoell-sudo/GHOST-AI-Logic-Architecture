# SIMULATION & VALIDATION REQUIREMENTS

To ensure the integrity of G-HOST AI, all proposals for architectural or calibration changes must be supported by evidence.

### 1. Evidence for Weight Changes ($\mathbf{W_n}$)
If proposing changes to W1, W2, or W3, the simulation must show the following results on historical flight data networks:
* **Increased Network Stability:** A decrease in the average time deviation percentage (**Variance Penalty/VP**) on the 10% worst-impacted flights.
* **Harmony Logic Correlation:** Evidence that the CR and DM scores are not disproportionately sacrificed.

### 2. Input Data Requirements
Validation must use a data set that includes critical variables:
* Real-time Runway Capacity (To test CR).
* Actual Fuel Cost Data (To test DM).
* Local Cancellation or Delay Data (To test STA N-Agent resilience).

### 3. Success Metrics
Simulations must clearly demonstrate that the new *outcome* has a **higher Harmony Score (S)** than the existing *baseline*.
