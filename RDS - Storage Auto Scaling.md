#RDS #Storage 

- Helps you increase storage on your RDS DB instance dynamically
- When RDS detects you are running out of free database storage, it scales automatically
- Avoid manually scaling your database storage
- You have to set Maximum Storage Threshold (maximum
- Automatically modify storage if:  
    • Free storage is less than 10% of allocated storage • Low-storage lasts at least 5 minutes  
    • 6 hours have passed since last modification
- Useful for applications with unpredictable workloads
- Supports all RDS database engines