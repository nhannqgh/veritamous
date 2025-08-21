
# Veritamous - MVP Specification

## 📋 Introduction

**Veritamous** is a platform that allows employees to share reviews about their companies in a completely anonymous and secure way. Using **Zero-Knowledge Proof (ZKP)** technology, the platform ensures that employees can verify their employment status without revealing their personal identity.

### Main Objectives:
- **Privacy-First**: Fully protect the identity of the reviewer
- **Verifiable**: Ensure only real employees can submit reviews
- **Transparent**: Provide reliable review information for job seekers
- **Anonymous**: Reviews cannot be linked to the author

## 🚀 Core Features of the MVP

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

