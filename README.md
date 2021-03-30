# Performance_Measures

Files required to run the analysis:
-	data.RData: the pseudo dataset
-	00_Functions.R: all the functions needed to run the analyses
-	01_Fit_PEM_MVN.R: the main file for conducting semi-competing risks analysis under the PEM-MVN model using “SemiCompRisks” package
-	02_Cumulative_Excess_Ratio.R: the main file for the Bayesian estimation of cumulative excess readmission/mortality ratios
-	03_Loss_Function_Based_Profiling.R: the main file for loss-function based joint profiling
-	RASCRF_PM_SM.so: the shared object file for calling core functions written in C from the R script “02_Cumulative_Excess_Ratio.R”
-	PEL_biv.so: the shared object file for calling core functions written in C from the R script “03_Loss_Function_Based_Profiling.R”


Files for the analysis results:
-	Output_Fit_PEM_MVN: the folder containing the output files from the semi-competing risks analysis under the PEM-MVN model
-	theta1.RData: the results file from the Bayesian estimation of cumulative excess readmission ratios
-	theta2.RData: the results file from the Bayesian estimation of cumulative excess mortality ratios
-	L01.R.RData: the results file containing the hospitals identified as the top 10% for performance with respect with 90-day readmission
-	L01.D.RData: the results file containing the hospitals identified as the top 10% for performance with respect with 90-day mortality

The R libraries needed are: 
-	SemiCompRisks, version >3.3, depends on  (R ≥ 3.3.0)
-	gaussquad, version 2.0.1, depends on (R≥ 2.0.1)

Instruction:
-	We provide the three separate master R scripts (01_Fit_PEM_MVN.R, 02_Cumulative_Excess_Ratio.R, 03_Loss_Function_Based_Profiling.R) along with the corresponding output files. Therefore, it is not necessary for users to run all three scripts in turn to get the final profiling results. For example, one can directly calculate cumulative excess readmission and mortality ratios (02_Cumulative_Excess_Ratio.R) by loading the files in the Output_Fit_PEM_MVN folder and skip the semi-competing risks analysis (01_Fit_PEM_MVN.R).


