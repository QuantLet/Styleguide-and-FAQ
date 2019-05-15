
#### Main YAML rules:
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
