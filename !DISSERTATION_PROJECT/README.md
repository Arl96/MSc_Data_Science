
This repository contains my dissertation project report (`FINAL.pdf`), as well as the four jupyter notebooks containing the code I wrote for this project.

<div class="myWrapper" markdown="1">
# my markdown content
this content is wrapped into a div with class "myWrapper"
</div>

**ABSTRACT**

 Human activity recognition (HAR) – the process of using machine learning 
algorithms to build models which classify human movement data into a set of predefined 
activity categories – has become a field of intense study in recent years. Over the last decade, 
many researchers have reported achieving state-of-the-art performance by employing deep 
learning algorithms, such as long short-term memory recurrent neural networks (LSTMs), in
their HAR models. However, there is a lack of standardisation of state-of-the-art 
performance in HAR research. Thus, we compared standardised versions of four commonly 
used LSTM architectures on their performance on two commonly used HAR datasets to 
more definitively determine which LSTM varieties show the most promise for HAR 
applications. We found that the CNN-LSTM architecture showed the most promise, reaching 
high levels of performance with minimal training time.

We also attempted to improve the performance of our models in several ways. Firstly,
we tested the efficacy of using a two-stage classification approach which first divided the data 
into stationary or dynamic movement categories before classifying the data into a specific 
activity category. This classification approach was largely unsuccessful, as it increased 
training times whilst rarely improving classification performance compared to the models 
built with a standard one-stage classifier. 

Secondly, two data manipulation techniques were applied to the datasets, the results 
from which were inconclusive. The first, oversampling, was not found to improve model 
performance, though we propose that it would be worthwhile to investigate using other, 
more advanced oversampling methods than the one we employed in our experiments. The 
second data manipulation technique, feature selection, improved performance in one dataset 
but not the other.
