# Move Health Platform Tech Stack

## Description
This is an outline of the tech stack chosen for the **Move Health Platform** and the reasoning behind those choices. These technologies were selected to meet specific requirements for scalability, ease of development, and the ability to integrate AI functionalities for financial document summarization.

## Table of Contents
1. [Frontend](#frontend)
2. [Backend](#backend)
3. [AI Tool](#ai-tool)
4. [Infrastructure](#infrastructure)
5. [Additional Tools](#additional-tools)

## Frontend

**Frameworks** - [React](https://reactjs.org)

React is a widely-used JavaScript library for building interactive and responsive user interfaces for single-page applications. It was chosen due to its modular component-based architecture, which allows for efficient development and reusability of UI components. Additionally, React’s ecosystem has strong community support and numerous libraries that can be easily integrated into the project.

## Backend

**Framework** - [Ruby on Rails](https://rubyonrails.org)  
**Database** - [PostgreSQL](https://www.postgresql.org)

Ruby on Rails is a full-stack web application framework that prioritizes simplicity and convention over configuration. It was selected due to its rapid development features, built-in security capabilities, and ease of integration with APIs.

PostgreSQL is a powerful, open-source relational database management system (RDBMS) that excels in handling large datasets and complex queries. It was selected for its ACID compliance, reliability, and support for complex financial data structures.

## AI Tool

**API** - [OpenAI (ChatGPT)](https://openai.com)

The AI Tool  that will will add to the  the Move Health Platform leverages OpenAI’s AP to process and summarize financial documents in PDF format. This tool allows both financial advisors and clients to get concise summaries of  financial document pdfs, enhancing productivity and saving time in the decision-making process.

## Infrastructure

**Hosting** - [Heroku](https://www.heroku.com)  
**Version Control** - [GitHub](https://github.com)

Heroku provides a platform-as-a-service (PaaS) environment that simplifies the deployment and scaling of the application without the need for extensive infrastructure management. It also integrates easily with other services such as databases, email providers, and CI/CD pipelines.

GitHub is used for version control and collaboration. It facilitates seamless team collaboration through its pull request and issue tracking system. GitHub also integrates with CI/CD tools to automate testing and deployment processes.

## Additional Tools

**Email Service** - [Postmark](https://postmarkapp.com)  
**Scheduling** - [cal.com](https://cal.com)

Postmark handles transactional emails such as user onboarding and password resets, ensuring reliable email delivery.  
cal.com  is integrated to manage appointments and consultations, allowing clients and advisors to schedule meetings directly from the platform.
