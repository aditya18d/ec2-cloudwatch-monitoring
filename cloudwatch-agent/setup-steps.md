# CloudWatch Agent Setup Steps (EC2 Linux)

## 1️⃣ Install CloudWatch Agent
```bash
sudo yum install amazon-cloudwatch-agent -y

2️⃣ Run Configuration Wizard
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-config-wizard

3️⃣ Start CloudWatch Agent
sudo systemctl start amazon-cloudwatch-agent
sudo systemctl status amazon-cloudwatch-agent

4️⃣ Verify Metrics

Navigate to CloudWatch → Metrics → CWAgent

Confirm memory and disk metrics are visible


---

## 🔹 `alarms/memory-utilization-alarm.md`

```md
# CloudWatch Memory Utilization Alarm

## Alarm Details
- Metric Namespace: `CWAgent`
- Metric Name: `mem_used_percent`
- Threshold: > 50%
- Evaluation Period: 1 datapoint within 5 minutes
- Statistic: Average

---

## Alarm Behavior
- Alarm enters **ALARM** state when memory exceeds threshold
- Alarm returns to **OK** once metric stabilizes
- SNS notification triggered on state change

---

## Screenshot
📍 <img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/27bb8246-f1e5-4a47-bbd7-757aabdce98f" />

  
`screenshots/memory-alarm-graph.png`
