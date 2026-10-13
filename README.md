# GSD

Sanctions designation lists are maintained by dozens of jurisdictions — OFAC, the EU, the UN Security Council, and others — each with independent update cycles, entity formats, and coverage priorities. Cross-referencing these lists at scale is operationally expensive for compliance teams, and the absence of a unified analytical layer makes systematic pattern detection across regimes difficult for researchers and policy analysts alike.

This project builds a basic sanctions intelligence pipeline on top of OpenSanctions, a consolidated open-source repository of global sanctions and politically exposed persons (PEPs) data. The pipeline ingests and combines multiple datasets, enriches records through complementary data joins — adding sanctioned maritime vessels and financial securities — and validates data quality before analysis is run.

Three analytical techniques are applied: a market-basket model using the A-Priori algorithm to identify frequent co-occurrence patterns in entity attributes; a recommendation system based on UV decomposition via SGD to detect cross-list coverage gaps; and a binary classifier to assess whether a PEP profile is statistically consistent with sanctions designation. Findings are exposed through an interactive Quarto dashboard rendering this notebook.

The intended use cases are AML/CFT compliance screening, defense-sector entity monitoring, and geopolitical risk analysis.
