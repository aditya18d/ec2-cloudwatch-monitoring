# EC2 System Monitoring and Alerting using Amazon CloudWatch & SNS

## 📌 Project Overview
This project demonstrates how to implement **host-level monitoring and alerting** on an AWS EC2 instance using **Amazon CloudWatch Agent** and **Amazon SNS**.  
The solution collects system metrics from the EC2 instance, evaluates threshold breaches using CloudWatch alarms, and sends automated email notifications.

This project was implemented in an **AWS Academy Learner Lab environment**.

---

## 🛠️ Services Used
- Amazon EC2
- Amazon CloudWatch
- Amazon CloudWatch Agent
- Amazon SNS
- IAM (Role-based access)

---

## 📊 Metrics Collected
Using **CloudWatch Agent (CWAgent namespace)**:
- Memory Utilization (`mem_used_percent`)
- Disk Utilization (`used_percent`)

---

## 🚨 Alerting Mechanism
- CloudWatch alarm configured on **memory utilization > 50%**
- Evaluation: **1 datapoint within 5 minutes**
- Notification triggered via **Amazon SNS (Email)**

---

## 📸 Screenshots (Proof of Implementation)

### CloudWatch Metric Visualization
📍 *Add screenshot here:*  
`screenshots/cloudwatch-metrics.png`

---

### CloudWatch Alarm Triggered
📍 *Add screenshot here:*  
`screenshots/memory-alarm-graph.png`

---

### SNS Email Notification
📍 *Add screenshot here:*  
`screenshots/alarm-triggered-email.png`

---

### CloudWatch Agent Running on EC2
📍 *Add screenshot here:*  
`screenshots/agent-running-status.png`

---

## ⚠️ Important Note (Learner Lab Context)
- Alarm naming reflects an initial intent to monitor CPU utilization.
- Due to **AWS Academy Learner Lab restrictions and session instability**, renaming the alarm and reconfiguring the agent was not possible.
- The final implementation correctly validates **metric collection, alarm evaluation, and SNS-based notifications**.

---

## 📘 Key Learnings
- Difference between default EC2 metrics and CloudWatch Agent metrics
- Configuring host-level monitoring using CWAgent
- Creating CloudWatch alarms with evaluation periods
- Integrating CloudWatch alarms with SNS
- Handling real-world limitations in restricted cloud environments

---

## ✅ Outcome
Successfully implemented an **end-to-end EC2 monitoring and alerting pipeline**, validating both metric collection and automated notifications.


