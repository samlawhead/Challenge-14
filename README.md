# Challenge-14

This is a very basic trading algorithm based upon a simple moving average strategy combined with a two machine learning models that backtest and evaulate it's performance for an Emerging Markets ETF. The first machine learning model is a Support Vector Classifier and the second uses an AdaBoost classifier. 

---

## Technologies

This project leverages python 3.7 with the following packages:

* [Pandas] (https://github.com/pandas-dev/pandas) - For data analysis
* [HvPlot] (https://github.com/holoviz/hvplot) - For visualization (charts and graphs) of the data
* [MatPlotLib] (https://github.com/matplotlib/matplotlib) - For plotting charts and graphs
* [NumPy] (https://github.com/numpy/numpy) - For running calculations
* [SciKit-Learn] (https://github.com/scikit-learn/scikit-learn) - For creating the machine learning models

## Installation Guide

Before running the application first install the following dependencies:

```python
   pip install pandas
   pip install numpy
   pip install hvplot
   pip install matplotlib
   pip install sklearn
```

---

## Usage

To use the model simply run the "main.ipynb" file in the terminal. The following images are screenshots showing the output with various different tuning parameters.

These are the results of the original parameters, the SVC classifier model with a 3 month training period, 4 day short window and 100 day long window.

<img src="https://github.com/samlawhead/Challenge-14/blob/main/CumReturnsActualvsStrategyv1.png" width=500 height=300>

There are the results of shortening the short window to 2 days. It results in better performance.

<img src="https://github.com/samlawhead/Challenge-14/blob/main/CumReturnsActualvsStrategy2shortwindows.png" width=500 height=300>

These are the results of increasing the short windows to 10 days. It results in worse performance.

<img src="https://github.com/samlawhead/Challenge-14/blob/main/CumReturnsActualvsStrategy10shortwindow.png" width=500 height=300>

These are the results of decreasing the long windows to 50 days. It results in worse performance.

<img src="https://github.com/samlawhead/Challenge-14/blob/main/CumReturnsActualvsStrategy50daylongwindow.png" width=500 height=300>

These are the results of increasing the long window to 120 days. It results in worse performance.

<img src="https://github.com/samlawhead/Challenge-14/blob/main/CumReturnsActualvsStrategy120daylong%20windows.png" width=500 height=300>

These are the results of decreasing the training period to 2 months. It results in better performance.

<img src="https://github.com/samlawhead/Challenge-14/blob/main/CumReturnsActualvsStrategy2moffset.png" width=500 height=300>

These are the results of increasing the training period to 4 months. It resulted in worse performance.

<img src="https://github.com/samlawhead/Challenge-14/blob/main/CumReturnsActualvsStrategy4%20m%20offset.png" width=500 height=300>

Below are the final results of the best model and tuning combination. The parameters included shortening the short window to 2 days, decreasing the training period to 2 months and utilizing the AdaBoost classifier. Its results are by far the best of any.

<img src="https://github.com/samlawhead/Challenge-14/blob/main/AdaboostStrategy.png" width=500 height=300>

---

## Contributors

Brought to you by Sam "Big Dog" Lawhead. 

---

## License

Copyright 2022

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
