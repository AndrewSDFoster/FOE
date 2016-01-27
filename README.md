Initialization Function (should run with any one or more of eclipses, transits
and rv):

 Inputs:
  TEP file (required)
  ETD transits
  results.txt
  RV from papers
  RV from Gaspar
  generic formats

 It checks if it needs to run, then converts these into TWO MCcubed
 initialization functions, one for period only, one for a full fit

 Makes output file including the following calculations:
 light time corrections

Period only run (should run even if no RV data):
 only uses transits and eclipses to fit the period, ephemeris, and eclipse midpoint phase
 which it will then use to also calculate ecosw
 use fft to calculate quick period from RV data

Full run
 Fits both: 
  an eccentric sinusoid to the RV data
  the period model
  
 After, it calculates the largest possible false esinw signal from stellar
 tides in the RV data

IF TIME:
 fix MCCubed to include parameter namnes and whether or not a parameter is a
 "nuisance" parameter.
