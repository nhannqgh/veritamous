# Veritamous Specification (MVP)

## 📋 Introduction

**Veritamous** is a platform that allows employees to share reviews about their companies in a completely anonymous and secure way. Using **Zero-Knowledge Proof (ZKP)** technology, the platform ensures that employees can verify their employment status without revealing their personal identity.

---

## 1. Goals and Objectives

- **Primary Goal:** Enable employees to share honest company reviews while fully protecting their identity and employment privacy.
- **Problem Solved:** Lack of trustworthy, anonymous company reviews due to privacy concerns and unverifiable sources.
- **Objectives:**
  - Ensure only real employees can submit reviews (verifiable, not fake)
  - Guarantee anonymity and privacy for reviewers
  - Provide reliable, aggregated company insights for job seekers

---

## 2. Research & Market Understanding

- **Market Needs:** Demand for authentic, anonymous company reviews; current platforms lack strong privacy guarantees.
- **Competitors:** Glassdoor, Blind, TeamBlind, Fishbowl (none use ZKP for privacy).
- **Trends:** Increasing employee demand for privacy and data protection.
- **Target Early Adopters:** Tech industry employees, privacy-conscious professionals, companies with >50 employees.

---

## 3. Customer Pain Points

- Fear of retaliation or exposure when leaving honest reviews
- Inability to verify if reviews are from real employees
- Lack of trust in existing review platforms
- Desire for actionable, reliable company insights

---

## 4. Prioritized Core Features

**4.1 ZK Email Domain Verification**
   - Prove employment at a company without revealing identity or email
   - Prevent duplicate reviews via nullifier

**4.2 Anonymous Review Submission**
   - Simple, category-based review form (ratings + free text)
   - No personal data stored or linked

**4.3 Company Directory**
   - List/search companies, show basic info and review stats
   - Admin adds/verifies companies and domains

**4.4 Review Display & Aggregation**
   - Anonymous review listing
   - Aggregated statistics (average ratings, distributions)
   - Minimum anonymity set before displaying reviews

---

## 5. MVP User Experience

- **Onboarding:** User selects company, completes ZK email verification
- **Review Flow:** After verification, user submits a review via a simple, intuitive form (ratings, pros/cons, advice)
- **Browsing:** Users can search companies, view aggregated stats and anonymous reviews
- **Privacy:** No account creation, no tracking, no personal data stored
- **Anonymity:** Reviews only shown when enough submissions exist to protect identity

---

## 6. Feedback & Iteration Plan

- **Feedback Collection:** In-app feedback form, optional anonymous survey after review submission
- **Metrics:** Track number of verified reviews, company coverage, review distribution, user satisfaction (via survey)
- **Iteration:** Use feedback and metrics to prioritize next features

---

## 🚀 MVP Feature Details

### 1. Email Domain Verification with ZK Proof

**Description**: The system verifies employees through their company email using ZK proof.

**Requirements**:
- Employees must have an email with the official company domain
- Verify email access without revealing the specific email address
- Generate a nullifier to prevent duplicate reviews

**How it works**:
1. **Challenge Generation**: The system sends a verification code to the company email
2. **ZK Proof Creation**: The employee creates a ZK proof to prove:
   - They have access to an email with the company domain
   - They know the verification code sent
   - They have not submitted a review before
3. **Proof Verification**: The system verifies the proof without knowing the specific email
4. **Nullifier Storage**: Store the nullifier to prevent duplicate reviews

### 2. Anonymous Review Submission

**Description**: Allows verified employees to submit anonymous reviews.

**Requirements**:
- Simple interface for writing reviews
- Support for category-based ratings (culture, compensation, work-life balance, etc.)
- Rating system (1-5 stars) for each category
- Free text for pros/cons/advice

**How it works**:
1. **Verification Check**: Check if the user has completed ZK verification
2. **Review Form**: Display the review form with the following fields:
   - Overall rating (1-5)
   - Category ratings (work-life balance, compensation, culture, management, career growth)
   - Text fields (title, pros, cons, advice to management)
   - Employment info (department, role level, employment status)
3. **Anonymous Submission**: Submit the review without any identity information
4. **Nullifier Usage**: Use the nullifier to ensure one-review-per-employee

### 3. Company Directory

**Description**: A list of companies that can be reviewed on the platform.

**Requirements**:
- Database of companies with basic information
- Support for search and filter
- Company profile pages
- Verification status of company domains

**How it works**:
1. **Company Registration**: Admin adds companies to the system
2. **Domain Verification**: Verify email domains belonging to the company
3. **Company Profiles**: Display company information and aggregated reviews
4. **Search & Filter**: Allow users to search for companies by name, industry, size

### 4. Review Display & Aggregation

**Description**: Display submitted reviews and aggregated statistics.

**Requirements**:
- Anonymous review listing
- Statistical aggregation (average ratings, distributions)
- Filtering and sorting capabilities
- Minimum anonymity set requirements

**How it works**:
1. **Review Listing**: Display reviews without identity information
2. **Statistical Calculation**: Calculate average ratings, percentiles
3. **Anonymity Protection**: Only display when there are enough reviews to ensure anonymity
4. **Filtering Options**: Filter by department, role level, employment status (if enough data)

