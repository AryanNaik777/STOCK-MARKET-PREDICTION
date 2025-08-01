Simple Moving Average (SMA) Crossover Strategy

This is a basic trading strategy implemented in Pine Script (//@version=5) that utilizes the crossover and crossunder of two Simple Moving Averages (SMAs) to generate buy and sell signals.

Features:
Two User-Defined SMAs: The script calculates a "short-term" and a "long-term" SMA based on user-defined lengths (defaulting to 9 and 21 periods, respectively).

Crossover Signals:

A buy signal is generated when the short-term SMA crosses above the long-term SMA.

A sell signal is generated when the short-term SMA crosses below the long-term SMA.

Visual Indicators:

The two moving averages are plotted directly on the chart for easy visualization.

Buy signals are marked with a green "BUY" label below the bar.

Sell signals are marked with a red "SELL" label above the bar.

Alerts: The script includes alertcondition functions to allow users to set up alerts for both buy and sell signals, enabling real-time notifications."
