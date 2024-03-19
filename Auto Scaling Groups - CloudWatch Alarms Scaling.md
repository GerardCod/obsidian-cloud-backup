#ASG #Scalability 

• It is possible to scale an ASG based on CloudWatch alarms
• An alarm monitors a metric (such as Average CPU, or a custom metric)
• Metrics such as Average CPU are computed for the overall ASG instances
• Based on the alarm:  
	• We can create scale-out policies (increase the number of instances)
	• We can create scale-in policies (decrease the number of instances)

