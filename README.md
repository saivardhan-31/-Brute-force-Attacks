# -Brute-force-Attacks
This project demonstrates brute-force attacks on vulnerable login systems using Burp Suite Intruder and Hydra, analyzing weak authentication mechanisms and implementing mitigation techniques in a controlled lab environment.

# Brute-force Attacks Project

## Objective
To analyze and perform brute-force attacks against web applications and study the impact of weak passwords, lack of rate limiting, and insecure login mechanisms.

## Lab Environment
- Kali Linux
- bWAPP / DVWA
- Burp Suite
- Hydra
- Wordlists (usernames & passwords)

## Lab 1: Burp Suite Intruder (Cluster Bomb)
- Intercepted login request via Burp Proxy
- Sent request to Intruder
- Configured Cluster Bomb attack type
- Set payload positions for username and password
- Analyzed response length and status codes to identify valid credentials

## Lab 2: Hydra Web Form Brute-force
- Identified login form fields and action URL
- Used Hydra to automate brute-force attack on login page
- Monitored output to detect successful login credentials

### Sample Command
- hydra -l admin -P passwords.txt <target-ip> http-post-form "/login.php:login=^USER^&password=^PASS^:Invalid"

## Tools Used
- Burp Suite (Proxy & Intruder)
- Hydra
- Kali Linux Terminal
- Web Browser

## Key Learning Outcomes
- Practical understanding of brute-force attacks
- Credential discovery using automated tools
- Analysis of server responses
- Security weaknesses in authentication systems

## Mitigation Strategies
- Strong password policies
- Account lockout and rate limiting
- CAPTCHA implementation
- Multi-Factor Authentication (MFA)
- Monitoring and logging failed login attempts

## Ethical Note
All testing was conducted in a legal lab environment (DVWA/bWAPP) for educational and ethical hacking purposes only.

## Conclusion
This project demonstrates how brute-force attacks can break weak authentication systems and highlights the importance of implementing strong security controls to protect login mechanisms.


