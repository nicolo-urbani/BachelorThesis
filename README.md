# Bachelor Thesis
Corso di Laurea Triennale in Informatica - Univesità degli studi di Milano Bicocca

Title: Adoption of Machine Learning Techniques for Intrusion Detection in
Telecommunication Network


## Abastrat

In recent years, to safeguard Telecommunication Networks from increasingly frequent and sophisticated attacks, various methods have been designed and developed by the scientific community to detect intrusions. Among the most widespread and effective solutions are various tools, including Network Intrusion Detection Systems (NIDS) based on Machine Learning techniques. The use of such NIDS systems has become necessary to provide more secure networks and mitigate the costs associated with attacks.

This report describes the internship activity aimed at analyzing and comparing different Machine Learning techniques for the identification and classification of attacks, based on network traffic analysis, a particularly relevant purpose for security in Telecommunication Networks, especially in the IoT (Internet of Things) domain.

Several datasets were considered to evaluate performance on different attacks and environments. The datasets used are NF-ToN-IoT-v2 and NF-CSE-CIC-IDS-2018-v2 (new versions of the ToN-IoT and CSE-CIC-IDS-2018 datasets), based on the set of features collected through the NetFlow protocol. These datasets, widely used in the literature, are recent and realistic, extracted from network environments simulating real situations.

Various Machine Learning techniques were explored, including Decision Trees, Random Forests, and Neural Networks, with the aim of comparing them. These models were applied to the NF-ToN-IoT-v2 dataset to evaluate performance and identify the most suitable classification model. The performance (F1-Score) achieved by the various models is comparable to those obtained by state-of-the-art works.

After choosing the best model, Random Forests, performance is evaluated by combining the NF-ToN-IoT-v2 and NF-CSE-CIC-IDS-2018-v2 datasets to assess the model's behavior on more complex datasets with different origins. Furthermore, additional analyses allow evaluating the chosen model in non-ideal situations, for example, when the model is tested on a specific type of attack not present during training. By combining multiple datasets, although model training is more complex, in most cases, flows are classified correctly. Further analyses conclude that when the model is not trained on a specific attack pattern, attacks are not classified correctly.

Finally, SHAP, an explainable AI methodology, is used to explain and interpret the classification decisions of Random Forests on the NF-ToN-IoT-v2 dataset. Considering the complexity of the model, the Shapley values of the features are analyzed to determine the contribution of each feature to the final prediction. From the analyses performed, it emerges that the feature that most influences classification is Longest Flow Packet, i.e., the length (in bytes) of the largest packet transmitted in the flow. The use of the SHAP method on a specific class has allowed identifying the most relevant features in the classification process of individual attacks.
