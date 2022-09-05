# Online Driving School Project In PHP Sql Injection

The Online Driving School Project is a simple mini project for driving institutes. The project contains admin, learners, and users. The user can either be police or victims/complainers. This project is for the institute of driver training first commenced its operations in managing the learners and people who want to take a good learners school as well as the admin which means the owner of the web application can select the best and near learners to the people and connect them both.

project link: https://code-projects.org/online-driving-school-project-in-php-with-source-code/



SQL injection vulnerability exists in /login.php. The username and password parameters are exploitable . Attackers can exploit this vulnerability to execute arbitrary SQL statements and get the admin privilege.



![](https://s2.loli.net/2022/09/05/A3Js5L82rUz9oca.png)



# POC

with `username='or user_role='Admin'#&password=1` , the attacker can login as admin



![](https://s2.loli.net/2022/09/05/cQdrTCAeiF1JUHM.png)



and the attacker can exploit it using sqlmap

![](https://s2.loli.net/2022/09/05/EUbgCBORIPvx4uG.png)