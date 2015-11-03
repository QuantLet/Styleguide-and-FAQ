# Styleguide of Quantlets

The following pages will introduce the Styleguide of Quantlets. An overview 
of the structure of a Quantlet is given and explaining each part's relevance.
You will find descriptions and instructions on how to format your 
code as well as detailed examples about the required information 
around your Quantlet. Several illustrative examples of correct Quantlets
are listed in the Appendix.

## Structure of a Quantlet Repository on Github

Every Quantlet Repository consists of two elementary parts / files with equal relevance:
* __Metainfo.txt:__ Contains Meta-Information about the functionality,
origin and purpose. Furthermore, a list of keywords and references
to other related Quantlets are stated. You will need to create the file 
"metainfo.txt", which will be formatted in 'YAML', an easy and intuitive
data serialization language. The formatted "metainfo.txt" will be used for 
[Visualization] (http://quantnet.wiwi.hu-berlin.de/d3/ia/) and
data mining practices (e.g. Clustering, filtering and recommendation engines) 
and is therefore mandatory. In the next sections,
you will find examples on how to format the "metainfo.txt".
Here you can download the prepared TEMPLATE of a "metainfo.txt":
[TEMPLATE_Metainfo.txt] (https://github.com/QuantLet/Validation-procedure-and-Styleguide/blob/master/TEMPLATE_Metainfo.txt)

* __Quantletcode.r:__ Your code doesn't need the commented meta information as header any more,
once you have provided a complete "metainfo.txt" as explained before.
Next, a correctly working code represents the second
elementary part. The described functionality in the metainfo should
practically be realizable by using the provided code. Besides correct 
functionality the code needs to be formatted according to the provided 
style guide. Formatting ensures human readability while comprehensibility is 
ensured by sufficient comments.

### Metainfo.txt
#### Required Meta-Information
1. __Name of Quantlet__ (e.g. SFEDAXlogreturns)
2. __Published in__ Book / Paper
3. __Description__ - at least 10 words; should begin with a verb and with capital letters, e.g.
"Plots the time series ..."
4. __Keywords__ - at least 5 words (the more the merrier) from the [keyword list](http://quantnet.wiwi.hu-berlin.de/index.php?p=searchResults&w=allkeywords&sort=f) only
4. __See also__ - mention related Quantlets
5. __Author__ - check for existing authors on the [website](http://quantnet.hu-berlin.de/) [if new, than write [New]
in this field]
6. __Submitted__ - state your name and the time of submission
7. __Datafile__ - check whether all datafiles which are used in the code are listed here
8. ___Input (optional)___ - Should contain some new info, which is not written 
in other meta-info fields
9. ___Output (optional)___ - Should contain some new info, which is not written
in other meta-info fields
10. __Example__ - check whether there is appropriate info on the website.
Should contain some new info, which is not written in other meta-info fields

#### We use 'YAML' to format metainfo.txt to make things easy and fast
YAML™ (rhymes with “camel”) is a human-friendly, cross language data serialization language. You will use it almost intuitively. 

#### Example of complete and correct "metainfo.txt" in YAML format
```yaml
 
Name of QuantLet:  MVAreturns
 
Published in:      Applied Multivariate Statistical Analysis
  
Description:       Shows monthly returns of six US firms from Jan 2000 to Dec 2009.
 
Keywords:          financial, portfolio, returns, asset, time-series, plot

See also:          MVAportfol_IBM_Ford, MVAportfol_IBM_PanAm

Author:            Zografia Anastasiadou
  
Submitted:         Fri, August 05 2011 by Awdesch Melzer
  
Datafile:          apple.csv, bac.csv, ed.csv, ford.csv, ibm.csv, ms.csv
  
Input:  
  
Output:  
  
Example:  
  
```
You will only need to know two basic elements:

- If you write multiple lines you have to put your text in ' '
```R
...
Description:       'Shows monthly returns of six US firms
                    from Jan 2000 to Dec 2009.'
...
```

- YAML prohibits the use of special german characters like "ä, ö, ü".

You can check the complete [YAML documentation](http://www.yaml.org/spec/1.2/spec.html).

### Code

#### Use "FormatR package" to clean up your R code (In the case you are using another language like Matlab try to implement the following steps accordingly) 
You can easily preprocess your code with the FormatR package. This will
do 80% of the work for you. In the following you will find instructions on how to execute the relevant
function.

----------------------------------------------------------  
```R
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
More details about the package FormatR are available in the [package documentation](https://cran.r-project.org/web/packages/formatR/index.html).

#### Style requirements
* __Change all "<-" with "="__

A QuantNet specific style requirement adresses the assignment operator. 
All "<-" should be replaced with "=" like shown below.
```R
# BAD
foo <- 5.0
bar <- function(x) 
    return x^2
}

# GOOD
foo = 5.0
bar = function(x){
    return x^2
}
```

* __Align assignments in subsequent lines by "="__

```R
foo     = 5.0
foobar  = 7.0
bar     = 8.0
```

* __Set four space characters for indentation (_this
should be done automatically by formatR_)__

```R
while (i<n){
    i = i + 1
}
```

## Final Check
1. Check if your code runs properly and complies to the style requirements
2. Check if MetaInfo is complete and that you have sufficient keywords from the [keyword list](http://quantnet.wiwi.hu-berlin.de/index.php?p=searchResults&w=allkeywords&sort=f) 

## Appendix
Example's of correctly formatted Quantlets with all required meta-information:
Pick out any of the "bubbles" in this [Visualization] (http://quantnet.wiwi.hu-berlin.de/d3/ia/),
then click on it and examine the files in the shown GitHub-folder. In particular the related "metainfo.txt"

Some Examples:

1. [MVAsirdata ] (https://github.com/QuantLet/Ready/blob/master/QID-1234-MVAsirdata/Metainfo.txt)
2. [MMSTATconfi_pi] (https://github.com/QuantLet/MMSTAT/blob/master/MMSTATconfi_pi/Metainfo.txt)
3. [MTS_expinf] (https://github.com/QuantLet/MTS/blob/master/MTS_expinf/Metainfo.txt)
