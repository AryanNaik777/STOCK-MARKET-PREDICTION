//@version=5
indicator("Simple Moving Average Crossover", overlay=true)

// User-defined inputs for moving averages
shortTermLength = input(9, title="Short-Term Moving Average Length")
longTermLength = input(21, title="Long-Term Moving Average Length")

// Calculate moving averages
shortMA = ta.sma(close, shortTermLength)
longMA = ta.sma(close, longTermLength)

// Plot moving averages
plot(shortMA, color=color.blue, title="Short-Term MA")
plot(longMA, color=color.red, title="Long-Term MA")

// Generate buy and sell signals
buySignal = ta.crossover(shortMA, longMA)
sellSignal = ta.crossunder(shortMA, longMA)

// Plot buy and sell signals on the chart
plotshape(buySignal, style=shape.labelup, location=location.belowbar, color=color.green, size=size.small, title="Buy Signal", text="BUY")
plotshape(sellSignal, style=shape.labeldown, location=location.abovebar, color=color.red, size=size.small, title="Sell Signal", text="SELL")

// Alerts
alertcondition(buySignal, title="Buy Alert", message="Buy Signal!")
alertcondition(sellSignal, title="Sell Alert", message="Sell Signal!")
