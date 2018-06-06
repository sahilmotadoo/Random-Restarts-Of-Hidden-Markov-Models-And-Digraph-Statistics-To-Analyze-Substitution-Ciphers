#Random_Restarts_Of_Hidden_Markov_Models_And_Digraph_Statistics_To_Analyze_Substitution_Ciphers

Similar to my previous project, which could be found at:
https://github.com/sahilmotadoo/Cracking-Substitution-Ciphers-Using-Hidden-Markov-Models-And-Digraph-Statistics

We use the same concepts to analyze substitution ciphers using HMM's, the difference being in the size of the data. In my previous project I have encrypted upto 50k characters. But what if we are presented with a situation where we have limited data? Or in this case, we have only a portion of the encrypted text 

The theory behind my implementation is pretty straighforward. HMM is a hill-climb based algorithm which tends to achieve a local maxima easily. When we reach a local maxima, the model is unable to improve further and we do not obtain the best possible results. Also, there is no way to come down this hill, we are kind of stuck there.

When we are presented with a local maxima among a set of data points, we randomly choose another point and restart our algorithm. So in essence, by restarting the HMM's 'n' times, we are able to achieve the best possible results with minimum data.

Of course this technique is computationally expensive and you would want to increase the number of restarts depending on data availability (i.e. low data volume means more restarts), but it is a trade-off. 
