# Federated-Learning-through-Distance-Based-Clustering
Federated Learning (FL) is a system architecture that leverages distributed networks such as mobile phones to enhance AI model personalization and performance while keeping personal data confidential to its owner. In this project, we aim to propose a novel addition to the traditional FL design that leverages clustering to group similar devices together and enhance their collaboration with one another during training.

In this paper, we carry out a three-phase experiment to explore our clustering method. The following is a summary of what we carried out:
* Phase 1
  * Split a target dataset across multiple devices
  * Train all devices using a traditional FL learning method

* Phase 2
  * Based on the weights of the devices after Phase 2, we run two clustering algorithms. The clustering algorithms output a list of clusters, with each cluster having a list of device ids belonging to it. Each cluster gets its own weights computed for it by averaging the weights of all the devices within it.
  * Train the devices further but instead of reporting their weights back to the central server, they report them to their cluster only. Therefore, this essentially creates multiple traditional FL networks where each network represents one cluster and the subset of devices belonging to that cluster

* Phase 3
  * We calculate multiple permutations of the weights generated after Phase 2 is complete and then use it to evaluate the improvement of the model after clustering is applied.
