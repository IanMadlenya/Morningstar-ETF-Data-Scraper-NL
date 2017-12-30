# Basic tool for (gently) scraping ETF data (across exchanges) from the Dutch [Morningstar](http://tools.morningstar.nl/nl/etfquickrank/default.aspx?Site=NL&Universe=ETALL%24%24ALL&LanguageId=nl-NL) ETF Quickrank / Database .

Please note:

- scraping this website is only allowed for personal use (as per Morningstar's Terms and Conditions).
- this tool is structured in a such a way that it gently / ethically scrapes the pages it encounters (in other words, scraping data might take a bit longer given the couple of "sleep" intervals embedded in the code)
- you will have to point the browser variable to the local path of your webdriver
- though this scraper has specifically been built for the Dutch Morningstar website, it enables one to extract data from multiple non-NL universes (e.g. ETFs listed on the Xetra, Nasdaq etc)

This tool has been written by means of [Python 3.5.1](https://www.python.org/downloads/release/python-351/), [Selenium 3.4.3](https://pypi.python.org/pypi/selenium) and [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/).

Example of the resulting dataframe one might expect:

```
    TER   close                                               link  \
0  0,15   39,34  http://www.morningstar.nl/nl/etf/snapshot/snap...
1  0,65   32,04  http://www.morningstar.nl/nl/etf/snapshot/snap...
2  0,20  162,08  http://www.morningstar.nl/nl/etf/snapshot/snap...
3  0,20  144,45  http://www.morningstar.nl/nl/etf/snapshot/snap...
4  0,20  210,06  http://www.morningstar.nl/nl/etf/snapshot/snap...

                                                name  \
0               Amundi ETF S&P 500 UCITS ETF USD EUR
1  First Trust Eurozone AlphaDEX® UCITS ETF Class...
2  iShares $ Treasury Bond 7-10yr UCITS ETF USD (...
3     iShares € Govt Bond 1-3yr UCITS ETF EUR (Dist)
4    iShares € Govt Bond 7-10yr UCITS ETF EUR (Dist)

                                        stars
0  http://tools.morningstar.nl/img/5stars.gif
1  http://tools.morningstar.nl/img/5stars.gif
2  http://tools.morningstar.nl/img/5stars.gif
3  http://tools.morningstar.nl/img/5stars.gif
4  http://tools.morningstar.nl/img/5stars.gif

```
