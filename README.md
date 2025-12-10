# MedTrack-Serverless-Medication-Tracker
A serverless AWS-based medication tracking application that manages schedules and sends automated dosage reminders using event-driven architecture.

# Project Goal
Create, update, and manage medication schedules
Automated dosage reminders via notifications
Event-driven backend using AWS Lambda
Secure REST APIs for frontend integration
Scalable, pay-per-use serverless architecture
Role-based access control using IAM

# Tech Used
Backend & Cloud
 AWS Lambda – Business logic and schedule processing
 Amazon DynamoDB – NoSQL storage for users and medications
 Amazon API Gateway – RESTful API endpoints
 Amazon SNS – Notification delivery for dosage alerts
 AWS IAM – Secure, least-privilege access control
Frontend
 Streamlit / Flask – Simple UI for managing medication data

# Architecture Overview
 Users interact with the Streamlit/Flask frontend to manage medication schedules.
 The frontend sends requests to API Gateway.
 API Gateway triggers Lambda functions to process requests.
 Medication data is stored and retrieved from DynamoDB.
 Scheduled or event-driven Lambda executions evaluate dosage times.
 SNS publishes reminder notifications to subscribed users.
 IAM roles and policies enforce secure access between services.
The system is fully serverless, fault-tolerant, and horizontally scalable.

# Project Structure
 medtrack/
├── backend/
│   ├── lambda/
│   │   ├── create_medication.py
│   │   ├── update_schedule.py
│   │   └── reminder_handler.py
│   └── infrastructure/
│       └── iam_policies.json
├── frontend/
│   ├── app.py
│   └── requirements.txt
├── README.md
└── requirements.txt

# Setup & Deployment
 Prerequisites
  AWS account
  AWS CLI configured
  Python 3.x
  IAM permissions to deploy serverless resources
 Deployment Steps 
  Create DynamoDB tables for users and medications
  Deploy Lambda functions
  Configure API Gateway routes
  Set up SNS topics and subscriptions
  Apply IAM roles and policies
  Run the frontend locally or deploy it

# Scalability & Design Considerations
 Serverless architecture eliminates server management
 DynamoDB supports horizontal scaling with minimal latency
 SNS enables asynchronous notification delivery
 Event-driven design improves reliability and cost efficiency

# Use Cases
 Personal medication tracking
 Healthcare reminders and alerts
 Serverless architecture demonstrations
 Cloud portfolio project for AWS-focused roles

# Future Improvements
 Authentication (Cognito / OAuth)
 Cron-based scheduling with EventBridge
 Multi-channel notifications (SMS, email)
 Audit logging and monitoring
 Infrastructure as Code (Terraform / SAM)

# Test URL
 http://medtrackwebsite.s3-website.ca-central-1.amazonaws.com/
