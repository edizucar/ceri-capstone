# Ediz Ucar CERI Capstone Project

The purpose of this project is to experimentally verify some of the claims of [grokking](https://arxiv.org/abs/2201.02177). Gaining insight into how models generalise out of the training distribution will be very useful, especially for models which operate on very complex domains e.g. with an action space of interactions with the physical world..


In this project, I experiment with some simple one layer MLPs on the XOR problem. The Python notebook demonstrates examples of different training vs test loss graphs based on different setup by modifying:
- Dataset size
- Hidden layer size
- Regularisation method
- Number of training epochs

The notebook provides examples of effective generalisation in which the underlying model has genuinely learned the XOR operation.

There are also examples of misgeneralisation (overfitting). These generally occurred with high parameter counts and small numbers of hidden layers.


There were no examples of grokking behaviour i.e. initial overfitting, but good generalisation after a long training period. There are multiple reasons that could have caused this:

1. Model architecture. The model architecture used is very simple and may not be suitable for more complex behaviour such as grokking. The grokking paper uses a transformer architecture which is more complex.

2. Problem complexity. The problem used - XOR - is similar in complexity to the complexity of problem used in the grokking paper (modular arithmetic) however it may not be relative to the architecture used. MLPs with a hidden layer can very easily solve XOR.

3. Training time. Grokking tends to occur over long training times, far beyond where you would normally train. I did not have the compute or time resources to be able to do this.

I would like to continue this project further with more experiments to see if I can, firstly replicate the grokking result and secondly to analyse the changes in weights before and after grokking occurs. The limiting factor on this project was primarily time constraints. Much of the time spent was background reading and code setup.
