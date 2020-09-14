# Implementation Goals:
A collection of research papers with corresponding algorithms and/or neural network architectures that I personally find
interesting, and would like to implement. As I make progress with these implementations (most likely in separate repositories)
I will maintain links to the implementations here, on this page.

## [Recurrent Neural Networks (RNNs)](https://en.wikipedia.org/wiki/Recurrent_neural_network):
### LSTMs and CTC:

#### 1. [Long Short-term Memory Network (LSTM)](https://en.wikipedia.org/wiki/Long_short-term_memory):
As far as I know, this is the first research paper (dating back to 1997) introducing the LSTM recurrent neural network 
architecture, for the purposes of offline handwriting recognition:
- [Long Short-term Memory](https://www.researchgate.net/publication/13853244_Long_Short-term_Memory) in
`Resources/RecurrentNeuralNets/lstm.pdf`

#### 2. RNNs for Keyword Spotting:
This research paper from Baidu was supposedly one of the first to apply RNNs to keyword detection in speech recognition:
- [Convolutional Recurrent Neural Networks for Small-Footprint Keyword Spotting](https://arxiv.org/ftp/arxiv/papers/1703/1703.05390.pdf)
in `Resources/RecurrentNeuralNets/ConvolutionalRNNsforKeywordSpotting.pdf`

#### 3. [Connectionist Temporal Classification (CTC) for RNNs](https://en.wikipedia.org/wiki/Connectionist_temporal_classification):
The following research paper from 2006 provides a methodology for training RNNs on sequence problems with variable timings.
Specifically, this LSTM network deals with connected handwriting recognition:
- [Connectionist Temporal Classification: Labelling Unsegmented Sequence Data with Recurrent Neural Networks](https://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=A556C400FD952400D0E8876B7F135200?doi=10.1.1.75.6306&rep=rep1&type=pdf)
in `Resources/RecurrentNeuralNets/ConnectionistTemporalClassification.pdf`

#### 4. Deep Speech End-to-End Speech Recognition:
This research paper from 2014 by Baidu, leveraged [CTC-trained RNNs](https://en.wikipedia.org/wiki/Connectionist_temporal_classification) 
to break the [Switchboard 2000 HUB5 speech recognition dataset](https://catalog.ldc.upenn.edu/LDC2002S09) benchmark:
- [Deep Speech: Scaling up end-to-end speech recognition](https://arxiv.org/abs/1412.5567) in 
`Resources/RecurrentNeuralNets/DeepSpeechScalingUpEndtoEndSpeechRecognition.pdf`

#### 5. RNN Acoustic Models for Speech Recognition
This [blog post](https://ai.googleblog.com/2015/09/google-voice-search-faster-and-more.html) and accompanying research
paper from Google in 2015, describes how recurrent neural networks were used to increase accuracy in Google voice search:
- [Fast and Accurate Recurrent Neural Network Acoustic Models for Speech Recognition](https://arxiv.org/pdf/1507.06947.pdf)
in `Resources/RecurrentNeuralNets/RNNAcousticModelsForSpeechRecognition.pdf`

#### 6. Show and Tell: A Neural Image Caption Generator
This research paper by Google in 2015 made headlines for using a CNN for object recognition, combined with an RNN to
generate image captions:
- [Show and Tell: A Neural Image Caption Generator](https://arxiv.org/pdf/1411.4555.pdf) in 
`Resources/RecurrentNeuralNets/ShowAndTellNeuralImageCaptionGenerator.pdf`


