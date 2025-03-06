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
  - **volume:** the number of options contracts bought
  - **open:** the price of the contract when the market opens
  - **close:** the price of the contract when the market closes
  - **high:** the highest price for the option contract on the given day
  - **low:** the lowest price for the option contract on the given day
  - **window_start:** the time in unix ns the transation was executed at

# Quarterly Earnings Dates and Reports
## Q1 2024: Reported April 30th, 2024
### EPS
| Expected | Reported | Suprise |
|----------|----------|---------|
| 0.83     | 0.98     | 18.12%  |

### Revenue
| Expected | Reported | Suprise |
|----------|----------|---------|
| 142.56B  | 143.31B  | 0.53%   |

## Q2 2024: Reported on August 1st, 2024
### EPS
| Expected | Reported | Suprise |
|----------|----------|---------|
| 1.02     | 1.26     | 23.76%  |

### Revenue
| Expected | Reported | Suprise |
|----------|----------|---------|
| 148.76B  | 147.98B  | -0.52%  |

## Q3 2024: Reported on October 31st, 2024
### EPS
| Expected | Reported | Suprise |
|----------|----------|---------|
| 1.14     | 1.43     | 25.22%  |

### Revenue
| Expected | Reported | Suprise |
|----------|----------|---------|
| 157.28B  | 158.88B  | 1.01%   |

## Q4 2024, February 6th, 2024
### EPS
| Expected | Reported | Suprise |
|----------|----------|---------|
| 1.48     | 1.86     | 25.29%  |

### Revenue
| Expected | Reported | Suprise |
|----------|----------|---------|
| 187.23B  | 187.79B  | 0.30%   |

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

## Does the magnitude of IV crush vary across different earnings periods, and can we predict it based on historical patterns?
### Key Findings
  - **IV Crush Varies by Quarter:**
    - Q1 and Q3 experience a 22% decrease in IV post-earnings, indicating higher uncertainty leading into these reports
    - Q2 and Q4 shows a smaller 6% drop in IV, suggesting lower implied risk or uncertainty surrounding earnings
  - **Earning Suprise Consitency:**
    - The Earnings Per Share (EPS) suprise remains relatively stable across all quarters, ranging from 18-25%
    - However, revenue suprises exhibit more variation, whihc may help explain difference in IV crush
  - **Potential Correlation Between Revenue Suprise and IV Crush:**
    - Q2 and Q4 have the lowest revenue suprises (-0.52% and 0.30%), which aligns with the smallest IV crush (6%) post-earnings not fall as sharply as post-earnings
    - This suggests that when revenue results are more predictable, IV does not rise as aggressibely pre-earnings and does
![Screenshot 2025-03-06 at 11 56 40 AM](https://github.com/user-attachments/assets/e61c6ba5-12b5-41c9-9562-a6dcc530dbae)



