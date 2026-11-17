# Meridian Health Partners: GRC Assessment Mapped to ISO/IEC 27001:2022

*Fictional portfolio simulation | Assessor: Maxim Bondarchuk*

> **Simulation disclosure:** Meridian is fictional. The evidence packet was AI-generated, including the interview excerpts, logs, and test records. This project is a selected-control assessment, not a certification audit of a real company.

## Results at a glance

| Assessment output | Current result |
| --- | --- |
| Risk Register | 8 risks: 3 High, 4 Medium, 1 Low before proposed treatment |
| Control Assessment | 10 controls: 2 Effective, 8 Partially Effective |
| Corrective Action Plans | 2 CAPs recorded as In Progress; fixes not yet verified |
| Framework mapping | All 10 controls mapped to selected ISO 27001 Annex A references |

## Project workflow

![Project workflow: company profile and evidence feed the Risk Register and Control Assessment, which lead to the CAP Tracker and future verification, with ISO 27001 Annex A mapping connecting controls to findings and actions](images/project_workflow.png)

The risk assessment, control review, and corrective action planning are documented. Implementing and verifying the fixes would happen next.

## 1. Project overview

Meridian Health Partners is a fictional company that features a 60-employee outpatient healthcare network with three physical clinic locations and a small central administrative office. An insurance contract listed for the company requires the company to conduct their first formal security assessment. And during the security assessment a risk register, control assessment, and a corrective action plan were created for the company to follow.

## 2. Scope and role

When it came to my role, I was assessing the company's security posture for the assessment from an outside perspective. When it came to reviewing the company's posture, I looked at various controls such as how the company handles access management, incident response, the contracts with their vendors, and security patching. Given that this assessment was done at an early stage, a verification was not conducted. This project is simulated and all the evidence is fictional.

## 3. Assessment approach

To identify risks, I considered the cause and the effect a risk would bring to the company. I then scored each risk by how likely it is to occur and the impact it would bring on the company on a 1-5 scale based on the company profile and simulated evidence. Next, I compared each stated control to the simulated evidence records, such as E02-A, which shows records of the HR and IT teams deprovisioning users and another example is E03-B, which shows how long it took for a workstation to lock when left unattended. A control was rated Effective if the control achieved its intended objective, with evidence supporting it, and a control was rated Partially Effective if the control operated with exceptions, inconsistencies, or weak evidence. From there, I chose CTRL-003 and CTRL-010 for corrective action because both tie directly to High risks in the risk register. CTRL-003 is the existing control for RISK-005, the highest-rated risk with a score of 20. CTRL-010 supports RISK-008, which scored 15 (High). Without an incident response plan that employees can actually find and follow, nobody would know what procedure to use to contain an issue when other controls fail. Finally, I mapped each control to ISO/IEC 27001:2022 Annex A to show which recognized security area each control falls under, making the assessment easier for readers to understand, though the mapping does not prove that Meridian complies with the standard.

### Scoring and ratings

Risk score = likelihood multiplied by impact. Low = 1-7, Medium = 8-14, High = 15-25.

Effective means evidence supports consistent operation. Partially Effective means there are exceptions or evidence gaps. Residual scores for proposed fixes are estimates, not verified reductions.

Likelihood was scored from 1 to 5 over a 12-month timeframe, where 1 means the likelihood of a risk occurring was rare, 2 for unlikely, 3 would indicate that the risk has a possibility of occurring, 4 is likely to occur, and 5 indicates almost certain to occur.

Impact was scored from 1 to 5 based on the effect of a certain risk occurring, where 1 means the impact of the risk was minimal, 2 would be viewed as an inconvenience, 3 would signify an average impact on the company, 4 would be critical for the company like patient data being exposed, and 5 would be severe like clinics having to shut down.

