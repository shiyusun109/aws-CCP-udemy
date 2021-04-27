# 🕐 Cloud Monitoring

- [CloudWatch Metrics](#cloudwatch-metrics)
- [CloudWatch Alarms](#cloudwatch-alarms)
- [CloudWatch Logs](#cloudwatch-logs)
- [CloudWatch Events - EventBridge](#cloudwatch-events---eventbridge)
- [CloudTrail](#cloudtrail)
- [X-Ray](#x---ray)
- [Service Health Dashboard](#service-health-dashboard)
- [Personal Health Dashboard](#personal-health-dashboard)
- [Summary](#summary)

## CloudWatch Metrics

CloudWatch provides metrics for every services in AWS. A Metric is a variable to monitor (CPU Utilization, NetworkIn…)

- Metrics have timestamps
- Can create CloudWatch dashboards of metrics
- Important Metrics:
  - EC2 instances: CPU Utilization (understanding the need of scale), Status Checks, Network (not RAM)
  - Default metrics every 5 minutes
  - Option for Detailed Monitoring ($$$): metrics every 1 minute
  - EBS volumes: Disk Read/Writes
  - S3 buckets: BucketSizeBytes, NumberOfObjects, AllRequests
  - Billing:Total Estimated Charge (only in us-east-1)
  - Service Limits: how much you’ve been using a service API
  - Custom metrics: we can create our own metrics

## CloudWatch Alarms

Alarms are use to trigger notifications for any metric. The alarms are customizable and we have multiple options (min, max, average, etc.). Alarms have three states: `OK` (green), `INSUFFICIENT_DATA` (yellow), `ALARM` (red).

With CloudWatch Alarms we can:

- Auto Scaling: Scale In/Up or Scale Out/Down EC2 instances to a desired count
- EC2 Actions: stop, terminate, reboot or recover an EC2 instance
- SNS Notifications: send notifications into SNS topics
- Billing Alarms
- Choose a schedule to check metrics and evaluate alarms.

## CloudWatch Logs

With CloudWatch Logs (customizable data of running applications). We can also enables real-time monitoring of logs and adjustable CloudWatch Logs retention (keep the logs for a week, a month, a year)

So, We can collect logs from applications within:

- Elastic Beanstalk: collection of logs from application
- ECS: collection from containers
- AWS Lambda: collection from function logs
- CloudTrail based on filter
- CloudWatch log agents: on EC2 machines or on-premises servers
- Route53: Log DNS queries

By default CloudWatch Logs does not work with EC2 instances, to do so, we need to

- Install CloudWatch Agent into EC2 Instance.
- Create the correct IAM Permissions.
- The agent also works with on-premise (Hybrid agent) so we can collect logs from it as well.
- The cloudwatch agent will communicate and send the logs to our CloudWatch Logs.

## CloudWatch Events - EventBridge

Is a service to do a serverless cron job and work with events within AWS Services.

- **Schedule**: we can create a scheduled script to run every X define period.
- **Event Pattern**: Event rules to react to a service doing an specific action such as:
  - Trigger Lambdas
  - Register notifications into SNS topics

### Amazon EventBridge

Amazon EventBridge is the next evolution of CloudWatch events. Received this new name and replaces CloudWatch Events name. (In the exam it is called EventBridge)

- Has a default event bus, which are Events generated by AWS Services
- Partner Event Bus: Can receive events from SaaS services or applications (Zendesk, DataDog, Segment, Auth0)
- Custom Event Bus:Can create custom event buses
- Schema Model: it a model event schema

> The main difference between CloudWatch Events and EventBus is that EventBus has new features and it a evolutions, so we have the default event bus (aws service) + partner and custom events and schema models.