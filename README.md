# implementation-of-dynamic-programming-code-for-jack-s-car-rental-problem
in this repository, I've provided an implementation of jack's car rental problem with python using **value iteration** algorithm.
## dynamic programming
![image](https://user-images.githubusercontent.com/74808396/182336415-5a54d4b8-f307-4a3b-889b-85de5a05410f.png)

dynamic programming or DP is a model-based reinforcement algorithm. you can read more about dynamic programming [here](https://medium.com/free-code-camp/demystifying-dynamic-programming-3efafb8d4296).
in the DP we want to find ***true*** state value function of our world and for reaching this goal we have two strong methods. **[value iteration](https://towardsdatascience.com/the-value-iteration-algorithm-4714f113f7c5)** and **[policy iteration](https://towardsdatascience.com/policy-iteration-in-rl-an-illustration-6d58bdcb87a7#:~:text=Policy%20Iteration%C2%B9%20is%20an%20algorithm,its%20own%20rewards%20and%20risks.)**.
I've implemented value iteration algorithm in this repository.
## theoretical background
you can read cahpters 4&5 of [reinforcement learning: An introduction](http://incompleteideas.net/book/the-book.html) book to gain very good theoretical knowledge  about dynamic programming.
## problem statement
![image](https://user-images.githubusercontent.com/74808396/182337044-dc87e189-3b9a-4031-a484-4e5ac74b18b2.png)

Jack manages two locations for a nationwide car rental company. Each day, some number of customers arrive at each location to rent cars. If Jack has a car available, he rents it out and is credited $10 by the national company. If he is out of cars at that location, then the business is lost. Cars become available for rent the day after they are returned. To help ensure that cars are available where they are needed, Jack can move them between the two locations overnight, at a cost of $2 per car moved.

We assume that the number of cars requested and returned at each location is a Poisson random variable. Recall that if X is a Poisson random variable, then


Suppose λ is 3 and 4 for rental requests at the first and second locations and 3 and 2 for returns.

To simplify the problem slightly, we assume that there can be no more than 20 cars at each location (any additional cars are returned to the nationwide company, and thus disappear from the problem) and a maximum of five cars can be moved from one location to the other in one night. We take the discount rate γ to be 0.9 and formulate this as a continuing finite Markov Decision Process, where the time steps are days, the state is the number of cars at each location at the end of the day, and the actions are the net numbers of cars moved between the two locations overnight.

### But what does it mean to solve this problem?

Solving this problem means solving two things, firstly how many cars should Jack move, overnight, between each location, to maximize his total expected reward, i.e., what should be his strategy (policy) given a situation (state) and secondly, if Jack knows this strategy, how can he compare which situations are better than others (value)?

refrence: [medium](https://towardsdatascience.com/elucidating-policy-iteration-in-reinforcement-learning-jacks-car-rental-problem-d41b34c8aec7)
