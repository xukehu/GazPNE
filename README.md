# ZSL-PLT
## Basic description

Location information in microblogs is crucial for situational awareness during disaster response, including where the damage is, where people need assistance and where help is available. Current approaches for extracting the place names from microblogs can be mainly divided into three groups: rule-based, gazetteer-based, and statistical learning-based. However, they face the challenge of detecting long place names not included in gazetteers, generalizing the extractor, and lacking sufficient annotated microblog data, respectively. To mitigate the gap, this study proposes a zero-shot learning approach for place entity tagging from tweets, named ZSL-PLT, which does not assume any annotated sentences at training time. It fuses rule, gazetteer, and deep learning-based approaches to achieve the best performance among all. Specifically, we apply a Convolutional Neural Network (CNN) and Long Short-Term Memory (LSTM)-fused deep learning model called C-LSTM to derive a general place name classifier based on abundant positive examples (around 22 million) from gazetteers (i.e., OpenStreetMap and GeoNames) and negative examples (around 220 million) synthesized by rules. The classifier is then used to score n-gram segments of the tweet text and select the top none-overlapping candidates. We evaluate the approach on 4,500 disaster-related tweets, including around 9,500 place names from three targeted streams corresponding to the floods in Louisiana (the US), Houston (the US), and Chennai (India), respectively. We provide a comparison against several competitive baselines. The results show that the proposed approach improves the average F1-score from 0.81 for the best performing system to 0.87 (a 7\% increase).
The Architecture of ZSL-PLT is as follows:
![Alt text](figure/workflow.tif?raw=true "Title")
