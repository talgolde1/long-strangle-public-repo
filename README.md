# Trading Algorithm Long Strangle

**Note: This project is private. Please refrain from sharing the code or any sensitive information about the project.**

This Python trading algorithm is designed to execute long strangle positions based on specific criteria and market conditions. The algorithm utilizes the Interactive Brokers (IBKR) API and the ib_insync library to fetch market data, execute trades, and monitor open positions and orders. Below, you'll find details on the algorithm's features, configuration, and usage.

## Features

1. **Market Data Retrieval**: The algorithm can fetch both historical and real-time market data from the Interactive Brokers Trader Workstation (TWS).

2. **Relative Volume Analysis**: It calculates relative volume and other technical indicators to make trading decisions.

3. **Long Strangle Strategy**: The algorithm focuses on executing long strangle positions when specific criteria are met. A long strangle involves buying both a call option and a put option with the same expiration date but different strike prices.

4. **Risk Management**: The algorithm includes risk management features, such as monitoring position P&L and adjusting position size.

5. **Logging and Notifications**: It generates logs and notifications for monitoring and debugging.

## Long Strangle Strategy

The primary trading strategy implemented by this algorithm is the long-strangle strategy. When certain conditions are met, the algorithm creates a long strangle position. Here are the key aspects of this strategy:

- **Long Strangle Position**: A long strangle involves purchasing both a call and a put option with the same expiration date but different strike prices.
- **Volatility Profits**: This strategy aims to profit from significant price movements in the underlying asset. It doesn't depend on the market's direction but relies on volatility.
- **Risk Management**: The algorithm incorporates risk management to control position size and monitor unrealized profits, ensuring responsible trading practices.

![Long Strangle](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Long_strangle_option.svg/1920px-Long_strangle_option.svg.png)

there are several advantages to the following strategy which are: 

- **Profit from Volatility** Long strangles are designed to profit from significant price movements in the underlying asset, regardless of its direction. This strategy benefits from increased volatility as it can lead to larger price swings, potentially resulting in substantial gains.
- **Market-Neutral** Long strangles are market-neutral strategies, meaning they can make a profit whether the market goes up or down significantly. This flexibility makes them suitable for uncertain or unpredictable market conditions.
- **Limited Risk** Unlike some other options strategies, long strangles have limited risk. The maximum loss is limited to the total premium paid for both the call and put options. This risk profile provides traders with a clear and predefined worst-case scenario.
- **Low Capital Requirement** Long strangles typically require less capital compared to buying the underlying asset itself. Traders can gain exposure to the price movements of the underlying asset at a fraction of the cost.
- **Higher Probability of Success** Long strangles have a higher probability of success compared to some other complex strategies. This is because they rely on the underlying asset making a significant move, which can happen more frequently in volatile markets.
- **Hedging Capabilities** Long strangles can be used as a form of portfolio insurance. If a trader has an existing position in the underlying asset and is concerned about a sudden price swing, they can use a long strangle to hedge against such a move.
- **Flexible Exit Strategies** Traders have flexibility in managing long strangle positions. They can choose to exit the entire position if they achieve their desired profit, or they can close out one leg of the strangle to adjust their exposure.

### Video Explanation
**[Long Strangle Video](https://www.youtube.com/watch?v=clhFk5Tp6E8)**

**Watch this YouTube video for an in-depth explanation of the long strangle strategy and how it can be applied in various market conditions.**


## Requirements

To run the algorithm, you'll need the following components:

- Interactive Brokers (IBKR) account with API access.
- IBKR Trader Workstation (TWS) installed and running.
- Python 3.7 or higher.
- ib_insync library installed (you can install it using `pip install ib_insync`).
- Other dependencies listed in the requirements.txt file.

## Configuration

Before running the algorithm, you should configure the following:

- IBKR API Connection: Specify the IP address and port of your TWS instance in the algorithm's configuration.
- Trading Strategy: Define your desired trading strategy by configuring the indicators, thresholds, and rules in the algorithm's code.
- Risk Management: Set risk parameters, such as maximum position size, maximum loss limits, and stop loss levels, to control the algorithm's behavior.

## Usage

Follow these steps to use the algorithm:

1. Clone the repository: `git clone https://github.com/your-username/long-strangle.git`

2. Install the required dependencies: `pip install -r requirements.txt`

3. Configure the algorithm: Update the configuration file with your IBKR API connection details and desired trading strategy.

4. Run the algorithm: Execute the main script using `python main.py`.

5. Monitor logs and notifications: Check the program's console output, log files, and any configured notification channels for updates on trades, positions, and errors.

6. Adjust parameters and strategy: Fine-tune the algorithm's settings based on performance analysis and your desired risk management approach.

**Note:** Make sure to add your Interactive Brokers account credentials to the TradingAlgorithm class before running the script.

## Running the Algorithm

To run the algorithm, create an instance of the `TradingAlgorithm` class and call its `run_algorithm` method, providing a list of stock symbols as input.

Example:

```python
if __name__ == "__main__":
    algorithm = TradingAlgorithm()
    algorithm.run_algorithm(symbol_list=["AAPL", "AMZN", "GOOGL", ...])
```

## Contact Information

For any inquiries or concerns regarding this code, please contact the project owner directly at talgolde1@gmail.com.

## License

- This code is provided for educational and informational purposes only. Use it at your own risk. Trading options involves financial risk, and past performance is not indicative of future results.
- This project is private, and all rights are reserved by the project owner. Unauthorized distribution or use of the code is strictly prohibited. This project is licensed under the [MIT License](LICENSE).

## Disclaimer

- This algorithm is provided for educational and informational purposes only. Use it at your own risk.
- Trading options involves financial risk, and past performance is not indicative of future results. Make sure to thoroughly understand the risks before engaging in real trading.
- The developer is not responsible for any losses or damages incurred as a result of using this algorithm.
