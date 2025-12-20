# Stock-Jump-in-Small-Cap-Stocks (an-insights-into-it)
The stock jump in amll cap stocks is really a blank space in quant researching and many trader and strategists view the small cap stock trading has highly risky because jumps just happen randomly due to the fact that those stocks have really low valumes and any trade related to it will cause a high percentage change in stock price(which is jump)
The stock jump is also caused by many other factors like bid-ask-spread, which i will discuss later.

# Our work
I believe that the jump size and the jump frequency does not following a normal distribution or a Laplace Distribution even if we count in volatility terms, meaning that if we countin tiny jump, it is still not normal or laplace distribution. It follows a distribution, called Double Pareto-Lognormal (dPlN). This distribution correctly address many features or jump diffusion in small cap stocks, which includes having a long tail and the shape of it.
I will develop a mathematically rigorous framework for forecasting short-horizon price jumps in small-cap stocks. Modeling jumps as a state-dependent point process embedded in a jump-diffusion price system, we link jump arrival intensity to observable liquidity and market microstructure variables. We derive exact jump probabilities, construct likelihood-based estimators, and provide an extensible framework incorporating both Poisson and self-exciting jump dynamics. The model supports out-of-sample probability forecasting over short horizons and integrates naturally with modern machine learning for feature representation.
We will use stats tool to study the time interval between jumps and past jump sizes, so that we can have an insight into jumps in the near future. While I do not always believe that one jump will trigger a next series of jumps, I think that the jumps follow a martinglae property and characters of jumps in small cap stocks are largely unknown, unlike big cap stocks.

# Acknwledgement
This content is devoted by two parties: Simple Quantitative Trading Strategies:
<img width="1280" height="640" alt="logo2" src="https://github.com/user-attachments/assets/7483fa50-7f0d-4fea-b86f-1c92839a8d6d" />
And General Math Review led by Qingyang Fang:
<img width="1280" height="640" alt="logo2" src="https://github.com/user-attachments/assets/ee59d965-efd5-4bb0-b5c5-e1ab718d31a9" />

# Methodology
## Small Cap Stock's Jump Detection and Distribution Stats
This part is divided into Jump Detection and Jump stats part. While Lee-Mykland is more time changable comparing to other models, it is a perfect fit for Small-cap Stocks. I find that, after kicking small scale volatility out my the jump set, we get a dPIN Distribution. Here are my results:
<img width="998" height="733" alt="截屏2025-12-19 下午5 07 43" src="https://github.com/user-attachments/assets/54222eec-eab3-43ba-9bf6-118d62be305a" />
<img width="996" height="557" alt="截屏2025-12-19 下午5 07 21" src="https://github.com/user-attachments/assets/6115cc46-a5da-4895-be20-dee4daa3c4b4" />

## Jump Interval Detection and Distribution Stats
In this part, we identified the time interval between jumps, so that we can apply algorithms to "predict jumps", meaning that we can predict the expection of number of jumps happen in one near future time interval. Noted that the precision of expectation prediction decrease as time pass on. Here are my results:
<img width="1035" height="762" alt="截屏2025-12-19 下午5 49 32" src="https://github.com/user-attachments/assets/ade041cf-71e3-47ed-a280-16fee01abd36" />
<img width="1008" height="543" alt="截屏2025-12-19 下午5 42 57" src="https://github.com/user-attachments/assets/3e33a92f-7902-4817-93c9-f8429c367e05" />
