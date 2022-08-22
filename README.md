# Flash Onsen

>**Note** <br />
> Work in progress

## Economic rationality

### Individual rationality
An agent is individually rational if they try to maximize its own revenue.
Example: Construct block with max fees

A miner receives a set of transactions $xx _{1}, \ldots, tx x _{n}$ with gas price $b_{1}, \ldots, b_{n}$ and $g_{1}, \ldots, g_{n}$ units of gas. The miner can choose any subset of transactions $T X$ such that $\sum_{t x \in T X } g_{ tx } \leq \max$ Gas.


\begin{equation*}
    T X \text { such that } \sum_{ tx \in T X } g_{ tx } \leq \max \text { Gas. }
\end{equation*}


### Example: Transaction inclusion
- A "dummy" node orders transaction by timestamp, by transaction hash or randomly.
- A rational node tries to solve the following optimization problem:
\begin{equation*}
\begin{array}{ll}
\max & \sum_{i=1}^{n} x_{i} b_{i} g_{i} \\
\text { s.t. } & \sum_{i=1}^{n} x_{i} g_{i} \leq \max G a s, \\
& x_{i} \in\{0,1\} \text { for } i=1, \ldots, n
\end{array}
\end{equation*}

> This is known as the Knapsack problem and is a NP-problem. In general, Ethereum nodes use a greedy approximation algorithm to obtain an approximation of the optimal solution.
> [source, https://youtu.be/WsrzWuA0xdo?t=157](https://youtu.be/WsrzWuA0xdo?t=157)

## Game Theory

### The Stage Game
A game is a tuple $G =(N, A, u)$ where:
- $N=\{1, \ldots, n\}$ is the set of players.
- $A=\prod_{i=1}^{n} A_{i}$, where $A_{i}$ denotes the set of actions for a player $i$.
- $u_{i}: A \rightarrow R$ is the utility function of a player $i$.
- Players want to maximize $u_{i}$ and take actions simultaneously.

### Strategy
A pure strategy can be thought as a plan subject to the observations they make during the course of the game of play. A mixed strategy is an assignment of a probability to each pure strategy.

### Nash equilibrium

A mixed strategy $s=\left(s_{1}, \ldots, s_{n}\right)$ is a Nash equilibrium if for every player $i$, and any strategy $\tilde{s}_{i}$, we have that
\begin{equation*}
u_{i}\left(s_{i}, s_{-i}\right) \geq u_{i}\left(\tilde{s}_{i}, s_{-i}\right)
\end{equation*}

### Theorem

#### Every game has a Nash equilibrium.


#### Example 2: L2 game
Game

Assume $N=\{1,2\}$ and $t=2$.
- $EV =$ The value that can be extracted if players know the content of txs per block.
- $CR =$ Commit and Reveal. If possible, slash the other player.
- RC $=$ Reveal and Commit. If possible, extract EV.
- $R =$ Reward per Block.
- $S =$ Slashing value s.t. $S >> EV$.


Problems and difficulties to cooperate
- Anonymous players.
- Unable to commit to future strategies.
- Economic incentives to deviate from commitment.
Conclusion on stage game cooperation
Hard to achieve consensus to cooperate.

#### What if games are played indefinitely?

##### Non-Myopic
Players are non-myopic if they are concerned for presents and future payoffs.
Given an infinite sequence of payoffs $r_{0}, r_{1}, r_{2}, \ldots$ for a player $i$ and a discount factor $\delta$ with $0 \leq \delta<1, i^{\prime}$ s future discounted reward is
\begin{equation*}
\sum_{i=0}^{\infty} \delta^{i} r_{i}
\end{equation*}
Intuition on discount factor:
- The agent values about near term profits than future profits.
- The discount factor models the players' patience.

\begin{equation*}
    \sum_{i=0}^{\infty} \delta^{i} r_{i}
    \end{equation*}


### Repeated game

#### Repeated games
The stage game is played indefinitely many times. Players can observe past actions. All player: share the same discount factor $\delta$.
Player's utility
Let $x_{t}$ be the tuple of actions played at round $t$, then the utility of a player $i$ with discount factor $\delta$ is:
\begin{equation*}
U_{i}=\sum_{t=0}^{\infty} \delta^{t} u_{i}\left(x_{t}\right)
\end{equation*}

### Folk theorem with perfect monitoring

#### Folk Theorem

Let $G$ be any $n$-player game.
- For all strictly pure-action individually rational action profiles ã, that is, $u_{i}(\tilde{a})>\operatorname{minmax}_{i}$ for all $i$, there is a $\bar{\delta} \in(0,1)$ such that for every $\delta \in(\bar{\delta}, 1)$, there exists a subgame-perfect equilibrium of the infinitely repeated game with discount factor $\delta$ in which $\tilde{a}$ is played in every period.
- For all feasible tuple $v$, there is a $\bar{\delta} \in(0,1)$ such that for every $\delta \in(\bar{\delta}, 1)$, there exists a subgame-perfect equilibrium, with payoff $v$, of the infinitely repeated game with public correlation and discount factor $\delta$.


#### Example 1: Arbitrage competition and the Folk theorem
Since $(50 \,/\ 50 )$ is a feasible payoff, we have by Folk theorem that, if both players are enough patient (for $\delta \geq 2 / 3$ holds), there exists a Nash equilibrium $$\left(s_{1}, s_{2}\right)$ such that $u_{i}\left(s_{1}, s_{2}\right)=50 \$$.
In these setting, we have that collision among searchers induce:
- $+$ profits for searchers,
- profits for miners.
compared to the stage game.

#### System performance

There exists Nash equilibrium that do not lead to egalitarian distribution of rewards.

> [source, https://youtu.be/WsrzWuA0xdo?t=924](https://youtu.be/WsrzWuA0xdo?t=924)



#### Example 2: L2 with Threshold decryption scheme

##### Repeated game: All for nothing
If players are enough patient $(\delta \approx 1)$, then there exists a Nash Equilibrium where both players, play the Reveal-Commit strategy and extract the MEV.
System performance
Since miners extract MEV from users, the users' revenue decreases compared to the myopic model.

> [source, https://youtu.be/WsrzWuA0xdo?t=966](https://youtu.be/WsrzWuA0xdo?t=966)


 
 
## Cobietron Article

Catagorize all trading pools into 4 major types such that it simplifies modeling. 


 
## Probabilistic thinking

> source: [https://cobie.substack.com/p/probabilistic-thinking](https://cobie.substack.com/p/probabilistic-thinking)

New entrants in the crypto community look to crypto “veterans” hoping for near-deterministic directional insight into these perplexing markets.

So, in this post, I will show you how to see the future.

**Seeing the future**

Successful crypto veterans know that crypto trading is a probabilistic outcomes business. Probabilistic thinking is basically just trying to estimate the likelihood of a specific future outcome becoming reality.

To my knowledge, seeing the future is currently impossible. Traders must instead predict the future by first seeing every possible future.

[![Doctor Strange travelled forward to look at 14,000,605 possible futures of  the conflict with Thanos. If he spent just one hour in each alternate future,  he spent roughly 1600 years studying the](https://cdn.substack.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F17065169-5513-4e10-abbe-10abbe9fe54a_979x547.jpeg "Doctor Strange travelled forward to look at 14,000,605 possible futures of  the conflict with Thanos. If he spent just one hour in each alternate future,  he spent roughly 1600 years studying the")](https://cdn.substack.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F17065169-5513-4e10-abbe-10abbe9fe54a_979x547.jpeg)

Oh, and none of this is investment advice. I’m not a professional and mostly am stumbling my way through the world the same way I was at age 13. Just documenting and sharing some thoughts and none of it is a science. I, like everyone else, am simply an aged baby walking blindfolded into a forest, startled by my own humanity.

Anyway, to illustrate with reality rather than a Marvel movie reference, let’s go back in time. Here’s what the 1D ETHUSD chart looked like at daily close on May 19th.

[![](https://cdn.substack.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F1e7e152c-209a-4bc0-924e-8d4214c57c9b_1150x710.png)](https://cdn.substack.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F1e7e152c-209a-4bc0-924e-8d4214c57c9b_1150x710.png)

When the market crashed in May, it took 8 days for Ethereum to go from around $4400 to below $1800.

During the crash, you could consider four possible scenarios for the future. I tweeted about them as we broke down below $2000.

[![](https://cdn.substack.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fa687147d-0393-418b-b622-071d315f5c20_1040x536.png)](https://cdn.substack.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fa687147d-0393-418b-b622-071d315f5c20_1040x536.png)

In case it helps, I have drawn some embarrassingly lo-fi versions of what the future charts might have looked like in each scenario.

**1\. The market has experienced another 2017-style boom/bust cycle and the top is in. We can expect a classic crypto “complacency shoulder” pattern.**

[![](https://cdn.substack.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F54785991-c41a-4129-8de6-3066865826f8_1864x668.png)](https://cdn.substack.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F54785991-c41a-4129-8de6-3066865826f8_1864x668.png)

**2\. The market will cool off before experiencing a 2013-style double-bubble and be bullish again towards the end of the year.**

[![](https://cdn.substack.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F42fe82bd-987c-4d36-ad13-3fbc8afc0fea_1784x668.png)](https://cdn.substack.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F42fe82bd-987c-4d36-ad13-3fbc8afc0fea_1784x668.png)

**3\. The market will go down-only and experience an almost unprecedented level of rekt.**

[![](https://cdn.substack.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fc75f1ea9-6b7d-49d0-9fbd-03bde314a8c8_1786x668.png)](https://cdn.substack.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fc75f1ea9-6b7d-49d0-9fbd-03bde314a8c8_1786x668.png)

**4\. The market will instantly recover and rocket to new highs very quickly.**

[![](https://cdn.substack.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F1550e305-2536-4574-b8b3-9730c8405eb0_1850x652.png)](https://cdn.substack.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F1550e305-2536-4574-b8b3-9730c8405eb0_1850x652.png)


There are of course slight variations of each idea above, as well as other potential scenarios that I didn’t bother considering because I thought they were too unlikely (eg. sideways forever).

After accounting for all the possible things that could happen, good traders will evaluate how likely they believe each scenario to be. At the bottom of the crash, they could be weighted something like this:

<pre>
p(1) = 45%

p(2) = 45%

p(3) = 5%

p(4) = 5%
</pre>

In effect, you believe scenario 1 and 2 are equally likely outcomes at 45% each and they are also the two most likely possible outcomes, but you are also considering that 3 and 4 may be possible too.

**If you evaluate the best possible trade for each scenario above, they are pretty simple:**

<pre>
1 — buy: buy the lows and sell the classic complacency shoulder pattern

2 — buy: buy the lows and hold for new highs

3 — sell: it’s going to actual zero

4 — buy: new highs by end of day, lfg
</pre>


## Notes on AMM Structure


### Examining the comovement between price and volume in liquidity pool returns


One of AMM’s most important divergences from traditional exchange is that it divides its market participants into two distinct roles: liquidity providers and traders. In a nutshell, the former deposits equal value of any pair of assets into the liquidity pool and the latter trades one for the other based on what’s available in the pool. This creates interesting ramifications in terms of risk for the liquidity providers. In this post, we study the characteristics of the price dynamics in Uniswap under the usual assumption that the prices of the underlying asset pair follow a drift-diffusion process. Note that the analysis assumes zero liquidity pool growth (other than due to transaction fees) and zero risk-free rate as well.

#### Uniswap Explained

Examine the liquidity pool composed of asset $A$ and $B$. For simplicity, let $a_t$ and $b_t$ denote the number of units of $A$ and $B$ available in the liquidity pool respectively. At any point in time, we have:

$$
a_t b_t = k
$$

This is known as the constant product formula. Since the liquidity pool must have equal value of both assets (one can arbitrage if it doesn’t!), it also implies that the current exchange rate of one unit of asset $A$ in terms asset $B$ is

$$
e_t = \frac{ A_t }{ B_t } = \frac{ b_t }{ a_t }
$$

where $A_t$ and $B_t$ are the unit prices of asset $A$ and $B$ measured in a common numeraire (be it Bitcoin or US dollar, your choice).

At time $0$, there are $a_0$ units of asset $A$ and $b_0$ units of asset $B$ in the pool. Now, if a new order comes along to buy $\Delta a_1$ units of asset $A$, after the transaction settles, the ending balances in the pool for asset $A$ and $B$ will be:

$$
a_1 = a_0 - \Delta a_1
$$

$$
b_1 = \frac{ k }{ a_0 - \Delta a_1 }
$$

This leads to a new exchange rate of:

$$
e_1 = \frac{ a_0 b_0 }{ (a_0 - \Delta a_1)^2 } = \frac{ a_0^2 }{ (a_0 - \Delta a_1)^2 } \cdot \frac{ b_0 }{ a_0 } > \frac{ b_0 }{ a_0 } = e_0
$$

which indicates that asset $A$ has appreciated against asset $B$, as a result of having fulfilled the demand for asset $A$ and the subsequent “scarcity” of it in the pool.

While the individual prices of asset $A$ and $B$ can still very much follow their own dynamics, Uniswap provides a way for traders to express their view on the price of one in terms of the other. In other words, everything is being valued on a relative term in the Uniswap exchange. This setup has a few desirable properties to it. Just to name a few:

-   if there’s no trade, the relative price level (i.e., exchange rate) stays at its initial value
-   a smaller trade is expected to be fulfilled at the market price of exchange without moving it too much
-   a larger trade will move the price substantially along the hyperbolic curve, with the asset in demand appreciating against the other
-   a very large trade (e.g., something close to the remaining balance in the pool) will lead to a price impact so prohibitively high that it is close to impossible to deplete the inventory.

In other words, Uniswap appears to achieve _infinite_ market depth with _finite_ supply of assets. Generally, the liquidity provider puts down:

$$
v_0 = a_0 A_0 + b_0 B_0
$$

amount of money (again, measured in an arbitrary numeraire) today in exchange for:

$$
v_t = a_t A_t + b_t B_t
$$

at time $t$. By contrast, a buy and hold strategy will have the following payoff at time $t$:

$$
v'_t = a_0 A_t + b_0 B_t
$$

## Price Slippage vs Fee Income

The payoff at time $t$ for liquidity providers can be further decomposed into two parts - capital appreciation (or depreciation) due to price slippage and income from collecting transaction fees.

One on hand, as trades fulfill, newly-arrived supply and demand drive the price away from its starting point. Formerly known as price slippage, this phenomenon can lead to either a gain or loss to the liquidity provider, but it always underperforms a buy and hold strategy (to see why, see the [appendix](#appendix)). To compensate for the underperformance, AMM usually charges a fee for trading. For example, Uniswap collects 0.3% on every transaction. The fees are put back to the pool right away and every liquidity provider has a pro rata claim on them. As it stands, fee income is effectively the sole incentive for liquidity providers to contribute assets into the pool, compared to simply holding on to the asset pair.

### The introduction of transaction fees brings _path dependence_ into the equation.
The introduction of transaction fees brings _path dependence_ into the equation. 

The terminal state alone is no longer sufficient to uniquely determine the payoff to liquidity provider - the path through which it arrives at the ending price also matters. This requires a slight modification to the constant production formula introduced earlier:

<img src="https://render.githubusercontent.com/render/math?math=a_t%20b_t%20%3D%20a_%7B%20t-1%20%7D%20b_%7B%20t-1%20%7D%20%2B%20f_t">

$$
a_t b_t = a_{ t-1 } b_{ t-1 } + f_t
$$

where $f_t$ is the amount of transaction fees collected at time $t$.

## Simulation Setup

Assume the prices of asset $A$ and $B$ follow the following dynamics:

<img src="https://render.githubusercontent.com/render/math?math=%5Cfrac%7B%20dA_t%20%7D%7B%20A_t%20%7D%20%3D%20%5Cmu%5EA%20dt%20%2B%20%5Csigma%5EA%20dW%5EA%20%5C%5C%0A%5Cfrac%7B%20dB_t%20%7D%7B%20B_t%20%7D%20%3D%20%5Cmu%5EB%20dt%20%2B%20%5Csigma%5EB%20dW%5EB%20%5C%5C">

$$
\frac{ dA_t }{ A_t } = \mu^A dt + \sigma^A dW^A \\
\frac{ dB_t }{ B_t } = \mu^B dt + \sigma^B dW^B \\
$$

where $dW^A$ and $dW^B$ are correlated Brownian motions:

<img src="https://render.githubusercontent.com/render/math?math=dW%5EA%20dW%5EB%20%3D%20%5Crho%20dt">
$$
dW^A dW^B = \rho dt
$$

Thanks to the explicit linkage between volume and price specified by the constant product formula, we have everything we need to back out the trading volume it takes to move the price by that much. Ignoring fees, the new price pair $A_t$ and $B_t$ defines how the balances of asset $A$ and $B$ evolve from the time $t-1$ to time $t$:

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bcases%7D%0A%5Cfrac%7B%20A_t%20%7D%7B%20B_t%20%7D%20%3D%20%5Cfrac%7B%20b'_t%20%7D%7B%20a'_t%20%7D%20%5C%5C%20%0Aa'_t%20b'_t%20%3D%20a_%7B%20t-1%20%7D%20b_%7B%20t-1%20%7D%20%5C%5C%0A%5Cend%7Bcases%7D">

$$
\begin{cases}
\frac{ A_t }{ B_t } = \frac{ b'_t }{ a'_t } \\ 
a'_t b'_t = a_{ t-1 } b_{ t-1 } \\
\end{cases}
$$

which yields:

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bcases%7D%0Aa'_t%20%3D%20%5Csqrt%7B%20%5Cfrac%7B%20a_%7B%20t-1%20%7D%20b_%7B%20t-1%20%7D%20A_t%20%7D%7B%20B_t%20%7D%20%7D%20%5C%5C%20%0Ab'_t%20%3D%20%5Csqrt%7B%20%5Cfrac%7B%20a_%7B%20t-1%20%7D%20b_%7B%20t-1%20%7D%20B_t%20%7D%7B%20A_t%20%7D%20%7D%20%5C%5C%0A%5Cend%7Bcases%7D">

$$
\begin{cases}
a'_t = \sqrt{ \frac{ a_{ t-1 } b_{ t-1 } A_t }{ B_t } } \\ 
b'_t = \sqrt{ \frac{ a_{ t-1 } b_{ t-1 } B_t }{ A_t } } \\
\end{cases}
$$

After taking transaction fees into consideration, we have the final form of remaining balances in the liquidity pool:

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bcases%7D%0Aa_t%20%3D%20a'_t%20%2B%20%5Ctextbf%7B%201%20%7D_%7B%20a_%7B%20t-1%20%7D%20%5Cgeq%20a'_t%20%7D%20(%20a_%7B%20t-1%20%7D%20-%20a'_t%20)%20c%20%5C%5C%20%0Ab_t%20%3D%20b'_t%20%2B%20%5Ctextbf%7B%201%20%7D_%7B%20a_%7B%20t-1%20%7D%20%3C%20a'_t%20%7D%20(%20b_%7B%20t-1%20%7D%20-%20b'_t%20)%20c%20%5C%5C%20%0A%5Cend%7Bcases%7D">

$$
\begin{cases}
a_t = a'_t + \textbf{ 1 }_{ a_{ t-1 } \geq a'_t } ( a_{ t-1 } - a'_t ) c \\ 
b_t = b'_t + \textbf{ 1 }_{ a_{ t-1 } < a'_t } ( b_{ t-1 } - b'_t ) c \\ 
\end{cases}
$$


where $c$ is the transaction fee rate and  $\textbf{ 1 }$  is the indicator function that takes the value of 1 if the underlying condition is true, or 0 if otherwise. Depending whether the order is to buy asset $A$ with asset $B$ or vice versa, transaction fees can either take the form of asset $A$ or $B$ before being put back to the liquidity pool. More specifically,

-   if $a_{ t-1 }$ is greater than $a’_t$, the trader must have purchased asset $A$ with asset $B$, resulting in a decline in the balance of asset $A$ and an increase in that of asset $B$. The protocol retains a portion of the payout (asset $A$) to the trader as transaction fees.

-   if $a_{ t-1 }$ is less than $a’_t$, the trader must have purchased asset $B$ with asset $A$, resulting in an decline in the balance of asset $B$ and an increase in that of asset $A$. The protocol retains a portion of the payout (asset $B$) to the trader as transaction fees.

## Putting It All Together

Under a set of arbitrarily-selected parameters, simulation results suggest that even after accounting for transaction fees, the buy and hold strategy still delivers a higher expected return after 1000 steps (transactions). However, acting as the liquidity provider significantly reduces the volatility due to the steady stream of fee income. It also outperforms buy and hold in terms of Sharpe ratio.


### How important is the correlation parameter? 

Liquidity provider benefits from a low correlation in at least two ways from a mean-variance optimization standpoint. 

- First, the lower the correlation is, the more the two assets’ prices tend to move in opposite directions. The higher level of divergence takes larger amount of trading volume to realize, which should translate into a higher fee income (despite more price slippage). 

- Secondly, a low correlation brings diversification so it’s expected to have lower volatility. All things considered, both expected return and volatility increases as correlation goes up while Sharpe ratio declines. In the extreme case, a correlation of 1 will result in very little price movement in relative terms, to the point where the return dynamics of liquidity provider behave very close to that of a buy and hold.


Last but not least, a higher transaction fee rate undoubtedly works in liquidity providers’ favor. All else equal, the higher the fee, the higher the return. Sharpe ratio also improves as the increase in expected return outpaces the increase in volatility.


# Appendix

### The Effect of Price Slippage

In the absence of transaction fees, compare the terminal values of the two following strategies:

-   strategy X: buy and hold
-   strategy Y: contribute to liquidity pool

Strategy X’s terminal value is given by:

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Balign%7D%0Av_t%5EX%20%26%3D%20(a_0%20e_t%20%2B%20b_0)%20B_t%20%5C%5C%0A%20%25%20%26%3D%20(a_0%20%5Cfrac%7B%20b_t%20%7D%7B%20a_t%20%7D%20%20%2B%20b_0)%20B_t%20%5C%5C%0A%20%25%20%26%3D%20(a_0%20%5Cfrac%7B%20%5Cfrac%7B%20k%20%7D%7B%20a_t%20%7D%20%7D%7B%20a_t%20%7D%20%2B%20b_0)%20B_t%20%5C%5C%0A%20%25%20%26%3D%20(a_0%20%5Cfrac%7B%20%5Cfrac%7B%20a_0%20b_0%20%7D%7B%20a_t%20%7D%20%7D%7B%20a_t%20%7D%20%2B%20b_0)%20B_t%20%5C%5C%0A%20%26%3D%20(%5Cfrac%7B%20a_0%20%5E%202%20%7D%7B%20a_t%5E2%20%7D%20%2B%201)%20b_0%20B_t%0A%5Cend%7Balign%7D">

$$
\begin{align}
v_t^X &= (a_0 e_t + b_0) B_t \\
 % &= (a_0 \frac{ b_t }{ a_t }  + b_0) B_t \\
 % &= (a_0 \frac{ \frac{ k }{ a_t } }{ a_t } + b_0) B_t \\
 % &= (a_0 \frac{ \frac{ a_0 b_0 }{ a_t } }{ a_t } + b_0) B_t \\
 &= (\frac{ a_0 ^ 2 }{ a_t^2 } + 1) b_0 B_t
\end{align}
$$

Meanwhile, strategy Y will have a terminal value of:

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Balign%7D%0Av_t%5EY%20%26%3D%20(a_t%20e_t%20%2B%20b_t)%20B_t%20%5C%5C%0A%20%25%20%26%3D%20(a_t%20%5Cfrac%7B%20b_t%20%7D%7B%20a_t%20%7D%20%2B%20b_t)%20B_t%20%5C%5C%0A%20%25%20%26%3D%202b_t%20B_t%20%5C%5C%0A%20%25%20%26%3D%202%20%5Cfrac%7B%20k%20B_t%20%7D%7B%20a_t%20%7D%20%5C%5C%0A%20%26%3D%20%5Cfrac%7B%202%20a_0%20b_0%20B_t%20%7D%7B%20a_t%20%7D%20%5C%5C%0A%5Cend%7Balign%7D">

$$
\begin{align}
v_t^Y &= (a_t e_t + b_t) B_t \\
 % &= (a_t \frac{ b_t }{ a_t } + b_t) B_t \\
 % &= 2b_t B_t \\
 % &= 2 \frac{ k B_t }{ a_t } \\
 &= \frac{ 2 a_0 b_0 B_t }{ a_t } \\
\end{align}
$$

Divide $v_t^X$ by $v_t^Y$,

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Balign%7D%0A%5Cfrac%7B%20v_t%5EX%20%7D%7B%20v_t%5EY%20%7D%20%26%3D%20%5Cfrac%7B%20%5Cfrac%7B%20a_0%20%5E%202%20%7D%7B%20a_t%5E2%20%7D%20%2B%201%20%7D%7B%20%5Cfrac%7B%202a_0%20%7D%7B%20a_t%20%7D%20%7D%20%5C%5C%0A%20%25%20%26%3D%20%5Cfrac%7B%20%5Cfrac%7B%20a_0%20%7D%7B%20a_t%20%7D%20%2B%20%5Cfrac%7B%20a_t%20%7D%7B%20a_0%20%7D%20%7D%7B%202%20%7D%20%5C%5C%0A%20%25%20%26%3D%20%5Cfrac%7B%20a_0%5E2%20%2B%20a_t%5E2%20%7D%7B%202%20a_0%20a_t%20%7D%20%5C%5C%0A%20%25%20%26%3D%20%5Cfrac%7B%20(a_0%20-%20a_t)%5E2%20%2B%202%20a_0%20a_t%20%7D%7B%202%20a_0%20a_t%20%7D%20%5C%5C%0A%20%26%3D%20%5Cfrac%7B%20(a_0%20-%20a_t)%5E2%20%7D%7B%202%20a_0%20a_t%20%7D%20%2B%201%20%5C%5C%0A%20%26%5Cgeq%201%0A%5Cend%7Balign%7D">

$$
\begin{align}
\frac{ v_t^X }{ v_t^Y } &= \frac{ \frac{ a_0 ^ 2 }{ a_t^2 } + 1 }{ \frac{ 2a_0 }{ a_t } } \\
 % &= \frac{ \frac{ a_0 }{ a_t } + \frac{ a_t }{ a_0 } }{ 2 } \\
 % &= \frac{ a_0^2 + a_t^2 }{ 2 a_0 a_t } \\
 % &= \frac{ (a_0 - a_t)^2 + 2 a_0 a_t }{ 2 a_0 a_t } \\
 &= \frac{ (a_0 - a_t)^2 }{ 2 a_0 a_t } + 1 \\
 &\geq 1
\end{align}
$$

As a result, a buy and hold strategy always outperforms being a liquidity provider in the absence of fee income.

### Expected Return and Volatility under the Baseline Setup

| Strategy | Expected Return | Volatility | Sharpe Ratio |
| --- | --- | --- | --- |
| Buy and Hold | 4.03 | 12.72 | 0.32 |
| Liquidity Provider | 2.88 | 5.56 | 0.52 |

### Expected Return and Volatility under Various Correlation Assumptions

| Strategy | Correlation | Expected Return | Volatility | Sharpe Ratio |
| --- | --- | --- | --- | --- |
| Liquidity Provider | \-0.5 | 1.86 | 2.23 | 0.83 |
| Liquidity Provider | 0 | 2.22 | 3.32 | 0.67 |
| Liquidity Provider | 0.5 | 2.63 | 4.67 | 0.56 |
| **Liquidity Provider** | **0.8** | **2.88** | **5.56** | **0.52** |
| Liquidity Provider | 0.9 | 2.98 | 5.96 | 0.50 |
| Liquidity Provider | 1 | 3.06 | 6.18 | 0.50 |

### Expected Return and Volatility under Various Fee Schedules

| Strategy | Fee | Expected Return | Volatility | Sharpe Ratio |
| --- | --- | --- | --- | --- |
| Liquidity Provider | 0% | 2.81 | 5.51 | 0.51 |
| Liquidity Provider | 0.15% | 2.84 | 5.51 | 0.52 |
| **Liquidity Provider** | **0.3%** | **2.88** | **5.56** | **0.52** |
| Liquidity Provider | 1% | 3.09 | 5.86 | 0.53 |
| Liquidity Provider | 5% | 4.48 | 7.91 | 0.57 |
| Liquidity Provider | 20% | 15.36 | 23.45 | 0.65 |

_**Bold** indicates baseline setup._
