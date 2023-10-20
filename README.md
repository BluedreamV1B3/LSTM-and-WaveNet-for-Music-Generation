# LSTM and WaveNet for Music Generation

The primary goal of this task is to gain a comprehensive understanding of building sequential models and handling sequential data. This knowledge can be applied to a wide range of applications in the fields of machine learning, and artificial intelligence.To achieve this, I employ TensorFlow to construct a Long Short-Term Memory (LSTM) neural network and a scaled-down version of WaveNet. The research centers around generating new chorales using the Bach chorales dataset as the training data. This endeavor serves multiple purposes:

1. Sequential Data Handling:

Understand the nuances of working with sequential data, which is fundamental in various machine learning applications. Music is a prime example of sequential data, and exploring it offers insights into handling temporal dependencies effectively.

2. TensorFlow Proficiency:

Strengthen our proficiency with TensorFlow, a widely used deep learning framework. Building a sequential model in TensorFlow, such as the LSTM network, enables me to enhance our expertise in implementing neural networks for specific tasks.

3. Chorale Generation with WaveNet:

Explore the potential of WaveNet, a famous generative model. In this case, I use a scaled-down version of WaveNet to generate new chorales. This help me to explore advanced techniques for creative music composition.

# The Dataset: 

The Bach chorales dataset comprises a collection of concise musical compositions, typically characterized by their consistent stylistic features. These chorales originated in the 18th century and were initially crafted by Johann Sebastian Bach. He employed a distinctive method of taking pre-existing melodies from contemporary Lutheran hymns and then orchestrating them to generate the parts for the remaining three voices. This dataset encompasses a total of 382 chorales, with each chorale varying in length from 100 to 640 time steps. Within each time step, you can find 4 integers, where each integer is indicative of a note's corresponding index on a piano. Notably, a value of 0 within a time step denotes that no musical note is being played at that specific moment.

Download the dataset here: https://homl.info/bach

# WaveNet

In a 2016 research paper, Aaron van den Oord and his fellow DeepMind researchers introduced an innovative architecture known as WaveNet. The primary aim of WaveNet is to generate new data samples that adhere to the original data distribution, making it a Generative Model. Their approach involved stacking 1D convolutional layers and progressively increasing the dilation rate, which controls how widely separated a neuron's inputs are at each layer. To elaborate, the initial convolutional layer analyzes just two time steps at once, whereas the subsequent layer considers four time steps, extending its receptive field. This progression continues with each layer doubling the time steps it examines. This design empowers the lower layers to capture short-term patterns, while the higher layers excel at recognizing long-term patterns. Thanks to this doubling dilation rate strategy, the network can efficiently process exceedingly long sequences.

![Xception](Xception-CNN.png)
