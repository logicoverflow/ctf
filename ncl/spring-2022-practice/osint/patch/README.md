# Vulnerability Patch
> Medium (45 points)

## Challenge & Solution

**Cyber Command**

Old software leaves you vulnerable to attack. Figure out what software versions we should be running on the city network.

_Q1 - 15 points
On what day did Redhat push out a patch to address CVE-2017-6074 for their RHE Linux 7 kernel?_

https://access.redhat.com/security/cve/CVE-2017-6074

```February 22, 2017```

_Q2 - 15 points
What is the largest UTC time that can be encoded by software with the Y2K38 bug (round DOWN to the minute)?_

https://en.wikipedia.org/wiki/Year_2038_problem

```03:14:07 UTC on 19 January 2038```

_Q3 - 15 points
One of our developers is updating our software to make it more secure. They see the function, strcpy being called. What is one safe equivalent function (with a similar API/prototype) they could use to prevent a buffer overflow?_

https://www.synopsys.com/blogs/software-security/detect-prevent-and-mitigate-buffer-overflow-attacks/

```strlcpy```
