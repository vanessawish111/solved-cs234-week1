Download Link: https://assignmentchef.com/product/solved-cs234-week1
<br>
<ul>

 <li>[CA session] Problem 1: MDP Design</li>

</ul>

You are in a Las Vegas casino! You have $20 for this casino venture and will play until you lose it all or as soon as you double your money (i.e., increase your holding to at least $40). You can choose to play two slot machines: 1) slot machine A costs $10 to play and will return $20 with probability 0.05 and $0 otherwise; and 2) slot machine B costs $20 to play and will return $30 with probability 0.01 and $0 otherwise. Until you are done, you will choose to play machine A or machine B in each turn. In the space below, provide an MDP that captures the above description.

Describe the state space, action space, rewards and transition probabilities. Assume the discount factor <em>γ </em>= 1. Rewards should yield a higher reward when terminating with $40 than when terminating with $0. Also, the reward for terminating with $40 should be the same regardless of how we got there (and equivalently for $0).

<ul>

 <li>Problem 2: Contradicting Contractions?</li>

</ul>

Consider an MDP <em>M</em>(<em>S,A,P,R,γ</em>) with 2 states <em>S </em>= {<em>S</em><sub>1</sub><em>,S</em><sub>2</sub>}. From each state there are 2 available actions <em>A </em>= {<em>stay,go</em>}. Choosing <em>“stay” </em>from any state leaves you in the same state and gives reward -1. Choosing <em>“go” </em>from state <em>S</em><sub>1 </sub>takes you to state <em>S</em><sub>2 </sub>deterministically giving reward -2, while choosing <em>“go” </em>from state <em>S</em><sub>2 </sub>ends the episode giving reward 3. Let <em>γ </em>= 1.

Let <em>V </em><sup>∗</sup>(<em>s</em>) be the optimal value function in state <em>s</em>. As you learned in class, value iteration produces iterates <em>V</em><sub>1</sub>(<em>s</em>)<em>,V</em><sub>2</sub>(<em>s</em>)<em>,V</em><sub>3</sub>(<em>s</em>)<em>,… </em>that eventually converge to <em>V </em><sup>∗</sup>(<em>s</em>).

<ul>

 <li>[CA Session]</li>

</ul>

Prove that the ∞-norm distance between the current value function <em>V <sup>k </sup></em>and the optimal value function <em>V </em><sup>∗ </sup>decreases after each iteration of value iteration.

<ul>

 <li>[Breakout Rooms]</li>

</ul>

Now let us consider exactly what forms of convergence are ensured.

For the given MDP, let us initialize value iteration as <em>V</em><sub>0 </sub>= [0<em>,</em>0]. Then <em>V</em><sub>1 </sub>= [−1<em>,</em>3] and <em>V</em><sub>2 </sub>= [1<em>,</em>3]. We also have <em>V </em><sup>∗ </sup>= [1<em>,</em>3].

Is there monotonic improvement in the <em>V </em>estimates for all states? If not, does this contradict the result in Q2(a) and why or why not?

<ul>

 <li>[Breakout Rooms] Problem 3: Stochastic Optimal Policies</li>

</ul>

Given an optimal policy that is <em>stochastic </em>in an MDP, show that there is always another deterministic policy that has the same (optimal) value.

<ul>

 <li>[Breakout Rooms] Problem 4: Parallelizing Value Iteration</li>

</ul>

During a single iteration of the Value Iteration algorithm, we typically iterate over the states in S in some order to update <em>V<sub>t</sub></em>(<em>s</em>) to <em>V<sub>t</sub></em><sub>+1</sub>(<em>s</em>) for all states <em>s</em>. Is it possible to do this iterative process in parallel? Explain why or why not.