# 学习笔记之Quant

* [Quants: What They Do and How They've Evolved](https://www.investopedia.com/articles/active-trading/111214/quants-what-they-do-and-how-theyve-evolved.asp#:~:text=Key%20Takeaways-,Quantitative%20trading%20(also%20called%20quant%20trading)%20involves%20the%20use%20of,aim%20to%20identify%20profit%20opportunities.)
* [Beginner's Guide to Quantitative Trading | QuantStart](https://www.quantstart.com/articles/Beginners-Guide-to-Quantitative-Trading/)
* [Self-Study Plan for Becoming a Quantitative Developer | QuantStart](https://www.quantstart.com/articles/Self-Study-Plan-for-Becoming-a-Quantitative-Developer/)
* [A Simple Guide to Become a Quantitative Developer](https://blog.quantinsti.com/quantitative-developer/) 

## [HFT](https://en.wikipedia.org/wiki/High-frequency_trading)

* High-frequency trading (HFT) is a type of algorithmic financial trading characterized by high speeds, high turnover rates, and high order-to-trade ratios that leverages high-frequency financial data and electronic trading tools.[1] While there is no single definition of HFT, among its key attributes are highly sophisticated algorithms, co-location, and very short-term investment horizons.[2] HFT can be viewed as a primary form of algorithmic trading in finance.[3][4] Specifically, it is the use of sophisticated technological tools and computer algorithms to rapidly trade securities.[5][6][7] HFT uses proprietary trading strategies carried out by computers to move in and out of positions in seconds or fractions of a second.[8]
* [High-Frequency Trading (HFT) Definition](https://www.investopedia.com/terms/h/high-frequency-trading.asp)
* [Low latency (capital markets) - Wikipedia](https://en.wikipedia.org/wiki/Low_latency_(capital_markets))
  * In capital markets, low latency is the use of algorithmic trading to react to market events faster than the competition to increase profitability of trades. For example, when executing arbitrage strategies the opportunity to "arb" the market may only present itself for a few milliseconds before parity is achieved. To demonstrate the value that clients put on latency, in 2007 a large global investment bank has stated that every millisecond lost results in $100m per annum in lost opportunity.[1]
  * What is considered "low" is therefore relative but also a self-fulfilling prophecy. Many organisations and companies are using the words "ultra low latency" to describe latencies of under 1 millisecond, but it is an evolving definition, with the amount of time considered "low" ever-shrinking.
  * There are many technical factors which impact on the time it takes a trading system to detect an opportunity and to successfully exploit that opportunity. Firms engaged in low latency trading are willing to invest considerable effort and resources to increase the speed of their trading technology as the gains can be significant. This is often done in the context of high-frequency trading.
* [What I’ve learned after coding for HFT and Low Latency Systems | LinkedIn](https://www.linkedin.com/pulse/what-ive-learned-after-coding-hft-low-latency-systems-ariel/)
  * Choose the right language
  * Keep it all in memory
  * Keep your hardware underutilized
  * Keep context switches to a minimum
  * Keep your reads sequential
  * Non blocking as much as possible
  * Async as much as possible
  * Parallelize as much as possible
