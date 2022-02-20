---
 title: What is SQL(Structured query language) injection.
 tags: [SQLi, App Security, Threats]
 style: fill
 color: info
 description: Hello Everyone, This blog will be deeply focusing on SQL(Structured query language) injection.
---


## Introduction
In this blog, I’ll explain what is SQL injection, and what are its types. We will also learn how to find different types of SQL injection vulnerabilities and also see the measures that can be taken to prevent SQL injection.

# What is Structured query language injection (SQLi)?

SQL Injection (SQLi) is a type of an [injection attack](https://www.ibm.com/docs/en/snips/4.6.0?topic=categories-injection-attacks) that makes it possible for an attacker to execute malicious SQL statements. These statements contain malicious payloads that control a database server behind the web application.
SQL injection attacks are one of the most ancient, powerful, and dangerous web application vulnerabilities.
<br>
OWASP (Open Web Application Security Project) organization lists injection attacks in their [OWASP Top 10](https://owasp.org/Top10/) 2021 document as the third (A3) threat to web application security.

<img src="/assets/images/sq1.png" alt="image" width="450" height="560">

## Impact of a successful SQL injection attack.

If an SQL injection attack is successfully done, attackers can use this attack to bypass application security measures by accessing the authentication and authorization of any web page or web application and fetching the data of the entire SQL database which may contain users' sensitive information.
Criminals use SQL injection vulnerability for gaining unauthorized access to any website or web application's personal data like customer information, personal data, organizational secrets, and more.

## Types of SQL injection

There are three types of SQL injection:
- In-band SQLi.
- Out-of-Band SQLi.
- Inferential SQLi (Blind SQLi).

Now let us explore these in detail,

<img src="/assets/images/sq2.png" alt="image" width="450" height="560">

### In-band SQLi.
In-band SQL Injection is the most common and easy-to-exploit SQL Injection attack. This SQL Injection occurs when an attacker is able to use the same communication channel to both launch the attack and gather results.

In-band SQLi is further divided into two types: Error-based SQLi and Union-based SQLi.

#### Error-based SQLi.
Error-based SQLi is a type of in-band SQL Injection technique that relies on error messages given by the database server in order to obtain information about the structure of the database. In some instances, error-based SQL injection alone is enough for an attacker to get into an entire database. Though the errors are very useful during the development phase of a web application, they should either be logged to a limited permission record or should be slowed down.

#### Union-based SQLi.
This SQL injection technique allows the UNION SQL operator to combine the results of two or more SELECT statements into a single result which is then returned as part of the HTTP response.

### Out-of-Band SQLi.
Out-of-band SQL Injection is mostly not very common because it depends on features that are being enabled on the database server which is being used by the web application. Out-of-band SQL Injection occurs when an attacker is not in the position to use the same channel to launch the attack and gather results.

Out-of-band techniques provide an attacker an alternative to inferential time-based techniques, especially if the server responses are not very stable making inferential time-based attacks unreliable.

### Inferential SQLi.
Unlike in-band SQLi, Inferential SQLi may take longer for an attacker to exploit. However, it is just as dangerous as any other type of SQL Injection. In an inferential SQLi attack, no data is actually transferred via the web application and the attacker would not be able to see the result of an attack. Instead, an attacker is able to rebuild the database structure by sending some payloads, observing the web application’s response and the resulting behavior of the database server.
There are two types of Inferential SQLi that are: Boolean-based (content-based) SQLi and Time-based SQLi.

#### Boolean-based (content-based) SQLi.
Boolean-based SQL injection is a type of attack that utilizes SQL to make the application deliver an altogether extraordinary outcome that is to a great extent reliant upon whether the question returns as a TRUE or a FALSE.
Depending upon the outcome, the remark in the HTTP response alters or remains unaltered. This allows an attacker to find whether the payload utilized gave valid info, despite the fact that no information from the database is returned.

#### Time-based Blind SQLi.

Time-based SQL Injection is an inferential SQL Injection technique that relies on sending an SQL query to the database which forces the database to wait for a specified amount of time (in seconds) before responding. The response time will indicate to the attacker whether the result of the query is TRUE or FALSE.
This attack is typically slow (especially on large databases) since an attacker would need to enumerate a database character by character.

## Methods To Detect SQL Injection Attacks.

The most common methods for detecting SQL injection attacks are:
- web framework.
- static analysis.
- dynamic analysis.
- machine learning technique. 

### Web Framework.
There are certain limitations to this method of detection. It can detect an SQL injection attack only when the SQL query from the hacker contains special characters. If the attack does not contain such a character, the method fails. 
The method works by filtering the special characters and identifying queries as SQL injection attacks. This is the basic method though it has been upgraded significantly with time. 

### Static Analysis.
In this method, the user input data are validated to reduce the chances of SQL injection attacks. It is not a true detection method because if a wicked input has the correct type of syntax, the results will fail to recognize the attack. Over the years, it has been improved with automated reasoning. It is based on the tautology (always true condition) concept. Therefore, SQL injection attacks except for a tautology cannot be identified.

### Dynamic Analysis. 
Dynamic analysis is an improved method over static analysis, and it can detect the vulnerabilities from SQL injection attacks. It works by collecting the SQL queries between the client and the application and between the application and the database. Then it analyzes the vulnerabilities, and it uses SQL injection attack codes to understand the vulnerability. It decides whether the attack is successful or not. It is widely used as no modification in the application is required as it can run independently. But the vulnerabilities need to be fixed manually. In fact, there are many who use static and dynamic analysis in combination for better detection. 

### Machine Learning Method.
The SQL queries are made to generate the parameters of detection. The runtime SQL queries are then compared to the generated ones. Depending on the quality of the generated parameters, most of the SQL injection attacks can be detected. There are also various others ways available such as using a crawler-based on machine learning method. This method is considered to be more effective than any other traditional detection and penetration testing. However, it cannot point out the vulnerabilities in the system. 

## Measures that can be taken to prevent SQL injection.

<img src="/assets/images/sq3.png" alt="image" width="450" height="560">

Here are some possible measures that can be taken to prevent an SQL injection attack from happening:

1. Do not use dynamic SQL - Try to avoid putting user-given input straight away to the SQL statements. Using a parameterized query and fetching users' data indirectly in your database would protect your system from SQLi. 
2. Do not leave sensitive credentials in plain text format - Try to keep all the sensitive data in your database's encrypted format. In case attackers gain access to your backend system through SQLi, they will not be able to exfiltrate a sensitive set of information.
3. Filter out user-provided inputs - You can smartly code your backend to escape out or filter out those characters which need to be escaped.
4. Provide restrictions or limitations in database permissions as well as in privileges - Access to the database should be at a minimum level as per requirement. Also, share the backend code with the least possible people.
5. Avoid displaying any database errors openly to the user - Some attackers also use these error messages to understand your database versions and type as well as some error messages showing the path of the database within the server. This will eventually bring down the morale of your web application's security.
6. You can also make use of Web application Firewalls to protect your database from SQLi attacks.
7. Keep your database systems and versions updated to the latest existing patches. This will eliminate the bugs, and hence, hackers will not be able to utilize those bugs to gain access to your database.

***NEXT BLOG WILL POSSIBLY BE ON sqlmap that is an open-source penetration testing tool that automates the process of detecting and exploiting SQL injection flaws and taking over database servers.***


THANK YOU FOR READING MY BLOG :)

