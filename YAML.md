
## Main YAML rules
1. The colon ' : ' separates the data field (left) from its description (right) and the dash ' - ' enumerates list items. Avoid them in all other cases or apply Rule 2.
2. If you write multiple lines or use special characters (as in the first rule) you have to put your text in single or double quotes, i.e. 'Your text' or "Your text".
3. If you want to use the apostrophe character <'> (represented by the single quote sign) in your text just put your entire text in double quotes, e.g. "It's your text!". 
4. Characters like {_, -, :, ", ...} are meant to be special characters. In case of doubt simply put your text in quotes.
5. It is very important to type the __exact apostrophe character <'>__ as displayed above!!! Depending on your keyboard and/or editor some other apostrophe variants can appear. Then you have to correct them manually or via Copy&Paste in order to achieve the version above.

### YAML format examples

All following five notations are accepted by YAML.

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