RISK-006 is the risk that employees retain company sensitive information after resigning and deprovisioning which can then harm the confidentiality of patients. It was rated a likelihood of 4 and an impact of 4, for a score of 16 (High). The likelihood is 4 because the company profile states that the employee turnover in front desk roles is high, averaging 40% annually. In addition, E02-A shows that 2 of the 6 employees were deprovisioned late and one wasn't deprovisioned at all, given the cutoff date. Impact is 4 because if this happened, patient information could be exposed, which could lead to HIPAA violations and lawsuits against the company.

CAP-001 was rated Medium severity because the workstation lock gap would not cause downtime, but it is a security misconfiguration that could be abused if not remediated, allowing employees to act on behalf of other employees. E03-B shows that 2 of the 6 sampled workstations were not configured correctly: one locked after 30 minutes, and one never locked.

CAP-002 was rated High severity because the incident response plan is restricted from most employees, and staff who don't know where the plan is could extend downtime for the company and clinics during an incident. E10-C shows that 2 of the 3 staff interviewed did not know where the plan was, and E10-A shows that the master copy is kept on a restricted Administration drive, with the only printed copy at the central office.

## 4. Key findings and business impact

### Finding one: Workstations not locking consistently

Meridian states that shared clinic workstations should automatically lock after 15 minutes of inactivity. However, E03-B shows that 2 of the 6 sampled workstations did not follow this setting: CL2-WS04 locked after 30 minutes, and CL3-WS06 never locked at all. E03-C explains why: CL2-WS04 is assigned to a Legacy Kiosk policy group with a 30-minute timeout, and CL3-WS06 was replaced in September but never had a lock policy assigned. This matters because an unlocked workstation lets employees act on behalf of others, which makes it hard to know who accessed patient records and could lead to HIPAA issues. To fix this, the company should implement a mandatory lock configuration so that all shared workstations lock after 15 minutes of inactivity.

*References: CTRL-003 | E03-B, E03-C | RISK-005 | CAP-001*

### Finding two: Incident response plan not accessible or maintained

Meridian states that it has a written incident response plan. However, E10-A shows the master copy is kept on a restricted Administration drive, with the only printed copy at the central office reception desk, so most staff can't easily reach it. E10-B shows the plan hasn't been maintained: the contact list hasn't been reviewed since February, the tabletop exercise was cancelled in May, and the after-hours contact still points to the MSP Legacy Support queue, which was retired on July 31. E10-C confirms the gap, since 2 of the 3 staff interviewed could not locate the plan. This matters because if an incident happens, staff wouldn't know what procedure to follow, which could extend downtime and hurt Meridian's chances of passing its first formal security assessment. To fix this, the company should make the plan available to all staff, update the after-hours contact to the MSP Service Desk, complete quarterly contact reviews, and reschedule the tabletop exercise.

*References: CTRL-010 | E10-A, E10-B, E10-C | RISK-008 | CAP-002*

### Connecting the records

A risk that shared a connection between my three files was RISK-005, where employees can act on behalf of others via the workstations. CTRL-003 is the control that was supposed to reduce this risk but instead showed that not all workstations had the same security configuration applied, further supporting workers being able to act on behalf of others. In E03-B, 2 out of the 6 workstations sampled did not have the security configuration in place. CAP-001 is the Corrective Action Plan that is used to mitigate and fix the control gap and reduce the risk. Implementing a mandatory settings configuration so that all stations lock after 15 minutes of inactivity should reduce the underlying issue of employees acting on behalf of others.

## 5. ISO 27001 Annex A mapping

I added the ISO mapping because it helps employers and auditors who know the ISO framework quickly understand what they are looking at. ISO/IEC 27001:2022 Annex A is used to classify which recognized security area each control falls under. The mapping makes each control easier to understand, but it doesn't mean the company is in compliance with the standard.

| Meridian control | Annex A reference and name | Why it relates |
| --- | --- | --- |
| CTRL-009: Clinic managers review physical access logs to the server closet quarterly | A.7.2 Physical entry | The control is about tracking who physically entered the server closet. |
| CTRL-007: IT-managed devices receive security patches monthly via the MSP | A.8.8 Management of technical vulnerabilities | Monthly patching is how the company finds and fixes known weaknesses on its devices. |

