corrplot2
=========

Extended functionality to the original "corrplot" function from the corrplot package in R.

Installation:
Open an R window and paste this line:
source("")


DESCRIPTION
1.
The original function allows to show coefficients, but has no way of setting up font size and font color.
Only two parameters are available: addCoef.col="black" and addCoefasPercent=T
The following parameters are added (with respective defaults):
addCoef.cex = 0.8 # font size of coeffficients
addCoef.font = 2 # font type 1=plain, 2=bold, 3=italic, 4=bold italic, 5=symbol
addCoef.labels = "all" # which cell to add coefficients, "all", "significant", "insignificant"
addCoef.outline = NULL # outline color of the text, i.e. "white", "red"; helps distinguish text from background of different colors

2.
The original function allows to plot confidence intervals as "circle" or "square". However the plot shows no indication
of the correlation value, only the confidence interval. Ironically, cells with high correlation and narrow confidence
intervals (eg. the best correlations) appeared as empty cells, while cells with large confidence inervals (less significant) appeared fuller. The first look of the plot gave the false impression that the less significant correlations were the most
prominent ones.
The updated function keeps the original options but adds to variants: plotCI="fullsquare" and plotCI="fullcircle".
These options produce three levels of squares/circles, the inner is the lower CI, the middle is the correlation value, the the upper is the highest CI. This way the most significant corre3lations do not loose their visual impact.



There are unanswered questions in the web regarding this issue:

The new function 
