# Rossmann Store Sales

## Data Exploration
### `train.csv`
#### Column information
|column name|data type|explanation|remark|
|---|---|---|---|
|Store|int64|a unique Id for each store|
|DayOfWeek|int64|the number of the weekday|
|Date|object|string of the date|
|Sales|int64|the turnover for any given day|
|Customers|int64|the number of customers on a given day|             
|Open|int64|an indicator for whether the store was open|0 = closed, 1 = open|             
|Promo|int64|indicates whether a store is running a promo on that day|
|StateHoliday|object|indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. |Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None|
|SchoolHoliday|int64|indicates if the record was affected by the closure of public schools|

* Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None

#### Data Cleaning
* There is no `null` records

### `store.csv`
#### Column information
|column name|data type|explanation|remark|
|---|---|---|---|
|Store|int64|a unique Id for each store||
|StoreType|object|differentiates between 4 different store models|a, b, c, d|
|Assortment|object|describes an assortment level|a = basic, b = extra, c = extended|
|CompetitionDistance|float64|distance in meters to the nearest competitor store||
|CompetitionOpenSinceMonth|float64|gives the approximate month of the time the nearest competitor was opened|             
|CompetitionOpenSinceYear|float64|gives the approximate year of the time the nearest competitor was opened|             
|Promo2|int64| a continuing and consecutive promotion for some stores|0 = store is not participating, 1 = store is participating|
|Promo2SinceWeek|float64|describes the calendar week when the store started participating in Promo2|
|Promo2SinceYear|float64|describes the year when the store started participating in Promo2|
|PromoInterval|object|describes the consecutive intervals Promo2 is started, naming the months the promotion is started|E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store|

### `test.csv`
* The columns are
`Store`,`DayOfWeek`,`Date`,`Open`,`Promo`,`StateHoliday`,`SchoolHoliday`
* The meanings of these columns are explained in above sections.
