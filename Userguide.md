# Styleguide of Quantlets

The following pages will introduce the Styleguide of Quantlets. 
You will find descriptions and instructions on how to format your 
code as well as detailed examples about the required information 
in the header of your Quantlet.

## Structure of Quantlets

Every Quantlet consists of two elementary parts with equal relevance:
* __Header-Section:__ Contains Meta-Information about the functionality,
origin and purpose. Furthermore, a list of keywords and references
to other related Quantlets are stated.  The relevance of the header lies
in its functionality as an information source for all suceeding data mining
activities (e.g. Clustering, filtering and recomandation engines). 
Because clustering is an integral part of QuantNet the provision of sufficient meta-information is
mandatory.

* __Code-Section:__ A correct working code represents the second
elemantary part. The described functionality in the metainfo should
practically be realised by using the provided code. Besides correct 
functionality the code needs to be formatted according to the provided 
styleguide. Formatting ensures readability while comprehensibility is 
ensured by sufficient comments.

### Header
#### Required Meta-Information
1. Name of Quantlet (e.g. SFEDAXlogreturns)
2. Published in Book / Paper
3. Description - at least 10 words should begin the verb and with the capital, e.g.
"Plots the time series ..."
4. See also - list related Quantlets
5. Author - check at the list of authors on the website [if new, than write [New]
in this field]
6. Datafile
7. Input (optional) - Should contain some new info, which is not written 
in other meta-info fields
8. Output (optional) - Should contain some new info, which is not written
in other meta-info fields
9. Example - check whether there is appropriate info on the website.
Should contain some new info, which is not written in other meta-info fields

#### Example of complete and correct header
```
# ------------------------------------------------------  
# Name of QuantLet:  
# ------------------------------------------------------  
# Published in:  
# ------------------------------------------------------  
# Description:  
# ------------------------------------------------------  
# Keywords:  
# ------------------------------------------------------  
# See also:  
# ------------------------------------------------------  
# Author:  
# ------------------------------------------------------  
# Submitted:  
# ------------------------------------------------------  
# Datafile:  
# ------------------------------------------------------  
# Input:  
# ------------------------------------------------------  
# Output:  
# ------------------------------------------------------  
# Example:  
# ------------------------------------------------------  
```
### Code

#### Use "FormatR package" to clean up your code  
You can easily preprocess your code with the FormatR package. In the
following you will find instructions on how to execute the relevant
function.

----------------------------------------------------------  
```
# Cleaning up the source code in an R script file "input.R",  
# Indentation is set to two space characters and maximum line width is 80 characters.
# The formatted code will be written into the new script file "output.R"

tidy_source(source = "input.R", indent = 2, width.cutoff = 80, file = "output.R")

# similar to the previous example, but using the clipboard instead of an input file

tidy_source(indent = 2, width.cutoff = 80, file = "output.R")

# when omitting function parameters the defaults
# indent = 4 and width. cutoff = 80 are being used.
# For simplicity, we recommend these for the use on QuantNet

tidy_source(file = "output.R")
```
More details about the package FormatR are available in the [package documentation](https://cran.r-project.org/web/packages/formatR/index.html)


#### Style requirements
1. indentation
2. ....

## Final Check
1. x
2. y

## Appendix

