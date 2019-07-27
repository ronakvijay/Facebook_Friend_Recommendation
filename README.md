## Social network Graph Link Prediction - Facebook Challenge
### Problem statement:
Given a directed social graph, have to predict missing links to recommend users (Link Prediction in graph).

### Data Overview
Taken data from facebook's recruting challenge on kaggle https://www.kaggle.com/c/FacebookRecruiting

data contains two columns soutce and destination eac edge in graph.

Data columns (total 2 columns):
- source_node int64
- destination_node int64

### Mapping the problem into supervised learning problem:
- Generated training samples of good and bad links from given directed graph and for each link got some features like no of followers, is he followed bak, page rank, katz score, adar index, some svd features of adj matrix, some weight features etc. and trained ml model based on these features to predict link.
- Some reference papers anda videos:
  - https://www.cs.cornell.edu/home/kleinber/linkpred.pdf
  - https://www3.nd.edu/~dial/publications/lichtenwalter2010new.pdf
  - https://kaggle2.blob.core.windows.net/forum-message-attachments/2594/supervised_link_prediction.pdf
  - https://www.youtube.com/watch?v=2M77Hgy17cg
### Business objectives and constraints:
- No low-latency requirement.
- Probability of prediction is useful to recommend highest probability links.
### Performace metric for supervised learning:
- Both precision and recall is important so F1 score is good choice.
- Confusion matrix
