# Test Plan: Stock Trading with AI Analyst

**Project Name:** Stock Trading AI Analyst  
**Version:** 1.0  
**Date:** November 24, 2025  
**Author:** Michael Ludwikowski  
**Project Advisor:** Dr. Hayes

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Test Strategy](#2-test-strategy)
3. [Test Environment](#3-test-environment)
4. [Test Schedule](#4-test-schedule)
5. [Entry and Exit Criteria](#5-entry-and-exit-criteria)
6. [Test Deliverables](#6-test-deliverables)
7. [Risk Analysis](#7-risk-analysis)
8. [Test Scenarios](#8-test-scenarios)
   - [8.1 Summary](#81-summary)
   - [8.2 Test Organization](#82-test-organization)
   - [8.3 Test Execution](#83-test-execution)
9. [Appendices](#9-appendices)

---

## 1. Introduction

### 1.1 Purpose
This test plan outlines the comprehensive testing strategy for the Stock Trading AI Analyst application. It defines the approach, resources, schedule, and specific test cases to verify all 44 functional requirements are met.

### 1.2 Project Overview  
The Stock Trading AI Analyst is an educational platform that simulates stock trading with fake money ($1000 initial balance per account). It uses an AI assistant (powered by OLLama v3.3) to provide stock predictions and automated investment capabilities, helping novice traders learn in a risk-free environment.

### 1.3 Scope

**In Scope:**
- User account management (create, reset, profiles, multiple accounts)
- Fake money wallet and balance management with overdraft prevention
- Stock trading simulation with real historical data
- Buy/sell operations, portfolio tracking, and transaction logging
- AI predictions, auto-investment, and performance tracking
- Notifications, alerts, and margin trading
- Educational features, tutorials, quizzes, and simulations
- UI/Dashboard functionality with responsive design
- Error handling, logging, and security validation

**Out of Scope:**
- Real money transactions
- Mobile native applications (Phase 2)
- Multi-language support (future enhancement)
- External trading platform integration

---

## 2. Test Strategy

### 2.1 Testing Approach
- **Unit Testing:** Component-level testing during development (developers)
- **Integration Testing:** Component interaction testing (UI ↔ Backend ↔ AI ↔ Database)
- **System Testing:** End-to-end validation of complete integrated system
- **User Acceptance Testing (UAT):** Real user validation with usability focus
- **Performance Testing:** Load testing (50+ concurrent users) and response time validation
- **Security Testing:** Input validation, authentication, authorization, data protection

### 2.2 Test Execution Methodology
- Tests consolidated into 20 comprehensive test cases (TC-001 through TC-020)
- Each test case covers multiple related functional requirements
- Execution tracking via **TestCases_All.xlsx** spreadsheet with individual sheets per test case
- Iterative testing with defect tracking and resolution cycles
- Priority-based execution: Critical → High → Medium → Low

### 2.3 Test Types

**Functional Testing:** Verify features work according to requirements  
**Integration Testing:** Validate component interactions  
**System Testing:** Complete system validation  
**Performance Testing:** Response times, concurrent users, AI accuracy  
**Security Testing:** Input validation, authentication, data protection  
**Usability Testing:** User experience, learning curve, satisfaction (SUS ≥68)

---

## 3. Test Environment

### 3.1 Hardware Requirements
- **Development/Test Machine:** 
  - CPU: Intel i7 or equivalent (multi-core for AI processing)
  - RAM: 16GB minimum (32GB recommended for AI model)
  - Storage: 50GB+ available SSD storage
  - Network: Stable internet for stock API calls

- **Test Devices:** 
  - Desktop browsers: 1920x1080 resolution
  - Tablet: 768x1024 resolution (responsive design testing)
  - Mobile: 375x667 resolution (responsive design testing)

### 3.2 Software Environment
- **Operating System:** Windows 10/11, Linux (Ubuntu 20.04+), or MacOS 11+
- **Backend Framework:** Python 3.10+, Django 4.x or Flask 2.x
- **AI Model:** OLLama v3.3 with llama model
- **Database:** PostgreSQL 14+ or SQLite 3.x
- **Browsers:** Chrome (latest), Firefox (latest), Safari (latest)
- **Stock API:** Alpha Vantage, Yahoo Finance, or similar real-time data provider
- **Testing Tools:** JMeter/Locust (load testing), pytest (unit tests)

### 3.3 Test Data
- **Stock Symbols:** 20-30 diverse stocks (AAPL, GOOGL, TSLA, MSFT, etc.)
- **Historical Data:** Minimum 1 year of daily OHLCV data per symbol
- **User Accounts:** Test users with various states (new, active, reset)
- **Portfolio States:** Empty, small position, diversified, margin positions
- **AI Training Data:** Labeled market scenarios (bull, bear, volatile)

---

## 4. Test Schedule

| Phase | Duration | Start Date | End Date | Owner | Deliverables |
|-------|----------|------------|----------|-------|--------------|
| **Test Planning** | 1 week | TBD | TBD | Michael | Test Plan, Test Cases |
| **Unit Testing** | 4 weeks | TBD | TBD | Developers | Unit Test Results |
| **Integration Testing** | 2 weeks | TBD | TBD | QA Team | Integration Test Report |
| **System Testing** | 2 weeks | TBD | TBD | QA Team | System Test Report |
| **Performance Testing** | 1 week | TBD | TBD | QA Team | Performance Metrics |
| **UAT** | 1 week | TBD | TBD | End Users | UAT Sign-off |
| **Defect Resolution** | Ongoing | TBD | TBD | Dev Team | Bug Fixes |
| **Regression Testing** | 1 week | TBD | TBD | QA Team | Regression Report |

**Total Estimated Duration:** 12 weeks (with parallel activities)

---

## 5. Entry and Exit Criteria

### 5.1 Entry Criteria (Test Phase Readiness)
- [ ] All features implemented and code-complete
- [ ] Test environment fully configured and operational
- [ ] Test data prepared, validated, and loaded
- [ ] Test cases reviewed and approved by stakeholders
- [ ] All blocking defects from previous phase resolved
- [ ] Test execution tools configured (spreadsheet, automation frameworks)

### 5.2 Exit Criteria (Test Phase Completion)
- [ ] All critical and high-priority test cases executed and passed
- [ ] No critical (P0) or high-severity (P1) defects remain open
- [ ] Medium/low severity defects documented with workarounds
- [ ] Code coverage meets minimum threshold (80%+ for critical modules)
- [ ] Performance benchmarks achieved:
  - Dashboard load time < 2 seconds
  - AI prediction generation < 5 seconds
  - Stock search response < 2 seconds
  - 50+ concurrent users supported without degradation
- [ ] AI prediction accuracy ≥ target threshold (documented baseline)
- [ ] System Usability Scale (SUS) score ≥ 68 (above average)
- [ ] UAT sign-off received from stakeholder representatives
- [ ] Test summary report completed and approved

---

## 6. Test Deliverables

1. **Test Plan Document** (this document) - Testing strategy and approach
2. **Test Cases Spreadsheet** (TestCases_All.xlsx) - 20 consolidated test cases with execution tracking
3. **Test Execution Reports** - Pass/fail status, screenshots, defect references
4. **Defect/Bug Reports** - Issue tracking logs with severity, priority, reproduction steps
5. **Performance Test Results** - Load testing metrics, response times, AI accuracy measurements
6. **UAT Feedback Report** - User satisfaction scores (SUS, NPS), qualitative feedback
7. **Test Summary Report** - Final testing outcomes, metrics, recommendations
8. **Traceability Matrix** - Requirements coverage mapping (Requirements 1-44 → Test Cases)

---

## 7. Risk Analysis

| Risk | Impact | Probability | Mitigation Strategy |
|------|--------|-------------|---------------------|
| AI model accuracy below target | High | Medium | Extensive training data collection, iterative model tuning, baseline documentation |
| Stock API rate limits/downtime | Medium | Medium | Implement caching strategy, fallback to cached historical data, multiple API providers |
| Database performance with large transaction history | High | Low | Database indexing, query optimization, connection pooling, load testing early |
| Insufficient test coverage of edge cases | High | Low | Automated testing, comprehensive code reviews, exploratory testing sessions |
| UAT participant availability delays | Medium | Medium | Early user engagement, flexible scheduling, remote testing options |
| AI model training time exceeds schedule | Medium | Low | Pre-train model with public datasets, parallel development tracks |
| Security vulnerabilities discovered late | High | Low | Security testing from early phases, input validation testing, penetration testing |
| Browser compatibility issues | Low | Medium | Cross-browser testing in parallel with development, use standard web technologies |
| Responsive design issues on mobile | Medium | Low | Mobile-first design approach, continuous responsive testing |

---

## 8. Test Scenarios

### 8.1 Summary

This test plan includes **20 consolidated test cases** covering all 44 functional requirements. Each test case combines related functionality for comprehensive validation. Detailed test cases with prerequisites, test data, step-by-step procedures, expected results, and requirements mapping are documented in **TestCases_All.xlsx**.

| Test Case ID | Description | Priority | Requirements Covered |
|--------------|-------------|----------|---------------------|
| **TC-001** | Comprehensive Account Management (Create, Validate, Reset, Profile Access) | Critical | Req 1, 3, 6 |
| **TC-002** | Multiple Accounts and Notification System | High | Req 4, 5 |
| **TC-003** | Wallet Balance Management and Transaction Processing | Critical | Req 2, 6, 7, 8, 10 |
| **TC-004** | Low Balance Notification System | High | Req 9 |
| **TC-005** | Stock Trading Operations (Buy, Sell, Portfolio, Charts, Search) | Critical | Req 11, 12, 13, 15, 16, 17, 19, 38 |
| **TC-006** | Price Alerts and Margin Trading | High | Req 14, 18 |
| **TC-007** | AI Predictions and Accuracy Validation | High | Req 20, 21, 23, 24, 25, 27, 28 |
| **TC-008** | AI Auto-Investing and Top Picks | High | Req 22, 24 |
| **TC-009** | AI Performance Tracking and Adjustable Settings | Medium | Req 26, 29, 30 |
| **TC-010** | Educational Tutorials and Risk Assessment | Medium | Req 31, 32, 35, 39 |
| **TC-011** | Training Simulations and Knowledge Quizzes | Medium | Req 33, 34 |
| **TC-012** | Dashboard UI and Responsiveness | High | Req 36, 37 |
| **TC-013** | Visual Indicators and Data Presentation | High | Req 37, 38 |
| **TC-014** | End-to-End System Integration | Critical | All 44 Requirements |
| **TC-015** | System Performance and Concurrent User Load | High | Req 1, 2, 36 |
| **TC-016** | Input Validation and Security Testing | High | Req 40 |
| **TC-017** | Network Failures and API Error Handling | High | All integration points |
| **TC-018** | AI Errors and Activity Logging | Critical | Req 41, 42, 43 |
| **TC-019** | First-Time User Onboarding and Learning Curve (UAT) | High | All user-facing features |
| **TC-020** | Long-Term User Satisfaction and AI Trust (UAT) | High | All features, AI effectiveness |

**Total: 20 Test Cases covering all 44 Functional Requirements**

### 8.2 Test Organization

**Functional Categories:**
- **Account Management** (TC-001, TC-002)
- **Wallet & Transactions** (TC-003, TC-004)
- **Stock Trading** (TC-005, TC-006)
- **AI Features** (TC-007, TC-008, TC-009)
- **Educational Content** (TC-010, TC-011)
- **User Interface** (TC-012, TC-013)
- **Integration & Performance** (TC-014, TC-015)
- **Error Handling & Security** (TC-016, TC-017, TC-018)
- **User Acceptance** (TC-019, TC-020)

**Test Execution Order:**
1. **Phase 1 - Core Functionality** (Critical): TC-001, TC-003, TC-005, TC-014, TC-018
2. **Phase 2 - Extended Features** (High): TC-002, TC-004, TC-006, TC-007, TC-008, TC-012, TC-013, TC-015, TC-016, TC-017, TC-019, TC-020
3. **Phase 3 - Enhanced Features** (Medium): TC-009, TC-010, TC-011

### 8.3 Test Execution

**Execution Process:**
1. Open **TestCases_All.xlsx** spreadsheet
2. Navigate to the appropriate test case sheet (TC-001 through TC-020)
3. Review Prerequisites and ensure test environment is ready
4. Follow test steps sequentially, recording Actual Results for each step
5. Mark each step as Pass/Fail/Not Executed
6. Document any defects with screenshots and details
7. Update test case status (Pass/Fail/Blocked)
8. Link defect IDs to failed test cases for traceability

**Defect Reporting:**
- All defects logged with: Severity (Critical/High/Medium/Low), Priority, Reproduction Steps, Screenshots
- Critical/High defects block test execution until resolved
- Medium/Low defects documented for future sprints

**Retesting:**
- Failed test cases re-executed after defect resolution
- Regression testing performed after major bug fixes

---

## 9. Appendices

### 9.1 References
- **Requirements Document:** (Link to functional requirements specification)
- **System Architecture:** (Link to system design documents)
- **API Documentation:** (Link to backend API specs)
- **Database Schema:** (Link to DB design documentation)

### 9.2 Test Case Details
See **TestCases_All.xlsx** for complete test case documentation with:
- Test Case ID, Description, Scenario
- Created By, Date Created, Version
- Tester Name, Date Tested, Test Status
- Prerequisites list
- Test Data specifications
- Priority (Critical/High/Medium/Low)
- Requirements mapping
- Step-by-step test procedures with Expected Results
- Actual Results and Pass/Fail status columns

### 9.3 Glossary
- **AI Analyst:** OLLama v3.3-powered prediction and auto-investment system
- **Fake Money:** Simulated currency ($1000 initial balance) for risk-free trading
- **Portfolio:** Collection of user's stock holdings with purchase prices and current values
- **Transaction Log:** Historical record of all buy/sell trades with timestamps
- **Margin Trading:** Ability to purchase stocks exceeding available balance (with limits)
- **SUS:** System Usability Scale - 10-question usability assessment (target ≥68)
- **NPS:** Net Promoter Score - User satisfaction metric (target ≥0)
