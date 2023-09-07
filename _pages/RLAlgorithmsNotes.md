## PPO

- It's multistep actually, the gradient update uses multiple steps back in time

## SAC



## TD3



## Double Deep Q Learning

Is this a new thing?

Helping to overcome overestimation?

It is based on Double Learning from Hasselt 2010 but with deep learning updates

https://towardsdatascience.com/double-deep-q-networks-905dd8325412



## Deadly Triad

The deadly triad issue is the fact that combining Bootstrapping, off-policy learning and function approximations ends up in a lot of instabilities, or no convergence. (https://towardsdatascience.com/introduction-to-the-deadly-triad-issue-of-reinforcement-learning-53613d6d11db)

- Bootstrapping and off policy learning and maximization
- 2018 Sutton and brat paper on this
- More recent empirical methods
- Doing these three things causes problems with convergence and overestimation



## Optimistic Q Functions

There is lots of other work on this recently as well.