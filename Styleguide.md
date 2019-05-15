
[<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/banner.png" width="880" alt="Visit QuantNet">](http://quantlet.de/index.php?p=info)

# <img src="pictures/githublogo.png" width="120" /> **Styleguide of QuantLets** [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/)[<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/d3/ia)


The following pages will introduce the Styleguide of Quantlets (Qs). An overview of the structure of a Q is given while explaining each part's relevance.
You will find descriptions and instructions on how to format your code as well as detailed examples about the required information for your Q. 

In the second section you will find basic instructions on how to work with the desktop client version of Github, which includes additional features to upload pictures and datafiles as separate files to your Q's repository.

Finally, several illustrative examples of correct Quantlets are listed in the Appendix.

## 1. Structure of a Quantlet folder in a Github repository (see also __Guideline II__ in [README](README.md))

Every Quantlet folder consists of two elementary parts / files with equal relevance:
* __Metainfo.txt:__ Contains meta-information about the functionality, origin and purpose of your Q. Furthermore, lists of keywords and references to other related Quantlets are stated. You will need to create the file "metainfo.txt", which will be formatted in 'YAML' - an easy and intuitive
data serialization language. The formatted "metainfo.txt" will be used for [Visualization] (http://www.quantlet.de) and data mining practices (e.g. clustering, filtering and recommendation engines) and is therefore __mandatory__.
In the next sections, you will find examples on how to format the "metainfo.txt". Here, You can download the prepared [TEMPLATE_Metainfo.txt] (TEMPLATE_Metainfo.txt)

* __Quantletcode:__ A correctly working code represents the second elementary part. The described functionality in the metainfo.txt should practically be realizable by using the provided code. Besides correct functionality the code needs to be formatted according to the here provided styleguide.
Formatting ensures human readability while comprehensibility is ensured by sufficient and precise comments.

### 1.1. Metainfo.txt
#### Required and optional Meta-Information

1. __Name of Quantlet__ : e.g. SFEDAXlogreturns (Omit endings like .r .m .sas or .py)
2. __Published in__ : Book / Paper / other Place of publication
3. __Description__ : at least 10 words; should begin with a verb and with capital letters, e.g. "Plots the time series ..."
4. __Keywords__ : at least 5 words (the more the merrier), please use the [yamldebugger](https://github.com/lborke/yamldebugger) for their validation, the more provided keywords are in the Quantlet list the better for the text mining!
5. __Author__ : Name of the Author
6. __See also (optional)__ : mention related Quantlets
7. __Submitted (optional)__ : state the name and the time of the original submission
8. __Datafile (optional)__ : All datafiles used by your code need to be listed here
9. __Input (optional)__ : Should contain some new info, which is not written in other metainfo fields
10. __Output (optional)__ : Should contain some new info, which is not written in other metainfo fields
11. __Example (optional)__  : Should contain a list of generated plots and descriptions, which are not written in other metainfo fields

#### _Important_:  
1. Make sure that the provided 'Name of Quantlet' and the actual filename of your provided Codefile is identical! Otherwise the automatic Readme.md creation will be incomplete.
2. If a Quantlet is written in more than one programming language (i.e. Matlab/SAS), add relevant data fields like Author[Matlab], Author[SAS], Submitted[Matlab], Submitted[SAS], ... to the Metainfo.txt if you want to distinguish between different versions/languages.
3. The first five metainfo fields are necessary, the [yamldebugger](https://github.com/lborke/yamldebugger) explicitely checks them. You can also provide your own metainfo fields in your "metainfo.txt" as long as they are YAML-compliant.


#### We use YAML to format metainfo.txt to make things easy and fast
YAML™ (rhymes with “camel”) is a human-friendly, cross language data serialization language. You will use it almost intuitively. Thanks to YAML, there is no need to use the #-Symbol as in Quantnet 1.0 in the metainfo anymore.
The metainfo and the code parts are now clearly separated. However, an automatic evaluation and aggregation of these elementary parts becomes possible.
It is even robust against redundant space in description parts although we advise to avoid these. Besides that, there are alternative ways on how to structure enumerations in a YAML-File.


#### Example of a complete and correct "metainfo.txt" in YAML format

```yaml
 
Name of Quantlet:  MVAreturns
 
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

#### Three main YAML rules:
1. The colon ' : ' separates the data field (left) from its description (right) and the dash ' - ' enumerates list items. Avoid them in all other cases or apply Rule 2.
2. If you write multiple lines or use special characters (as in Rule 1 or examples below) you have to put your text in single quotes, i.e. 'Your text'. For single lines without special characters there is no need to do so.
3. If you want to use the apostrophe character <'> (represented by the single quote sign) inside your text just type the single quote sign twice.

### It is very important to type the exact apostrophe character <'> as displayed above!! Depending on your keyboard and/or editor some other apostrophe variants can appear. Then you have to correct them manually or via Copy&Paste in order to achieve the version above.

- __Optional__ data fields, where no description is provided, can be omitted completely (Above example includes them for illustration purposes anyway). The automatic Readme.md creation process also skips empty data fields.
- The order of appearance of the data fields is irrelevant. They are treated as an "unordered list". Only their presence and content behind the colon ' : ' is crucial.
- Characters like {_, -, :, ", ...} are meant to be special characters. In case of doubt simply put your text in single quotes (See "Three main YAML rules").

More tips and tricks can be found here: [Complete idiot's introduction to yaml](https://github.com/Animosity/CraftIRC/wiki/Complete-idiot's-introduction-to-yaml)


#### YAML format examples:

---
All subsequent five notations are accepted by YAML. We recomend to use such notations which display the text in the best human readable way, because the metainfo text is used later for the Readme file creation (this process is executed in an automatic way).

```yaml

Description:       Shows monthly returns of six US firms from Jan 2000 to Dec 2009.

Description:       'Shows monthly returns of six US firms from Jan 2000 to Dec 2009.'

Description:       'Shows monthly returns of six US firms
                    from Jan 2000 to Dec 2009.'

Description:       'Shows monthly returns of six US firms
from Jan 2000 to Dec 2009.'

Description : 'Shows monthly returns
of six US firms from
Jan 2000 to Dec 2009.'

```

---

For further details please check the complete [YAML documentation](http://www.yaml.org/spec/1.2/spec.html) or find additional information in our [FAQ section](https://github.com/QuantLet/Styleguide-and-FAQ/wiki/03_Questions:-YAML)

## 4. Appendix
Examples of correctly formatted Quantlets with all required meta-information:
Pick out any of the "bubbles" in the [Q Visualization] (http://www.quantlet.de), then click on it and examine the files in the shown GitHub-folder. In particular the related "metainfo.txt".

Some Examples:

1. [MVAsirdata ] (https://github.com/QuantLet/Ready/blob/master/QID-1234-MVAsirdata/Metainfo.txt)
2. [MMSTATconfi_pi] (https://github.com/QuantLet/MMSTAT/blob/master/MMSTATconfi_pi/Metainfo.txt)
3. [MTS_expinf] (https://github.com/QuantLet/MTS/blob/master/MTS_expinf/Metainfo.txt)
