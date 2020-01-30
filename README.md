# TDDiscourse

This repository contains the TDDiscourse dataset, created as part of the paper: ["TDDiscourse: A Dataset for Discourse-Level Temporal Ordering of Events" (Naik et al., 2019)](https://www.aclweb.org/anthology/W19-5929.pdf).

TDDiscourse is a dataset for temporal ordering of events, which specifically focuses on event pairs that are more than one sentence apart in a document. 

TDDiscourse was created by augmenting TimeBank-Dense [(Cassidy et al., 2014)](https://www.aclweb.org/anthology/P14-2082.pdf), a corpus of English news articles containing annotations for events and temporal relations based on the TimeML annotation scheme [(Sauri et al., 2006)](https://catalog.ldc.upenn.edu/docs/LDC2006T08/timeml_annguide_1.2.1.pdf). 

TimeBank-Dense focuses mainly on event pairs which are in the same or adjacent sentences (though they do include labels for some event pairs which are more than one sentence apart). TDDiscourse was created to address this gap and to turn the focus towards discourse-level temporal ordering, which turns out to be a harder task.

This dataset is divided into the following subsets:

#### 1. TDDMan
TDDMan is manually annotated subset of TDDiscourse, created according to the guidelines described in [(Naik et al., 2019)](https://www.aclweb.org/anthology/W19-5929.pdf). The TDDMan sub-folder contains the train, dev, and test splits for this subset. Additionally, it also contains a file which provides extra annotations for a small sample (n=107) from the test set. These extra annotations label each event pair with the phenomena required to deduce the correct temporal relation for the pair. A complete list of the phenomena and some prelimiary phenomenon distribution statistics can be found in section 6 of [(Naik et al., 2019)](https://www.aclweb.org/anthology/W19-5929.pdf).

#### 2. TDDAuto
TDDAuto is the automatically generated subset of TDDiscourse, created according by the heuristic algorithm described in [(Naik et al., 2019)](https://www.aclweb.org/anthology/W19-5929.pdf). The TDDAuto sub-folder contains the train, dev, and test splits for this subset. It also contains a file which provides extra phenomenon annotations for a small sample (n=110) from the test set, similar to the one in TDDMan.

#### Dataset Statistics:
The following table gives a brief overview of the train, dev, and test splits for TDDiscourse:

| Subset | Train | Dev | Test |
|--------|-----|-----|--------|
| TDDMan | 4000 | 650 | 1500 |
| TDDAuto | 32607 | 1435 | 4258 |

#### Temporal Relation Labels:
TDDiscourse uses the following temporal relations:

| Label | Relation |
|----|-----|
| a | After |
| b | Before |
| i | Includes |
| ii | Is Included |
| s | Simultaneous |

For any questions or to report any issues with the data, please reach out to: anaik@cs.cmu.edu.
