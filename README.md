# DarwinNet - Can Neural nets learn without backprop?

DarwinNet is just a fancy name for evolutionary neural net with a small difference. Most evolutionary neural nets use evolutionary techniques along with backprop to come up with the best architecture for neural net. The learning (weight updates) still happens with backprop.
There are few projects that use evolutionary neural net to learn the weights of the network without any backprop. 
https://github.com/ivanseidel/IAMDinosaur
and
https://github.com/mitchvoll/NeuroEvolutionDriver

## Idea : 
1. Create a bunch of neural nets (genomes) with random weights. This is the nitial population.
2. Evaluate all the models with a fitness function (Eg. accuracy or loss for a device classification task) on a dataset.
3. Natural selection - Select the top N best neural nets based on fitness function.
4. Crossover - Use the selected neural nets to create new ones (crossover can be done in multiple ways).
5. Mutation - Add random noise to the weights of the neural nets. 
6. Repeat step 2.

If you look at neural nets as a part of your brain then backkprop probably makes sense (with a good loss function - which we are yet to invent). But, the brain is good at learning new things because it comes with hundreds of thosands of years of evolutionary context. The idea here is to see if neural networks can learn without any backprop and with evolution. The above two examples use linear neural nets in a reinforcement learning setting to let an agent learn from the mistakes of the previous generations. This is shown to be working well. However, the number of output units in the above two examples is fewer (3 to 6). The aim here is to see if such a technique works and scales with large dataset and slightly more complicated environment like classification and image regeneration (like autoencoders).


