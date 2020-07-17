# Exercise 2.8

## Question:
In Figure 2.4 the UCB algorithm shows a distinct spike in performance on the
11th step. Why is this? Note that for your answer to be fully satisfactory it
must explain both why the reward increases on the 11th step and why it
decreases on the subsequent steps. Hint: if _c_ = 1, then the spike is less
prominent.

## Answer:
Based on the definition of the UCB algorithm, the agent is encouraged to
explore. Remember, any previously unexplored action is by definition a
maximizing action, so the agent will have explored all of the 10 (or, in general
_k_) different arms of the testbed by the 11th step. After exploring all of the different options, the agent will have a better initial estimate of the action values compared to the ε-greedy algorithm (which will have done relatively little exploration). The better initial estimates will lead the UCB-based agent to choose a better action on the 11th step.

It is important to note that while the UCB-based agent has relatively good
initial estimates of the action values, they are not (necessarily) optimal.
Therefore, the agent will have to continue interacting with the testbed to
improve its action value estimates, causing the average reward to drop until the
estimates start to converge on their expected values.
