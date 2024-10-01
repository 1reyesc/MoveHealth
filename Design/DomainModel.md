# Move Health Platform - Domain Model

## Description
The **Move Health Platform** is a healthcare insurance planning tool designed specifically for financial advisors and their clients. The platform helps advisors create personalized financial plans, healthcare estimates, and provides advanced AI tools for document summarization. Below is an explanation of the domain model that describes the key entities and how they interact.

## Target Users
The platform supports three types of users:

1. **Financial Advisors**: These professionals assist clients in making informed decisions regarding investments, insurance, tax planning, and estate planning. Financial advisors using the platform are comprehensive planners helping their clients achieve their financial goals.
  
2. **Clients of Financial Advisors**: Primarily older adults nearing retirement (between 55-64 or 65+) or those with significant wealth. These clients rely on the financial advisors for healthcare and financial planning.

3. **Health Plan Advisors**: Health Plan Advisors specialize in assisting clients with choosing healthcare plans, estimating costs, and ensuring that clients enroll in appropriate coverage.

## Domain Model

### Entities

- **User**
  - General base entity representing anyone who uses the platform.
  - Attributes:
    - `id`: Unique identifier for each user.
    - `name`: Full name of the user.
    - `role`: Role of the user (Financial Advisor, Client, Health Plan Advisor).
    - `email`: Email address for user communication and login.
    - `password`: Secure password for authentication.

- **Financial Advisor**
  - A specialized user role focused on helping clients with financial planning and healthcare estimates.
  - Attributes:
    - `certification`: List of certifications held by the financial advisor.
    - `clientsManaged`: Number of clients under the advisor's management.
  - Functions:
    - **advise()**: Helps clients make informed decisions regarding their financial future.

- **Health Plan Advisor**
  - A specialized user focused on healthcare plan management and helping clients choose the best coverage.
  - Attributes:
    - `expertise`: Area of healthcare specialization.
    - `clientsManaged`: Number of clients the health plan advisor is managing.
  - Functions:
    - **guideClients()**: Guides clients in selecting healthcare plans.

- **Client**
  - Users who are being advised by financial advisors and health plan advisors.
  - Attributes:
    - `healthInfo`: Personal healthcare details relevant to plan selection.
  - Functions:
    - **viewPlans()**: Allows clients to view their healthcare plans.

- **Onboarding Process**
  - Tracks the steps a new user follows when joining the platform.
  - Attributes:
    - `onboardingId`: Unique identifier for the onboarding process.
    - `status`: Current status of the onboarding (e.g., in-progress, completed).
    - `stepNumber`: The current step in the onboarding sequence.
  - Functions:
    - **viewProgress()**: Shows the current progress of the onboarding.
    - **moveToNextStep()**: Moves the user to the next step of onboarding.

- **Healthcare Plan**
  - Represents the healthcare options available to a client.
  - Attributes:
    - `planId`: Unique identifier for each healthcare plan.
    - `name`: Name of the healthcare plan (e.g., Bronze, Silver, Gold).
    - `coverageType`: The type of coverage the plan offers.
    - `maxOutOfPocket`: The maximum out-of-pocket expenses for the plan.
  - Functions:
    - **estimateCost()**: Provides an estimate of the healthcare costs based on the plan.

- **AITool**
  - An AI tool that processes financial or healthcare PDFs and generates summaries.
  - Functions:
    - **generateSummary(pdfDocument)**: Summarizes the content of a PDF document to assist clients and advisors.

### Entity Relationships

- **User** has many **Healthcare Plans**.
- **User** has a single **Onboarding Process**.
- **User** can be a **Financial Advisor**, **Health Plan Advisor**, or a **Client**.
- **Financial Advisors**, **Health Plan Advisors**, and **Clients** all interact with the **AITool** for document summarization.

### Diagram
