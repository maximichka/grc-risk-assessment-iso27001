# Meridian Lab Questions

*By Maxim Bondarchuk*

**1. Did any risks in your Risk Register match problems you found in your Control Assessment?**

Yes. RISK-005 and CTRL-003 connect because both relate to the same underlying issue: workers being able to access other employees' workstations and act on their behalf, putting patient privacy at risk and exposing the company to financial and legal trouble. Because this issue appeared in both the risk register and the control assessment, it isn't a risk that can be left unattended. One way to remediate the risk and control gap is to require all workers to log out of their workstation when stepping away and to enforce a screen lock after 15 minutes of inactivity. A stricter option would be a screen lock after 3–5 minutes, though that goes beyond what CAP-001 currently proposes.

**2. Did you assess controls involving an outside vendor, such as the EHR or billing company?**

Yes. Three of the ten controls involved vendors and their software. One was CTRL-005, which states that the EHR vendor is contractually required to encrypt Meridian's data at rest. I found that the vendor did not provide thorough evidence that the data is actually encrypted at rest. Assessing vendor controls is valuable because relying on a contract without evidence leaves gaps that can be exploited if they aren't addressed.

**3. Would another person's assessment look different because you made your own decisions about risks, findings, and fixes?**

Yes. My assessment reflects my own decisions about risks and their effects, shaped by my real-world experience. For example, RISK-005 describes employees sharing logged-in workstations, which can allow workers to act on behalf of others. In a previous job, I saw how this kind of shared access can be misused and cause real financial loss. Because I've seen how people can exploit this risk and the impact it can have on a company and its employees, I gave it a higher rating than someone without that experience might.

[Back to the project README](README.md)
