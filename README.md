# What is this?
This is a small Python script that will retrieve official currecy exchange rates from the Bank of Lithuania, which you can also manually retrieve [here](https://www.lb.lt/lt/pagal-buhalterines-apskaitos-istatyma-formuojami-euro-ir-uzsienio-valiutu-santykiai). At the moment, it returns USD/EUR rate.

# Running the tool
## Install dependencies
```
$ virtualenv env
$ source env/bin/activate
$ pip install -r requirements.txt
```
## Execute
The script takes the list of dates (separated by new line) in the format of `YYYY-MM-dd`. They can either be read from stdin
```
$ echo "2020-05-20
2020-03-01
2020-01-01
2018-03-22" | python main.py
```
or you can pass a file name with dates as the first argument
```
python main.py /tmp/dates
```
The script will then write exchange rates in the same order to stdout
```
0.913
0.911
0.890
0.814
```
