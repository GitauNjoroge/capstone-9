# Capstone-9: Enterprise-Grade Secure Cloud Platform on AWS

**Author:** Peter Gitau (GitauNjoroge)
**AWS Account:** 803871049728 | **Region:** us-east-1
**Organisation:** Nairobi FinTech — CBK Regulated | **Date:** May 2026

---

## Architecture---

## Modules Completed

| # | Module | Key Services | Status |
|---|--------|-------------|--------|
| 1 | Multi-Account Governance | Organizations, SCPs, CloudTrail | ✅ |
| 2 | IAM Zero-Trust + OIDC | Permission Boundaries, GitHub OIDC | ✅ |
| 3 | Automated Incident Response | GuardDuty, EventBridge, Step Functions, Lambda | ✅ |
| 4 | Continuous Compliance | AWS Config, Security Hub, Inspector | ✅ |
| 5 | Application Security | WAF Web ACL, ALB, Rate Limiting | ✅ |
| 6 | Full-Stack Encryption | KMS CMK (auto-rotation), ACM, HTTPS | ✅ |
| 7 | Attack Simulation | SQLi, XSS, Rate Limit, GuardDuty samples | ✅ |
| 8 | Executive Report | Architecture diagram, exam answers | ✅ |

## Files in This Repo

| File | Requirement |
|------|-------------|
| `.github/workflows/deploy.yml` | Req 2 — OIDC CI/CD workflow |
| `iam/permission-boundary.json` | Req 2 — Permission boundary JSON |
| `iam/github-oidc-trust.json` | Req 2 — OIDC trust policy |
| `governance/scp-production-guardrails.json` | Req 1 — SCP JSON |
| `incident-response/stepfunctions-definition.json` | Req 3 — Step Functions |
| `incident-response/isolate-instance-lambda.py` | Req 3 — Lambda code |
| `app-security/waf-web-acl-rules.json` | Req 5 — WAF rules |
| `encryption/kms-key-policy.json` | Req 6 — KMS key policy |

## CI/CD: OIDC Federation — No Static Keys

The workflow uses GitHub OIDC. No AWS credentials are stored anywhere.
Trust is scoped to this repo and main branch only:
`repo:GitauNjoroge/capstone-9:ref:refs/heads/main`
