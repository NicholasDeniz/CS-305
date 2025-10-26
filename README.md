# CS-305
# Nicholas Deniz
# Project 2 

"Briefly summarize your client, Artemis Financial, and its software requirements. Who was the client? What issue did the company want you to address?"

The client, Artemis Financial, develops financial plans for their customers. Financial plans including retirement, savings, insurance, and investments. They sought out Global Rain, who creates custom software design and development, to protect their client's data and financial information. As apart of their agile scrum team I was tasked with meeting Artemis's security requirements. They wanted to add a file verification step to its web application to ensure secure communications. So that when data is transferred a data verification step in the form of a checksum would be needed.

"What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?"

I used OWASP to run a dependency scan and reported multiple critical/high CVEs like Spring Framework, Tomcat, Hibernate Validator, Logback, and Jackson. I then saw unsecure coding practices like a broad catch, Exception, and a leak of data in the exceptions info. I then provided a mitigation plan to upgrade to a supported Spring Boot line and patched versions. Also, to practice secure coding when dealing with the exception catch and provide more generic message that don't give out internal information. It is important to code securely because it can prevent leaks in data, make code reliable, and keep to compliance. Also, it increases trust in the brand which is quite important in the finance industry as customers wouldn't want a unsecure company to have their personal data. 

"Which part of the vulnerability assessment was challenging or helpful to you?"

The part of the vulnerability assessment that was the most challenging was going throught the CVE list and finding out the optimal way to fix them. It can be difficult going trough all these CVEs and understanding each one of them to a point where you can offer aid. Especially as most of them were outdated. What was most helpful to me was understanding that issue and building a solid mitigation plan that would help fix those issues. The mitigation plan was to upgrade to a supported Spring Boot line and patched versions. It was helpful to learn to analyze Maven dependency reports and to understand CVE information.

"How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?"

I increased layers of security by strengthening transport security with TLS, only HTTPS. I also used the mainstream SHA-256 hash for integrity, made a note that internal information shouldn't be leaked in the source and configuration, and proposed a safe way of handling errors and input validation. In the future I would make sure BOM is kept up to date, run OWASP dependency checks frequently, use SAST, review code, and keep to OWASP ASVS to help in making secure decisions.  

"How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?"

I confirmed it functioned by testing the HTTPS endpoint https://localhost:8443/hash. I made sure it was functional by checking that the HTTPS endpoint had the specific fields expected, name, unique data, and the SHA-256 digest. Also, that the certificate was shown. From the security side how things I made sure TLS was active and checked there were no build/runtime errors. I rescanned the dependency check and confirmed what was expected, that there were no new vulnerabilities. In the future I would use static testing and penetration testing to make sure that there were no new vulnerabilities. 

"What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?"

I used OWASP Dependency Check Maven, Java keytool, and Spring Boot tools that were helpful in completing the assignment. Good practices would be validating input, using SHA-256 hash (especially for integrity), storing keys, and generic error messages to avoid info leaks. These practices should always be employed in future tasks to keep a good level of security development as anything less would lead to bad results. 

"Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?"

This assignment is proof that I understand how to analyze and identify vulnerabilities, employ secure communication using HTTPS and TLS, and follow industry level standards that are set by NIST and OWASP. The project also shows experince in forming mitigation plans, and with cryptographic practices. These are useful skills in cybersecurity and software engineering. 
