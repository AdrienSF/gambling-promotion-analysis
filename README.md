# An analysis of online gambling promotions

The basis is gambling is the following: any one individual may win, but on average in the long term the house always wins. I will be exploring how online casinos offer promotions while ensuring that this principle is never violated. A quick google query led me to find a few [types of online gambling promotions](https://www.vegasslotsonline.com/free-spins/).

## Free Spins Deposit Bonus
When the gambler makes a deposit, the casino gifts additional credit for free. Thanks to wagering requirements, this does not violate the basis of gambling: before cashing out, the gambler must bet M times more on casino games than the amount they started with. Let's construct a simple model:

Expectancy (mean payout/odds): $E(x) = qx$ where $0 < q < 1$, In other words when you bet x on average you will only win back qx.

To meet wagering requirements you need to bet repeatedly, but every bet leaves you with less to bet again with. The expected credit remaining after n bets is
$C(n) = xq^n$, and you want to reach a total spent of Mx credits.

Total spent credits: $S(n) = C(0) + C(1) + ... + C(n)$<br>
$$S(n) = x \sum_{i=0}^{n} q^{i}$$

As such, to earn anything you need to reach a number of n bets such that
$S(n) = Mx$ <br>
$$\Leftrightarrow x\sum_{i=0}^{n} q^{i} = Mx$$
$$\Leftrightarrow \sum_{i=0}^{n} q^{i} = M$$
But this is convergent if $|q| < 1$, $$\lim_{i\to\infty} \sum_{i=0}^{\infty} q^{i} = \frac{1}{1-q}$$

It now becomes obvious what casinos do: they simply choose q and M such that the series $$\sum_{i=0}^{\infty} q^{i}$$ is bounded from above by M.
With $M > \frac{1}{1-q}$ the average gambler never reaches the requirement to cash out ... unless they put in more money, making the promotion a success. This also means that we can deduce an upper bound for the odds if we know the wagering requirement M: rearrange $\frac{1}{1-q} < M <=> 1 - q > \frac{1}{M}$,  so $q < 1 - \frac{1}{M}$ and $E(x) < x(1 - \frac{1}{M})$. If you have to bet $M=3$ times the starting amount to cash out for instance, the odds are _at most_ $1- \frac{1}{3} = \frac{2}{3}$ for any game, or the casino would lose mmoney.

## Free Spins No Deposit Bonus
This type of promotion is identical to the previous, except that no deposit is needed. The same technique regarding the convergent series can be used here, meaning that the expected situation is one where the gambler will lose all the free credit before being able to cash out. There is an issue though: the gambler can never lose any money, but there is a chance they could win something. Indeed, if the gambler consistently beats the odds, the wagering requirement will be met and a net profit can be cashed out. The house never wins anything but the gambler could win something, meaning that on average the house actually loses. This is inconceivable. From the gambler's perspective, this is not very remarkable: taking advantage of the promotion gives them a small chance of winning something, most likely only a pitiful sum that's not really worth the time and effort. From the casino's perspective however, this is devastating: with thousands or even millions of people participating in the promotion, a good chunk of money is going to be reliably and undoubtedly lost. Perhaps the casino considers this loss a worthwhile investment in order to attract more customers? I doubt it. Instead, I believe that by adding constraints, the casino brings down the probability of the house losing anything to abysmal, egregiously small figures. In this case, the promotion will only cost the casino a fraction of a cent yearly.

Example of a constraint:
"If you have not made a deposit, there is a minimum withdrawal amount of £30" - [mrspin.co.uk](https://www.mrspin.co.uk/our-terms/terms-and-conditions/)<br>
<!--- [TODO]: find p s.t. P(can cash out) < arbitrary      If the casino gifts £5 initial credit, then it may choose P(can cash out) = --->
It's possible that reaching £30 after wagering requirements is so unbelievably unlikely as to be functionally impossible. Let's say for example that the probability of the event "gambler can withdraw" is 1/10^12. Then even if every living individual in the world took advantage of this promotion, the most likely outcome (by far) is that no one would win anything.

## Deposit Bonus + Free Spins
For this type of promotion, the same method used for the first promotion is effective: on average, the gambler is forced to lose their deposit before they can reach wagering requirements.

## Free Spins Promotions / Free Spin Prizes
These types of promotions are only available to regular users, meaning that the casino has already made a profit from the gambler, so it is clear that the principles of gambling are not violated.

