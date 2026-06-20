# Quant Notebooks

Scratch notebooks used to write, test, and validate code for quant/time-series blog posts before it gets cleaned up and published.

## Structure

```
notebooks/
  arima/            notebooks for the ARIMA series (stationarity, ACF/PACF, AR/MA/ARIMA)
  cointegration/     notebooks for the upcoming cointegration/pairs trading series
```

Add a new folder per blog series/topic as needed.

## Setup

```bash
python3 -m venv venv
source venv/bin/activate        # on Windows: venv\Scripts\activate
pip install -r requirements.txt
```

## nbstripout

This repo uses [nbstripout](https://github.com/kynan/nbstripout) to strip notebook outputs before each commit, keeping diffs clean and avoiding bloated history from embedded plots/output. After cloning, run:

```bash
pip install nbstripout
nbstripout --install
```

This only needs to be run once per local clone — it installs a git filter that automatically strips output on `git add`/`commit`, without modifying what you see in Jupyter itself.
