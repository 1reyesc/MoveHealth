## Actors
- **Financial Advisors**: Individuals responsible for helping clients achieve their financial goals. Advisors assist with investments, insurance, estate planning, and tax planning. They use the platform to upload, share, and review documents related to health insurance planning for their clients.
  
- **Clients of Financial Advisors**: Early retirees or individuals nearing retirement age, typically between 55-64 years old, with investments between $1MM and $5MM. They rely on financial advisors to manage their health insurance options.

- **Health Plan Advisors**: Team members of Move Health who assist financial advisors and their clients with health insurance planning. They review uploaded documents, summarize health insurance plans, and help with enrollment.

- **Admin**: System administrators who monitor user activity, manage document uploads, and ensure compliance with system rules.

- **External Systems**: Systems that handle document uploads, PDF processing, and AI functionalities for summarizing and editing documents.

## Use Cases

### UC1: Upload PDF Document
- **Description**: Financial advisors need to upload documents related to health insurance planning for clients. This is a core feature enabling document management and analysis.
- **Actors**: Financial Advisors, Clients of Financial Advisors
- **Flow**:
  1. The advisor or client selects the "Upload Document" feature.
  2. The user selects a PDF file from their system.
  3. The system processes and uploads the document.
  4. The system verifies if the document is related to health insurance.
  5. The system notifies the user if the document is accepted or rejected.
- **Business Requirement**: BR1 (Improve MVP to enhance engagement and productivity for advisors).

### UC2: Summarize Uploaded PDF
- **Description**: The system provides a summarized version of the uploaded health insurance document, breaking it down into four key points for easy understanding.
- **Actors**: Financial Advisors, Clients of Financial Advisors, Health Plan Advisors
- **Flow**:
  1. After uploading, the user selects the "Summarize Document" feature.
  2. The AI processes the document and extracts key information.
  3. The system displays a summary with four main points.
- **Business Requirement**: BR2 (Provide users with a friendly, easy-to-use interface and accessible information).

### UC3: Ask AI Questions About Document
- **Description**: Users can ask specific questions or provide prompts related to the uploaded document. The AI will provide answers based on the document content.
- **Actors**: Financial Advisors, Clients of Financial Advisors
- **Flow**:
  1. The user uploads a document.
  2. The user asks the AI a question related to the document.
  3. The AI processes the question and responds with an answer.
- **Business Requirement**: BR1 (Improve efficiency and engagement for users by providing interactive tools).

### UC4: Edit Document via AI Prompt
- **Description**: The system allows editing of the uploaded document based on AI-driven prompts. This feature is aimed at improving document revisions efficiently.
- **Actors**: Financial Advisors, Clients of Financial Advisors
- **Flow**:
  1. The user uploads a document.
  2. The user provides an editing prompt to the AI.
  3. The AI suggests or implements edits in the document.
  4. The user reviews the edited document.
- **Business Requirement**: BR2 (Provide tools that make the platform easy to use and valuable for clients).

### UC5: Admin Monitoring
- **Description**: Admins monitor document uploads and ensure that only valid health insurance-related documents are uploaded. They can track usage and document types in the dashboard.
- **Actors**: Admin
- **Flow**:
  1. Admin logs into the dashboard.
  2. Admin views uploaded documents and related metadata.
  3. Admin ensures compliance with system rules.
- **Business Requirement**: BR1 (Support operational efficiency through monitoring and compliance tools).
