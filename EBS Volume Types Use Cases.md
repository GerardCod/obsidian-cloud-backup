#EBS #Storage

## General Purpose SSD

• Cost effective storage, low-latency  
• System boot volumes,Virtual desktops, Development and test environments • 1 GiB - 16TiB

• gp3:  
	• Baseline of 3,000 IOPS and throughput of 125 MiB/s  
	• Can increase IOPS up to 16,000 and throughput up to 1000 MiB/s independently

• gp2:
- Small gp2 volumes can burst IOPS to 3,000
- Size of the volume and IOPS are linked, max IOPS is 16,000
- 3 IOPS per GB, means at 5,334 GB we are at the max IOPS

## Provisioned IOPS (PIOPS) SSD

• Critical business applications with sustained IOPS performance  
• Or applications that need more than 16,000 IOPS  
• Great for databases workloads (sensitive to storage perf and consistency)
• io1 (4 GiB - 16TiB):  
	• Max PIOPS: 64,000 for Nitro EC2 instances & 32,000 for other • Can increase PIOPS independently from storage size
• io2 Block Express (4 GiB – 64 TiB):  
	• Sub-millisecond latency  
	• Max PIOPS: 256,000 with an IOPS:GiB ratio of 1,000:1
• Supports EBS Multi-attach

## Hard Disk Drives (HDD)

• Cannot be a boot volume
• 125 GiB to 16TiB
• Throughput Optimized HDD (st1)  
• Big Data, Data Warehouses, Log Processing  
• Max throughput 500 MiB/s – max IOPS 500
• Cold HDD (sc1):
- For data that is infrequently accessed
- Scenarios where lowest cost is important
- Max throughput 250 MiB/s – max IOPS 250