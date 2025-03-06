# Amazon-Option-Analysis
[SQL | Python | Tableau]

# Analyzing Amazon Option Data Pre & Post Earnings for FY 2024
## Questions to be Asked:
  - **How does implied volatility (IV) behave before and after Amazon's earnings, and what does this mean for options traders?**
  - **Does the magnitude of IV crush vary across different earnings periods, and can we predict it based on historical patterns?**
  - **Which strike prices experience the highest changes in implied volatility around earnings?**
  - **How do call and put option volumes behave leading up to earnings and can they indicate market sentiment?**

# Data Collection:
The data was collected using Polygon.io's hisotircal option data aggregated by minute. This site is recognized globally and is trusted by major institutions including Google, Public, and Stanford.
![Screenshot 2025-03-05 at 1 49 05 PM](https://github.com/user-attachments/assets/1da7ab84-b3a4-4470-a495-63a31ccd2888)

 - **ticker:** The full option contract
   - Ex: O:SPY230327P00390000
     - O: indicated that this is an options contract
     - SPY: underlying asset or security for the option
     - 230327: represents the expiration date in YYMMDD format. The contract expires on March 27th, 2023 in this example
     - P: stands for a put option. Call options would have a C instead
     - 00390000: stands for the strike price of the option. In this contract the strike price is $390

# Data Analysis
## How does implied volatility (IV) behave before and after Amazon's earnings, and what does this mean for options traders?
### Key Findings
  - **Pre-Earnings IV:** The average Implied Volatility near Amazon's earnings reports is 38.48%
  - **Earnings IV:** On the day of earnings, IV spikes by approximately 25% to 48.19%
  - **Post-Earnings IV Crush:** IV decreases significantly after earnings, with drops ranging from 23% to 34%
  This IV behavior is a textbook example of an IV crush where option prices become inflated before earnings then deflate sharply after uncertainty resolves.

![Screenshot 2025-03-05 at 2 21 05 PM](https://github.com/user-attachments/assets/fd701f47-1b2b-4c0c-8960-78f3695cd276)

### Implications for Traders
**Strategies to Consider Pre-Earnings:**
  - **Buying Options:** Since IV is increasing rapidly leading up to earnings, traders might buy options early to benefit from the IV increase
  - **Long Straddle/Strangle:** Traders are expecting a big move in Amazon's (maybe unsure about direction) may buy both calls and puts. However, these positions must overcome the IV crush post-earnings
  - **Avoid Selling Options Too Early:** Since IV is rising, selling options too soon may leave money on the table

**Strategies for Earnings Day:**
  - **Selling High IV Premium:** Traders can capitilize on inflated option prices by selling options (covered calls, cash-secured puts, or iron condors). This takes advantage of IV peaking and the expected post-earnings IV crush.

**Strategies for Post-Earnings:**
  - **Buying Options at a Discount:** After IV Crush, options become cheaper. Traders expecting further volatility may find good entry points.
  - **Avoid Holding High IV Options Too Long:** If a trader holds options through earnings the IV drop may significantly reduce their value, even if the stock moves in their favor.
 
