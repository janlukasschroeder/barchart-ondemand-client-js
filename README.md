## Javascript client for Barchart OnDemand

A no dependency Javascript wrapper for Barchart OnDemand.

### Example Code

```javascript
var onDemand = new OnDemandClient();

onDemand.setAPIKey('change-me');
onDemand.setJsonP(true);

/* get a quote for AAPL and GOOG */
onDemand.getQuote({symbols: 'AAPL,GOOG'}, function (err, data) {
    if (err) {
        console.error(err);
    } else {
        var quotes = data.results;
        for (x in quotes) {
            console.log("getQuote: " + quotes[x].symbol + " [" + quotes[x].name + "] = " + JSON.stringify(quotes[x]));
        }
    }
});
```

### Supported APIs
#### Price Data
* getQuote
* getHistory
* getFuturesOptions
* getSpecialOptions
* getEquityOptions

#### Profiles and Financial Data
* getProfile
* getFinancialHighlights
* getFinancialRatios 
* getIncomeStatements 
* getCompetitors 
* getInsiders
* getRatings
* getIndexMembers

#### Splits, Dividends and Earnings
* getCorporateActions 
* getEarningsEstimates

#### Leaderboards and Lists
* getLeaders 
* getHighsLows 

#### Charts and Analytics
* getChart
* getTechnicals
* getSignal 
* getMomentum

#### News and Filings
* getNews
* getSECFilings

#### Meta Data
* getInstrumentDefinition 
* getFuturesSpecifications 
* getFuturesExpiration 
* getFuturesOptionsExpiration

#### Other
* getWeather
* getUSDAGrainPrices
