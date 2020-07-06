# Generate .ics Calender file from scraped list of dates
### requirements
* sed
* awk
* bash

### download example page with calendar infos
 
```bash
$ wget example.com/calendar.html -O example.html
```
### example output for page where dates are after specific String
the string in this example is "Unterrichtsfreie Zeit - Zeitraum: "
```bash
$ cat example.html | sed -n -e 's/^.*Unterrichtsfreie Zeit - Zeitraum: //p' 
11.04.2020 - 10.04.2020
12.04.2020 - 13.04.2020
02.05.2020 - 01.05.2020
08.06.2020 - 08.07.2020
21.09.2020 - 22.09.2020
01.10.2020 - 01.10.2020
11.11.2020 - 12.11.2020
03.12.2020 - 14.12.2020
```
### change date format dd.mm.yyyy to yyyymmdd
```bash
| sed -E 's,([0-9]{2}).([0-9]{2}).([0-9]{4}),\3\2\1,g'
```
### echo in file dates.txt
```bash
> dates.txt
```
### all in one line
```
$ cat example.html | sed -n -e 's/^.*Unterrichtsfreie Zeit - Zeitraum: //p' | sed -E 's,([0-9]{2}).([0-9]{2}).([0-9]{4}),\3\2\1,g' > dates.txt
```
### download, make my_ics.sh script from my [/scripts](https://github.com/club-mate/scripts) repository executable and execute it in the same folder where dates.txt was generated before
```bash
$ wget https://raw.githubusercontent.com/club-mate/scripts/master/my_ics.sh
$ chmod +x my_ics.sh
$ ./my_ics.sh > my.ics
```
### know you should have your my.ics file for importing it in your calendar app
