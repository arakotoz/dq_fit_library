## DQ fit library
This class can be used to fit invariant mass distributions (signal + backgorund). To run it is necessary **ROOT6**. 
The class contains:
* class files: **DQFitter.cxx** and **DQFitter.h**
* function library: **FunctionLibrary.C**
* test macro: **run_test_fit.C**

The test fit code performs a simple fit of a gaussian signal and a pol0 / expo background

In the root environment run with:
* **.x DQFitter.cxx+**
* **.x run_test_fit.C++**

An AnalysisResults.root file will be produced containing:
* the canvas fit the histogram and the fitting functions
* the canvas with the ratio Data / Fit
* the canvas with the residuals (data - background after fit)
* the histogram with the X2 / NDF, the number of signal events and the parameters of interest (POI)

The class can use also the RooFit library. In this case the used has to create a class following the example of GausPdf.cxx.
At this point the PDF can be added to the class and used for the fit.

## QC macro
This macro can be used to produce control plots reading the O2 DQ tableMaker and tableReader.In addition it extracts basic J/psi
basic features (mass position and width) using the DQ fit library

In the root environment run with:
* **.x DQFitter.cxx+**
* **.x run_qc.C++**
