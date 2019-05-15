
[<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/banner.png" width="880" alt="Visit QuantNet">](http://quantlet.de/index.php?p=info)

# <img src="pictures/githublogo.png" width="120" /> [**Styleguide of QuantLets**](guidelines/Styleguide_Guide_GitHub.pdf) [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/)[<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/d3/ia)


The following page will further the Styleguide of Quantlets (Qs). An overview of the structure of a Q is given while explaining each part's relevance.
You will find descriptions and instructions on how to format your code as well as detailed examples about the required information for your Q. 

In the second section you will find basic instructions on how to work with the desktop client version of Github, which includes additional features to upload pictures and datafiles as separate files to your Q's repository.

Finally, several illustrative examples of correct Quantlets are listed in the Appendix.

### Structure of a Quantlet folder in a Github repository
This contains additional information to [**Styleguide of QuantLets**](guidelines/Styleguide_Guide_GitHub.pdf).

Every Quantlet folder consists of two elementary parts / files:
* __Metainfo.txt:__   
  - Contains meta-information about the functionality, origin and purpose of your Quantlet. Furthermore, lists of keywords and references to other related Quantlets. 
  - You will need to create a Metainfo.txt file, which will be used for the [Quantlet Visualization](http://www.quantlet.de) and data mining practices (e.g. clustering, filtering and recommendation engines) and is therefore __mandatory__.
  - We use YAML to format metainfo.txt to make things easy and fast, YAML is a human-friendly, cross language data serialization language that can be parsed by a computer. For further information about YAML notations, see [YAML](YAML.md).
  - You can use the [Metainfo.txt template](TEMPLATE_Metainfo.txt) as a blueprint for your Metainfo.txt file. If you are unsure about your Metainfo.txt files parsability, we recommend you to use this page [yaml-online-parser.appspot.com](http://yaml-online-parser.appspot.com/) to check it.

* __Quantletcode:__   
  - A correctly working code represents the second elementary part. The described functionality in the Metainfo.txt should practically be realizable by using the provided code.

#### _Important_:  
1. Make sure that the provided 'Name of Quantlet' and the actual filename of your provided Codefile is identical! Otherwise the automatic Readme.md creation will be incomplete.
2. If a Quantlet is written in more than one programming language (i.e. Matlab/SAS), add relevant data fields like Author[Matlab], Author[SAS], Submitted[Matlab], Submitted[SAS], ... to the Metainfo.txt if you want to distinguish between different versions/languages.
