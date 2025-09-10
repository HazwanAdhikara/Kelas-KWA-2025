# Lab: SQL injection vulnerability allowing login bypass(PortSwigger)

This lab contains a SQL injection vulnerability in the login function.

To solve the lab, perform a SQL injection attack that logs in to the application as the administrator user.

## Steps

1. Akses labnya.
   <img src="./img/4-landingpage.png">

2. Modif parameter `username` dengan `administrator'--`
   <img src="./img/4-login.png">
   <img src="./img/4-success.png">
