Cross-hedge project: castor meal hedged with NCDEX castor seed futures	
	
Asset A (spot exposure)	Castor meal: SEA daily quote "Castormeal Ext (FOR) (Bulk) (Ex-Kandla)", Rs per metric tonne
Asset B (hedge instrument)	NCDEX Castor Seed futures, symbol CASTOR, basis Deesa, Rs per quintal
Why A has no own futures	No castor meal contract appears on NCDEX (all symbols checked in 733 daily exchange files). Castor oil was rejected because NCDEX lists CASTOROIL.
Economic link	Crushing castor seed yields castor oil and castor meal (joint products), so meal prices depend on seed prices.
Study window	3 Oct 2023 to 22 Sep 2026 (2.97 years). Hedge horizon: one NCDEX trading day.
	
SHEET GUIDE	
1_Sources	Every data source with URL, access method, unit and primary/secondary status
2_A_Raw	All 639 SEA posts in the window with the castor meal cell exactly as published, and the status given to each
3_A_Clean	The 539 castor meal quotes used after cleaning
4_B_Contracts	Every CASTOR contract-day row from the official NCDEX files (no continuous series)
5_B_Inventory	One row per CASTOR contract: dates, observations, volume and open interest
6_Roll_Schedule	The 36 roll dates under the fixed T-10 rule, with old/new contract prices and the roll gap
7_B_Returns	Return-consistent futures series: each daily return uses a single contract (live formulas)
8_Aligned	The 491 matched one-day returns for A and B, plus hedged-portfolio returns (live formulas)
9_Hedge_Model	Hedge ratio, regression statistics and hedge effectiveness, all as live Excel formulas
10_Verification	Independent checks against live SEA pages, raw NCDEX files and a Python recomputation
11_Data_Quality_Log	Every excluded or missing observation and why
12_Candidate_Screening	All pairs tested before this one and why they were rejected
	
	
Method in one line	Daily log returns; OLS of A on B in-sample gives h*; the same h* is applied unchanged out-of-sample; effectiveness = 1 - Var(hedged)/Var(unhedged).
