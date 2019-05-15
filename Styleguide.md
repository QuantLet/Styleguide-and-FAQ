
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
- You will need to create a Metainfo.txt file, which will be used for the [Quantlet Visualization] (http://www.quantlet.de) and data mining practices (e.g. clustering, filtering and recommendation engines) and is therefore __mandatory__.
- We use YAML to format metainfo.txt to make things easy and fast, YAML is a human-friendly, cross language data serialization language that can be parsed by a computer.
- You can use the [Metainfo.txt template](TEMPLATE_Metainfo.txt) as a blueprint for your Metainfo.txt file. If you are unsure about your Metainfo.txt files parsability, we recommend the page [yaml-online-parser.appspot.com](http://yaml-online-parser.appspot.com/) to check it.

* __Quantletcode:__ A correctly working code represents the second elementary part. The described functionality in the Metainfo.txt should practically be realizable by using the provided code.

#### _Important_:  
1. Make sure that the provided 'Name of Quantlet' and the actual filename of your provided Codefile is identical! Otherwise the automatic Readme.md creation will be incomplete.
2. If a Quantlet is written in more than one programming language (i.e. Matlab/SAS), add relevant data fields like Author[Matlab], Author[SAS], Submitted[Matlab], Submitted[SAS], ... to the Metainfo.txt if you want to distinguish between different versions/languages.

#### Three main YAML rules:
1. The colon ' : ' separates the data field (left) from its description (right) and the dash ' - ' enumerates list items. Avoid them in all other cases or apply Rule 2.
2. If you write multiple lines or use special characters (as in Rule 1 or examples below) you have to put your text in single or double quotes, i.e. 'Your text' or "Your text".
3. If you want to use the apostrophe character <'> (represented by the single quote sign) in your text just put your entire text in double quotes, e.g. "It's your text!". 
4. Characters like {_, -, :, ", ...} are meant to be special characters. In case of doubt simply put your text in quotes.
5. [YAML](YAML.md)

### It is very important to type the exact apostrophe character <'> as displayed above!! Depending on your keyboard and/or editor some other apostrophe variants can appear. Then you have to correct them manually or via Copy&Paste in order to achieve the version above.

- __Optional__ data fields, where no description is provided, can be omitted completely (Above example includes them for illustration purposes anyway). The automatic Readme.md creation process also skips empty data fields.
- The order of appearance of the data fields is irrelevant. They are treated as an "unordered list". Only their presence and content behind the colon ' : ' is crucial.
- 

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
