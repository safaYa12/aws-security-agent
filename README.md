# AWS Security Agent — End-to-End Application Security Assessment

An end-to-end application security assessment of **OWASP Juice Shop** using AWS Security Agent, covering custom security requirements, application design reviews, threat modelling, Git-integrated code reviews, and penetration testing with manual validation of findings.

## Overview

This project explores how AWS Security Agent can support application security throughout the software development lifecycle (SDLC), from security design and threat identification to source code analysis and penetration testing.

The assessment used OWASP Juice Shop as the target application and included custom security requirements, S3-hosted assessment inputs, Git integration, and manual verification of reported vulnerabilities.

## Objectives

- Create custom application security requirements and compliance rules.
- Validate JWT authorization best practices.
- Enforce company requirements prohibiting FTP and SFTP file hosting in applications.
- Perform a security design review against OWASP Juice Shop.
- Generate and review an application threat model.
- Integrate source code reviews with Git and pull requests.
- Perform penetration testing and independently validate reported findings.
- Understand how security findings can inform secure coding and remediation workflows.

## Project Workflow

### 1. Custom Security Requirements Pack

Created a custom security requirements pack to assess application security controls and company-specific compliance requirements.

**Security requirements covered:**

- **JWT authorization:** Validate JWT authorization and implementation against security best practices.
- **FTP restrictions:** Prohibit FTP-based file hosting in company applications.
- **SFTP restrictions:** Enforce the defined company requirement prohibiting SFTP file hosting in company applications.

The custom pack was subsequently used as part of the application design security review.

**Outcome:** Established application-specific security requirements that could be evaluated during the design assessment.

### 2. Application Security Design Review

Conducted a security design review of OWASP Juice Shop using the uploaded application design document.

**Input:** `Juice Shop – Application Design Doc`

**Activities:**

1. Uploaded the application design documentation.
2. Configured and executed the security design review.
3. Evaluated the design against the applicable security requirements.
4. Reviewed the resulting compliance findings, including findings associated with the custom security requirements pack.

**Result:** Identified **9 non-compliant findings** during the design review.

The results demonstrated how application design documentation can be assessed against security requirements before relying solely on implementation-level testing.

### 3. Threat Modelling

Configured a threat modelling assessment using the OWASP Juice Shop source code hosted in Amazon S3.

**Activities:**

1. Uploaded the Juice Shop source code to an S3 location.
2. Configured the S3 URL as the source input for the threat model.
3. Created and executed the threat model in the AWS Security Agent interface.
4. Reviewed the resulting threat model overview and findings.
5. Manually identified an additional threat and added it to the findings for tracking and assessment.

**Outcome:** Generated a threat model from the application source and supplemented the agent's findings with a manually identified threat.

This phase demonstrated the value of combining automated threat analysis with human security review.

### 4. Git-Integrated Code Review

Configured source code review using the Juice Shop source hosted in S3 and integrated the workflow with Git.

**Activities:**

1. Configured the source code S3 URL as the code review target.
2. Edited the code review configuration.
3. Connected the Git integration and installed the AWS Security Agent integration on the Git account.
4. Configured the review settings to include:
   - Security requirements
   - Vulnerability findings
5. Modified vulnerable application code.
6. Created a pull request in Git.
7. Observed the agent's code review and validation workflow.

**Outcome:** Exercised a pull-request-based security review workflow in which code changes could be evaluated against security requirements and vulnerability findings.

This demonstrated how application security checks can be incorporated into developer workflows rather than being limited to standalone assessments.

### 5. Penetration Testing and Manual Validation

Performed a penetration test against OWASP Juice Shop using AWS Security Agent.

**Activities:**

1. Configured the penetration test and reviewed the available settings.
2. Supplied the Juice Shop source code S3 URL as the code scanning source.
3. Executed the assessment and reviewed the resulting logs and findings.
4. Investigated a reported SQL-related vulnerability.
5. Cross-checked the agent-provided Python validation script.
6. Manually followed the recommended reproduction steps to independently verify the finding.

**Outcome:** Validated the reported SQL-related vulnerability through both script-assisted verification and manual reproduction.

This phase reinforced the importance of verifying automated security findings instead of treating every generated finding as confirmed.

## Key Results

| Assessment area | Result |
|---|---|
| Custom security requirements | Created a custom requirements pack |
| JWT security | Included JWT authorization best practices |
| FTP/SFTP restrictions | Defined application compliance requirements |
| Security design review | 9 non-compliant findings identified |
| Threat modelling | Generated a threat model and added a manually identified threat |
| Git integration | Configured security reviews around pull requests |
| Code review | Reviewed security requirements and vulnerability findings |
| Penetration testing | Investigated a SQL-related finding and manually validated it |

## Tools and Technologies

- **AWS Security Agent** — Application security assessment workflows
- **Amazon S3** — Source code and assessment input hosting
- **Git** — Source control and pull request workflow
- **OWASP Juice Shop** — Deliberately vulnerable application used for testing
- **Python** — Agent-provided vulnerability validation script
- **JWT** — Authorization security requirements
- **FTP/SFTP** — File-hosting compliance requirements

## Screenshots and Walkthrough

The project includes a detailed screenshot walkthrough documenting the configuration, execution, and findings of the assessment.


## Security Considerations

- OWASP Juice Shop was used as a deliberately vulnerable assessment target.
- Keep source code, S3 objects, credentials, and assessment artefacts protected according to their sensitivity.
- Redact AWS account IDs, access tokens, session credentials, private URLs, and other sensitive information from published screenshots.
- Independently validate findings before classifying vulnerabilities as confirmed.
- Treat remediation as a separate activity unless a fix has been implemented and verified.
- Run security testing only against authorized targets and within the defined assessment scope.

## Key Takeaways

This project provided practical experience with application security across multiple stages of the SDLC:

- Translating organizational security requirements into assessable controls.
- Reviewing application designs for compliance gaps.
- Using source code to support threat modelling.
- Integrating security analysis with Git-based development workflows.
- Investigating penetration-testing findings and independently reproducing a vulnerability.
- Combining automated security analysis with manual validation.

## Conclusion

The project demonstrated an end-to-end application security assessment workflow using AWS Security Agent and OWASP Juice Shop. It covered security requirements, design compliance, threat modelling, Git-integrated code review, and penetration testing, with particular emphasis on validating findings through independent analysis.

**Focus:** Cloud application security | Secure SDLC | Threat Modelling | Security Requirements | Git Integration | Penetration Testing | Vulnerability Validation
