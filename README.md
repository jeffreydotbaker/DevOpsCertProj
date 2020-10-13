# DevOpsCertProj
Edureka DevOps Certification Final Project
==========================================
This project simulates a CI/CD workflow allowing the developers to continually update and test code.
In order to test pipeline, a workflow is developed as follows:
A string " Jeffrey baker" is added to the "About Us" page. The testing mechanism must find this string
on a newly configured / updated Test environment

WorkFlow
--------
1. Changes are mage to "about Us" page -> "Jeffrey Baker"
2. The Updated local repo is pushed to the remote git repository
3. Jenkins polls the SCM endpoint via cron and noticies that changes are made
4. A test server IP 192.168.56.105 is configured with the new docker images, containers and updated website
   via Ansible plugin
5. A Selenium test script checks a) that "About Us" is clickable b) searches for the string "Jeffrey Baker" 
   on the webpage
6. Pipeline fails if string is not found
