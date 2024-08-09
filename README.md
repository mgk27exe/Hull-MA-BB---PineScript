# Hull-MA-BB---PineScript

This script is written in Pine Script, which is used to create custom indicators and strategies on the TradingView platform. Below is a detailed breakdown of the script's functionality:

Overview:
Script Purpose: The script appears to be a custom indicator that combines multiple technical analysis tools such as the Hull Moving Average (HMA), Bollinger Bands (BB), and Volume Weighted Average Price (VWAP). It also includes alerts for potential trading signals.
Licensing: The script is under the Mozilla Public License 2.0, while parts of it (Moving Average 3.0 script) are licensed under the MIT license by Alex Orekhov.

Inputs:
Length Inputs: The script uses two lengths (length1 and length2) for different moving averages.
MA Type: The user can choose between different types of moving averages (EMA, SMA, VWMA, WMA).
Source: The input source for the moving averages, typically based on price data like hl2 (average of high and low prices).
VWAP and Bollinger Bands: Parameters such as VWAP length, source, offset, and standard deviation for Bollinger Bands can be adjusted.

Functions:
getMA(): A helper function that returns the chosen moving average type based on user input.
getNMA(): A function to calculate a custom normalized moving average (NMA) using two different moving averages.
hma(): Calculates the Hull Moving Average, which is a faster and smoother moving average designed to reduce lag.
hma3(): A modified version of the HMA calculation with additional smoothing.
kahlman(): Implements a Kahlman filter, which is used for smoothing and predicting the trend.

Plots:
NMA Plot: The script plots the normalized moving average (NMA) as a yellow line on the chart.
VWAP Plot: The middle VWAP line is plotted in pink with its length determined by the user input.
Bollinger Bands: The script plots the upper and lower Bollinger Bands along with a baseline.
Hull Trend with Kahlman: It plots long and short signals based on the Hull Moving Average, optionally smoothed by the Kahlman filter. These plots are color-coded (lime for uptrend, red for downtrend), and crossover points are marked with shapes on the chart.

Alerts:
Alert Conditions: The script includes alerts for when the long or short crossover occurs, allowing users to be notified when certain conditions are met.

Summary:
This script is designed to be a comprehensive tool for traders who want to combine various moving averages, Bollinger Bands, and VWAP to analyze market trends. It also incorporates a Kahlman filter for additional trend smoothing and generates alerts for potential trade entries (long or short positions). The customization options for moving averages, source data, and alert conditions make it a versatile tool for different trading strategies.
