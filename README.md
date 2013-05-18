The Mozilla and Eclipse Defect Tracking Dataset
============================================

Welcome to the _Mozilla and Eclipse Defect Tracking Dataset_ containing over 47000 and 168000 of bugs reported for Eclipse and Mozilla respectively. Besides the single latest snapshot of a bug report, we also provide all the changes each bug has gone through in its lifetime. Below, you can find additional information about the dataset.

# Table of Contents
- [Description](#description)
	- [Model of the Dataset](#model-of-the-dataset)
	- [Structure of the dataset](#structure-of-the-dataset)

# Description
The Eclipse and Mozilla Defect Tracking Dataset contains bug reports reported for 4 popular products of both Eclipse and Mozilla. For Eclipse and Mozilla respectively, the following products are selected:

<table border="0">
<tr>
<td>
**Product**		| **No. of Bugs**	| **No. of Components**
----------------|-------------------|----------------------
Platform		|	24775			|	22
JDT				|	10814			|	6
CDT				|	5640			|	20
GEF				|	5655			|	5
<td>
<td>
**Product**		| **No. of Bugs**	| **No. of Components**
----------------|-------------------|----------------------
Platform		|	24775			|	22
JDT				|	10814			|	6
CDT				|	5640			|	20
GEF				|	5655			|	5
<td>
</tr>
</table>

For each product, we provide the resolved reported bugs with the corresponding report attributes as shows in Figure~\ref{fig:model}. The attributes (instances of _Report Attribute_ in the model) that are considered in this dataset are the following:


For each attribute, we compiled a list of updates denoting the different "changes" that have been performed over the entire lifetime of the respective report. For each such change, we include the timestamp when the attribute was updated (the _when_) and the new value of the respective bug report attribute (the _what_).

## Model of the Dataset

<img align="center" width="60%" src="https://raw.github.com/ansymo/msr2013-bug_dataset/master/figures/model.png">

## Structure of the Dataset

<img align="center" width="60%" src="https://raw.github.com/ansymo/msr2013-bug_dataset/master/figures/dataset-structure.png">


In regards of its format, the _Eclipse and Mozilla Defect Tracking Dataset_ has been packaged as a bundle of XML files (see Figure~\ref{fig:structure}). Primarily, the two projects Eclipse and Mozilla are organized in separate directories. For each product of the respective projects, there is a separate directory storing all information relevant for that particular product. Each of these directories, or smaller sub-repositories, consists of a set of XML files containing the respective updates of a single particular attribute. This way, the full history of each considered bug attribute is stored in each separate XML file.

Furthermore, each product directory includes an additional ``main'' XML file (_i.e.,_ \textsf{reports.xml}) which stores the attributes of the bug that are unchangeable throughout the lifetime of the bug, _i.e.,_ the \textsf{id} of the reported bug, the recorded time of when the bug was reported and the particular reporter who filed the bug. 
For the timestamps we use for the opening time and time of each update, we use the UNIX time notation\footnote{Unix time, or POSIX time, is a system for describing instances in time, defined as the number of seconds that have elapsed since midnight Coordinated Universal Time (UTC), 1 January 1970.}. In Listing~\ref{lst:myListing1} and~\ref{lst:myListing2}, we show fragments of the XML files content and structure.
		
# Citing us

> Ahmed Lamkanfi, Javier P\'erez, Serge Demeyer, "The Eclipse and Mozilla Defect Tracking Dataset: a Genuine Dataset for Mining Bug Information" in _MSR '13: Proceedings of the 10th Working Conference on Mining Software Repositories_, May 18-–19, 2013. San Francisco, California, USA.

# Please contribute



