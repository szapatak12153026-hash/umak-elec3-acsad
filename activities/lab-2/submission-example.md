# Lab 2 Submission 



## Instance Tracking
**First Instance**
- Instance ID: i-00a89e4544b8f652f
- Availability Zone: ap-southeast-1b

**Second Instance**
- Instance ID: i-00a89e4544b8f652f
- Availability Zone: ap-southeast-1b

## Questions
1. Why did the group stop at 2 instances?

The Auto Scaling Group stopped at two instances because its maximum capacity was configured to 2. This limit prevents the group from launching additional instances beyond the specified maximum, even when CPU utilization remains high.

2. Why did terminating an instance by hand not remove the cost?

Terminating an instance manually did not permanently reduce the group's capacity because Auto Scaling automatically launched a replacement to maintain the desired capacity and satisfy the minimum capacity requirement. The replacement instance could continue incurring charges.

3. Why is the target value 40 percent and not 90 percent?

A 40% CPU utilization target allows the Auto Scaling Group to respond to increasing workloads before the existing instance becomes overloaded. A 90% target could allow CPU utilization to remain very high while a new instance launches and initializes, potentially causing slow response times or service interruptions.

4. What did the automatic cutoff protect us from?

The automatic cutoff helped prevent unexpected AWS charges by stopping or limiting the lab's resources after the allotted period. It reduced the risk of leaving instances and other resources running accidentally after the lab session.

5. What changes when a load balancer sits in front of the group?

A load balancer provides a single entry point for users and distributes incoming requests among healthy instances in the Auto Scaling Group. Users can access the application through the load balancer's DNS name instead of manually choosing individual insta