The full mapping for all 10 controls is in the [Control Assessment workbook](workbooks/Meridian_Control_Assessment.xlsx).

## 6. Corrective actions and planned verification

I chose CTRL-003 and CTRL-010 for corrective action because both tie directly to High risks in the risk register. CTRL-003 is the existing control for RISK-005, the highest-rated risk with a score of 20. Without workstations that lock consistently, employees may knowingly or unknowingly act on behalf of other workers, which could lead to changes in patient records or HIPAA issues. CTRL-010 supports RISK-008, which scored 15 (High). Without an incident response plan that employees can actually find and follow, nobody would know what procedure to use to contain an issue when other controls fail.

| CAP | Related control | Action summary | Owner | Target date | Status | Planned verification |
| --- | --- | --- | --- | --- | --- | --- |
| CAP-001 | CTRL-003 | Apply a mandatory lock configuration so all shared workstations lock after 15 minutes of inactivity | IT Administrator | 2027-02-25 | In Progress | Re-examine lock settings and test sampled workstations to confirm they lock after 15 minutes |
| CAP-002 | CTRL-010 | Make the incident response plan available to all staff, complete contact reviews, reschedule the tabletop exercise, and update the after-hours contact to the MSP Service Desk | Clinic Managers | 2027-03-15 | In Progress | Interview staff, run a tabletop exercise, and have managers sign off on the updated plan |

Because this assessment was done early in the process, no fixes have been verified yet. Verification is planned after each CAP's target completion date.

## 7. Supporting files

| File | Spreadsheet or document | PDF |
| --- | --- | --- |
| Risk Register | [Meridian_Risk_Register.xlsx](workbooks/Meridian_Risk_Register.xlsx) | [PDF](pdf/Meridian_Risk_Register.pdf) |
| Control Assessment and ISO mapping | [Meridian_Control_Assessment.xlsx](workbooks/Meridian_Control_Assessment.xlsx) | [PDF](pdf/Meridian_Control_Assessment.pdf) |
| CAP Tracker | [Meridian_CAP_Tracker.xlsx](workbooks/Meridian_CAP_Tracker.xlsx) | [PDF](pdf/Meridian_CAP_Tracker.pdf) |
| AI-generated evidence packet | [Meridian_Evidence_Packet.docx](evidence/Meridian_Evidence_Packet.docx) | [PDF](pdf/Meridian_Evidence_Packet.pdf) |
| Final self-check answers | [reflections.md](reflections.md) | — |

```
.
├── README.md
├── reflections.md
├── images/       project workflow diagram
├── workbooks/    Risk Register, Control Assessment, CAP Tracker (.xlsx)
├── pdf/          readable PDF versions of each workbook and the evidence packet
└── evidence/     AI-generated evidence packet (.docx)
```

## 8. Lessons learned and next steps

The biggest lesson from the assessment was that a stated control is not the same as an effective control. A statement does not mean that a control is working as intended unless there is evidence to back up the claim. Many times, in this project, the stated controls made it sound like everything was working perfectly, but once I looked at the evidence, it showed that not everything was working as intended.

When scoring risks and choosing ratings, I relied on the evidence, but also on my own judgment from personal experience. Working in a central fill pharmacy, my peers and I have seen risks like employees sharing workstations and workstations taking a long time to lock after inactivity. Because of that, when it came to rating these risks, I understood the actual effect they can have on patients and the company.

In a real engagement, I would also communicate with the company's employees and vendors and ask deeper questions, such as requesting vendors' SOC 2 reports or the company's vendor list. Gathering this type of information provides stronger evidence of the company's actual security posture. This would benefit the assessment because the results would be more realistic, rather than relying on statements provided by the management team.

Next, Meridian would need to implement the corrective actions for each control gap. Someone would then verify that the fixes actually worked, using a new round of testing and evidence. If the evidence shows the issues are resolved, the CAPs can be closed; if not, the gaps would be reassessed and new corrective actions created.
