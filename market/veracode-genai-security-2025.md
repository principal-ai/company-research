---
type: market-signal
title: Veracode 2025 GenAI Code Security Report
description: Findings on the rate and pattern of security vulnerabilities in AI-generated code across 100+ LLMs.
timestamp: 2026-06-16
volatility: slow
as_of: 2025-07-30
tags: [primary-source, ai-coding, security]
sources:
  - https://www.veracode.com/resources/analyst-reports/2025-genai-code-security-report/
  - https://www.businesswire.com/news/home/20250730694951/en/AI-Generated-Code-Poses-Major-Security-Risks-in-Nearly-Half-of-All-Development-Tasks-Veracode-Research-Reveals
  - https://www.helpnetsecurity.com/2025/08/07/create-ai-code-security-risks/
---

# Veracode 2025 GenAI Code Security Report

Veracode tested AI-generated code across 80 curated coding tasks and more than
100 large language models. Announced 2025-07-30. One finding per heading.

## Insecure choice ~45% of the time
When models had a choice between a secure and an insecure way to write code, they
chose the insecure option in 45% of cases.

## 2.74x more vulnerabilities than human code
AI-generated code contained 2.74x more vulnerabilities than human-written code in
Veracode's tests.

## Worst categories
Cross-Site Scripting had an 86% failure rate; Log Injection an 88% failure rate.

## Worst language
Java was the riskiest language tested, with a 72% security failure rate.

## Not improving with model scale
Newer and larger models did not produce more secure code than smaller ones,
suggesting the pattern is structural rather than a temporary limitation.
