
[<img src="https://github.com/QuantLet/Styleguide-and-FAQ/blob/master/pictures/banner.png" width="880" alt="Visit QuantNet">](http://quantlet.de/index.php?p=info)

# <img src="pictures/githublogo.png" width="120" /> **Styleguide and FAQ** [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/)[<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/d3/ia)


## Build software better, together, now (QuantNet 2.0 @ GitHub)
<img src="pictures/RapidPrototyping.png" width="880" />

### We highly recommend that you first familiarize yourself with the [Styleguide](guidelines/Styleguide_Guide_GitHub.pdf), at best before you start programming your project.

__This repository includes:__
- [__Styleguide of Quantlets__](guidelines/Styleguide_Guide_GitHub.pdf): There you find information about ...
	- requirements toward the Quantlet(s) and the accompanying Metainfo.txt file,
	- how to structure your Quantlet(s) in the repository,
- [Submission Guideline for Members of the Quantlet organization](guidelines/Submission_Guide_GitHub_Members.pdf): There you can find information ...
	- how to submit to or change an existing repository,
	- how to fork a repository into the Github Quantlet organization,
	- how to create a new repository.
- [Submission Guideline for NON Members of the Quantlet organization](guidelines/Submission_Guide_GitHub_Non_Members.pdf): There you find information ...
	- how to submit to an existing repository via pull request,
	- entire repsotories can only be forked into the Github Quantlet organisation by a member. 
- Frequently Asked Questions - [FAQ](https://github.com/QuantLet/Styleguide-and-Q-A/wiki)
- Template for mandatory file in every QuantLet subfolder of a repository (see also __Guideline II__):
 - [metainfo.txt](TEMPLATE_Metainfo.txt)
\- Please format your added content according to YAML as described in the [Styleguide](Styleguide.md). Thanks to your effort, we are able to automatically provide a standardized Readme.md to your repository.
- __YAML parser debugger__ ([yamldebugger](https://github.com/lborke/yamldebugger)) according to the QuantNet style guide:
	the R-Package [yamldebugger](https://github.com/lborke/yamldebugger) may be freely used for testing and validating the own Quantlets
	bevore uploading them into https://github.com/quantlet .
	Mainly, it checks the validity of the YAML meta information and the completeness of the mandatory data fields as described in [Styleguide](Styleguide.md)

	
__Guideline I:__
- Abbreviations
  - Q = Quantlet
  - QNet = Quantnet
  - repo = repository
  - GH = GitHub
  
__Guideline II:__
- Every Q has to be in its own subfolder in the repository (see also [Workflow](QuantNet2.pdf)). 
  - Reponame/Qfolder1/files of Q1
  - Reponame/Qfolder2/files of Q2
  - Reponame/Qfolder3/files of Q3
  
- Some Examples:

  1. [MSM] (https://github.com/QuantLet/MSM) (Reponame: MSM, 12 Qfolders)
  2. [Psychological-diagnostics] (https://github.com/QuantLet/Psychological-diagnostics) (Reponame: Psychological-diagnostics, 1 Qfolder)
  3. [TimeVaryingPenalization] (https://github.com/QuantLet/TimeVaryingPenalization) (Reponame: TimeVaryingPenalization, 4 Qfolders)

__Guideline III:__
- Avoid blanks in the repository names!
- Avoid unnecessary special characters in the names of repositories, subfolders and Qs
- In case of doubt use the underscore character "_"
- Some good Examples:
  1. [big_data_analysis] (https://github.com/QuantLet/big_data_analysis)
  2. [MMSTAT] (https://github.com/QuantLet/MMSTAT)
  3. [Git2Q3-Collaboration] (https://github.com/QuantLet/Git2Q3-Collaboration)
- Some bad Examples:
  1. [lCARE-BTU-HU-] (https://github.com/QuantLet/lCARE-BTU-HU-) (unnecessary dash)
- Please note that repos with bad name notation will be excluded from final validation and importing into the [Visualization] (http://quantnet.wiwi.hu-berlin.de/d3/ia/). It's up to you to rename your repos accordingly. Actually, some special characters make the automatic processing impossible.
