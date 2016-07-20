# of7dse

## Data sources
### Spin
Get the data by:

1. going to the app: http://spin.sos112.si/spin2/javno/
2. selecting only "car accidents"
3. turning on developement console with network monitoring
4. copying GET request url from developement console
5. replacing the day parameter and setting it to 100000, which gives data for more than 10 previous years (11.42)

## Exploratory analysis
* Count the number of car accidents by years:
`for i in {2000..2017} ; do printf $i'\t'; cat ../data/spin.csv | awk '$2 ~ /'$i'/' | wc -l; done`
