![http://quantnet.wiwi.hu-berlin.de/style/banner.png](http://quantnet.wiwi.hu-berlin.de/style/banner.png)

# <img src="pictures/githublogo.png" width="120" /> **Styleguide of QuantLets** ![qlogo](pictures/qloqo.png)


The following pages will introduce the Styleguide of QuantLets. An overview 
of the structure of a QuantLet is given and explaining each part's relevance.
You will find descriptions and instructions on how to format your 
code as well as detailed examples about the required information 
around your QuantLet. 

In the second section you will find basic instructions on how to work with the desktop client version of Github, which includes additional features to upload pictures and datafiles as separate files.

Finally, several illustrative examples of correct QuantLets
are listed in the Appendix.

## 1. Structure of a QuantLet Repository on Github

Every QuantLet Repository consists of two elementary parts / files with equal relevance:
* __Metainfo.txt:__ Contains Meta-Information about the functionality,
origin and purpose. Furthermore, a list of keywords and references
to other related QuantLets are stated. You will need to create the file 
"metainfo.txt", which will be formatted in 'YAML', an easy and intuitive
data serialization language. The formatted "metainfo.txt" will be used for 
[Visualization] (http://quantnet.wiwi.hu-berlin.de/d3/ia/) and
data mining practices (e.g. Clustering, filtering and recommendation engines) 
and is therefore mandatory. In the next sections,
you will find examples on how to format the "metainfo.txt".
Here you can download the prepared TEMPLATE of a "metainfo.txt":
[TEMPLATE_Metainfo.txt] (https://github.com/QuantLet/Validation-procedure-and-Styleguide/blob/master/TEMPLATE_Metainfo.txt)

* __QuantLetcode.r:__ Your code doesn't need the commented meta information as header any more,
once you have provided a complete "metainfo.txt" as explained before.
Next, a correctly working code represents the second
elementary part. The described functionality in the metainfo should
practically be realizable by using the provided code. Besides correct 
functionality the code needs to be formatted according to the provided 
styleguide. Formatting ensures human readability while comprehensibility is 
ensured by sufficient comments.

### 1.1. Metainfo.txt
#### Required and optional Meta-Information

1. __Name of QuantLet__ : e.g. SFEDAXlogreturns (Omit endings like .r .sas or .m)
2. __Published in__ : Book / Paper
3. __Description__ : at least 10 words; should begin with a verb and with capital letters, e.g.
"Plots the time series ..."
4. __Keywords__ : at least 5 words (the more the merrier) from the [keyword list](http://quantnet.wiwi.hu-berlin.de/index.php?p=searchResults&w=allkeywords&sort=f) only
4. __See also (optional)__ : mention related QuantLets
5. __Author__ : check for existing authors on the [website](http://quantnet.hu-berlin.de/) [if new, then write [New]
in this field]
6. __Submitted (optional)__ : state your name and the time of submission
7. __Datafile__ : check whether all datafiles which are used in the code are listed here
8. ___Input (optional)___ : Should contain some new info, which is not written 
in other meta-info fields
9. ___Output (optional)___ : Should contain some new info, which is not written
in other meta-info fields
10. __Example (optional)__  : Should contain a list of generated plots and description, which is not written in other meta-info fields

Make sure that the provided 'Name of QuantLet' and the actual filename of your provided Codefile is identical.


#### We use 'YAML' to format metainfo.txt to make things easy and fast
YAML™ (rhymes with “camel”) is a human-friendly, cross language data serialization language. You will use it almost intuitively. Thanks to 'YAML', there is no need to use the #-Symbol in the metainfo.txt anymore. It is even robust against redundant space in description parts although we advise to avoid these. Besides that, there are alternative ways on how to structure enumerations in a YAML-File.

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

- The colon ' : ' separates the data field (left) from its description (right)

- _Optional_ data fields, where no description is provided can be omitted completely (Above example includes them for illustration purposes anyway). 

- If you write multiple lines or use special characters you have to put your text in single quotes  ' '. For single lines without special characters there is no need to do so. 
```R
...
Description:       'Shows monthly returns of six US firms
                    from Jan 2000 to Dec 2009.'
...
```

#### Alternative ways of enumerations in metainfo.txt
As mentioned above, there are different ways you can structure enumerations in 'YAML'.
Below you find the two possible alternatives:
```yaml
...
Keywords:          financial, portfolio, returns, asset, time-series, plot
...
Keywords:          
- financial
- portfolio
- returns
- asset
- time-series
- plot

```

For further details please check the complete [YAML documentation](http://www.yaml.org/spec/1.2/spec.html).

### 1.2. Code

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
## 2. Github Desktop Client - Basic instructions
Besides the browser version of Github, there is also a desktop client for local use. Github desktop client is an easy to use graphical user interface for those who are not comfortable with Git (Commandline version). The desktop client allows to upload pictures and datafiles as separate files, which will be necessary if plots are generated by your code or whenever a dataset is required. However, you will need to understand some basics to avoid common errors.
To find an appropriate client version for your operating system click [here](http://git-scm.com/download/gui/linux)

#### 2.1. How to clone repositories to your local pc
Before you can locally work on your desired repository you need to 'clone' it first. This will create a local copy of the masterbranch on your local workspace. It now becomes critical to keep your local branch synced to any changes conducted to the remote master branch and vice versa. If you don't, you will encounter syncing errors due to differences between your local and the remote branch. We will now describe how to avoid this common error.

#### 2.2. Avoiding Sync-Errors

1) _Local synchronization_ - Sync your local repository before beginning any work in that repository

2) _Conduct local changes_ - Change/ add/ delete files

3) _Commit_                - Commit your conducted changes within your Github Desktop Client

4) _Back synchronization_  - Sync your local repository, so that changes are inherited in remote branch

#### 2.3. Resolving Sync-Errors
It might happen that you forget to synchronize your repository as prescribed which could lead to Sync-errors. If that has happened to you, you will have to work with the Gitshell commandline to solve this error.
Following articles might help you with that:
- [Git Documentation-Getting started](https://git-scm.com/videos)
- [Dealing with non-fast-forward errors] (https://help.github.com/articles/dealing-with-non-fast-forward-errors/)

#### 2.4. Upload pictures and datafiles as separate files
You can easily add files to your local repositories which will be commited and therefore uploaded to the remote branch. Simply add pictures or datafiles to the desired local repository. If you have not specified a special directory upfront, the directory will most likely be C:\Users\Username\Documents\GitHub\Repository_xy.

## 3. Final Check
1. Check if your code runs properly and complies to the style requirements
2. Check if MetaInfo is complete and that you have sufficient keywords from the [keyword list](http://quantnet.wiwi.hu-berlin.de/index.php?p=searchResults&w=allkeywords&sort=f) 

## 4. Appendix
Example's of correctly formatted QuantLets with all required meta-information:
Pick out any of the "bubbles" in this [Visualization] (http://quantnet.wiwi.hu-berlin.de/d3/ia/),
then click on it and examine the files in the shown GitHub-folder. In particular the related "metainfo.txt".

Some Examples:

1. [MVAsirdata ] (https://github.com/QuantLet/Ready/blob/master/QID-1234-MVAsirdata/Metainfo.txt)
2. [MMSTATconfi_pi] (https://github.com/QuantLet/MMSTAT/blob/master/MMSTATconfi_pi/Metainfo.txt)
3. [MTS_expinf] (https://github.com/QuantLet/MTS/blob/master/MTS_expinf/Metainfo.txt)
