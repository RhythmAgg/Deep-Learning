# Deep-Learning - Theory and practices

## Assignement 1
### Q1
- The question involved reaching global minimum of the popular benchmarking function Rosenbrock function $` f(x, y) = x^2 + 100(y − x^2)^2 `$ which has its global minimum at X = $`[0 , 0]^T `$
- The optimization was achieved through Gradient descent algorithms and contour plots were plotted to show the convergence of different Algorithms (regular GD, Polyak Momentum, Nesterov, Adam)
- The Code uses python with numpy and pandas as well as Matplotlib for Visualisation

### Q2
- The question involved reaching global and local minimum of the function $`\frac{50}{9}(x^2 + y^2)^3 - \frac{209}{18}(x^2 + y^2)^2 + \frac{59}{9}(x^2 + y^2) `$  which has its global minimum at X = $`[0 , 0]^T `$
- and local minima at $` x^2 + y^2 = 1 `$
- The optimization was achieved through Gradient descent algorithms and contour plots were plotted to show the convergence of different Algorithms (regular GD, Polyak Momentum, Nesterov, Adam)
- The Code uses python with numpy and pandas as well as Matplotlib for Visualisation

### Q3
- This part of the assignment was based on implementing a Multi Layered Neural Network for regression task from scratch using numpy and pandas.
- The dataset is ' Concrete Compressive Strength '  along with its Meta data. It contains samples with numerical features along with a real valued Target variable which gives the compressive strength of the sample as a highly non-linear function of the features.
- The neural network has been implemented with different set of hyperparameters and Update algorithms (*backProp*, *Rprop*, *Quickprop*)
- The hyperparameters include different Activation functions used at the hidden layer (*tanh*, *LeakyRELU*) and different number of hidden units)
- For all Models, MSE loss has been used as the optimization criterion
- Model training and Validation testing has been done with 30% test split without replacement. The no. of epochs has been set to 1000 for each regression model and graphs have been plotted depicting convergence with Epochs
- The Data preprossing strategies like Standard Scaling and Min Max scaling have been tested to improve predictions, and Data visualisation to see Features distribution
- All sets of the parameters have been compared on the basis of the time to convergence, Average Test loss and Time taken for the epochs and inferences have been drawn on these metrics

## Assignement 2 (Pytorch)
### Q1
- The task was to build an AutoRegressive model utilising RNN capabilities
- Experimented with different hidden layer, number of neurons
- Used early stopping as the regularization
- Visualised the loss and convergence

### Q2
- The task was to show long term dependency retained in LSTMS as opposed to RNNS which suffer from vanishing gradient issue
- The input sequence length was kept 100 with direct dependency between the timestep(0) and timestep(100) with random sequence in between
- RNNs and LSTMs were implemented and their performance measured on the dataset generated

### Q3
- The task was to train an encoder-decoder model to learn a transformation which
takes a sentence and outputs a transformed sentence. Both the sentence and
the transformed sentence are 8 characters long and only consist of lowercase
English alphabets.
- The encoder consisted of Bidirectional RNN/GRU with experimental hidden size
- The decoder was unidirectional RNN/GRU with input concatenated with encoder output at all timestep
- Teacher enforcing with variable probability was used during training for faster convergence
- With early stopping as regularisation, the model with least Validation Loss was saved and used for inference
- A checker script was run to evaluate the performance of the model (incorporated in the notebook itself)
