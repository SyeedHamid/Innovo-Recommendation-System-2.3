
### Subcritical-Safe Extraction Recommendation Engine


This project implements a safety-aware, yield-maximizing recommendation engine for plant compound extraction. It enforces subcritical pressure-temperature constraints using NIST saturation data and selects optimal set-points using machine learning.

**Features**

**- Subcritical Safety Enforcement:** Classifies extraction configurations as SAFE, WARNING, or DANGEROUS using saturation pressure logic.

**- Yield Prediction (Model 2.2):** Trains an XGBoost regression model on empirical plant data to predict extraction yield.

**- Set-Point Recommendation (Model 2.3):** Performs grid search to find higher-yielding subcritical-safe overrides.

**- Stakeholder-Readable Reporting:** Outputs time, temperature, pressure, pH, yield, safety status, and diagnostics in clear, audit-ready format.

**- Final Recommendation Across Plants:** Selects the highest-yielding subcritical-safe configuration across all inputs.





Sample Output

================================================================================
🌿 Recommended Extraction Parameters — Glycyrrhiza_Glabra
================================================================================

🌟 Best Yield Parameters (Subcritical-Safe):
- Time min: 5.0
- Temperature c: 145.16
- Pressure bar abs: 19.7
- Ph neutral est: 5.75
- Yield: 14.12

Safety Status: ⚠️ Warning

Why Flagged:
The pressure of 19.70 bar exceeds the subcritical assurance threshold at 145.16 °C.
Threshold: ~8.49 bar (150% of saturation pressure)
Details: 19.70 > 8.49

Suggested Resolution:
Reduce pressure below threshold or confirm vessel integrity for high-pressure operation.

================================================================================
🌿 Recommended Extraction Parameters — Ellagic_Acid_Peel
================================================================================

🌟 Best Yield Parameters (Subcritical-Safe):
- Time min: 18.0
- Temperature c: 130.144
- Pressure bar abs: 9.441
- Ph neutral est: 5.94
- Yield: 4.64

Safety Status: ⚠️ Warning

Why Flagged:
The pressure of 9.44 bar exceeds the subcritical assurance threshold at 130.14 °C.
Threshold: ~6.30 bar (150% of saturation pressure)
Details: 9.44 > 6.30

Suggested Resolution:
Reduce pressure below threshold or confirm vessel integrity for high-pressure operation.

================================================================================
🏆 Final Recommendation: Highest-Yielding Subcritical-Safe Configuration
================================================================================

Top Performer: Glycyrrhiza_Glabra
Yield: 14.12%
Safety Status: ⚠️ Warning
Pressure of 19.70 bar exceeds subcritical assurance threshold at 145.16 °C.
Threshold: ~8.49 bar (150% of saturation pressure)
Proceed only if vessel integrity is validated or pressure is reduced.
