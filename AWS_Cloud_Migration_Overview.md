# AWS Cloud Migration - Tools and Services Portfolio

## Overview

AWS provides a comprehensive suite of tools and services to facilitate cloud migration across three key phases: **Assess**, **Mobilize**, and **Migrate and Modernize**. This portfolio enables organizations to plan, execute, and track their migration journey efficiently while minimizing risks and downtime.

---

## Migration Framework

The AWS migration framework follows a structured approach:

```
Assess → Mobilize → Migrate and Modernize
```

### **Phase 1: Assess**
Understand your current environment, build a business case, and identify migration readiness.

### **Phase 2: Mobilize**
Plan the migration strategy, prepare the landing zone, and establish governance.

### **Phase 3: Migrate and Modernize**
Execute workload and data migrations while modernizing applications.

---

## AWS Migration Tools and Services by Category

### 🔍 **Discovery and Assessment**

#### **AWS Application Discovery Service**
- **Purpose**: Collects detailed information about your on-premises data center infrastructure
- **Key Features**:
  - Agentless or agent-based discovery
  - Server configuration, performance metrics, and network dependencies
  - Integration with AWS Migration Hub
- **Use Case**: Build a comprehensive inventory of your IT assets to inform migration planning
- **Best Practice**: Use agent-based discovery for deeper insights into server dependencies and performance data

#### **AWS Migration Evaluator**
- **Purpose**: Provides a data-driven business case for migrating to AWS
- **Key Features**:
  - Cost analysis comparing on-premises vs. AWS
  - Right-sizing recommendations
  - Quick insights for cost savings
- **Use Case**: Build executive-level business cases with TCO analysis
- **Best Practice**: Collect at least 30 days of performance data for accurate cost projections

#### **AWS Migration Portfolio Assessment (MPA)** *(Partner Only)*
- **Purpose**: Creates consolidated infrastructure data and Total Cost of Ownership (TCO) analysis
- **Key Features**:
  - Portfolio-level migration planning
  - Wave planning and prioritization
  - Integration with partner tools
- **Use Case**: Large-scale enterprise migrations requiring detailed portfolio analysis
- **Target Audience**: AWS Partners and large enterprise customers

#### **Migration Readiness Assessment**
- **Components**:
  - **CART (Cloud Adoption Readiness Tool)**: Self-service assessment
  - **MRA (Migration Readiness Assessment)**: Partner-led comprehensive evaluation
- **Purpose**: Identify gaps in organizational readiness across six key dimensions
- **Best Practice**: Complete MRA before large-scale migrations to address skill gaps and process improvements

---

### 📋 **Planning and Design**

#### **AWS Migration Hub**
- **Purpose**: Centralized tracking and management console for migrations
- **Key Features**:
  - Single dashboard for multiple migration projects
  - Track progress across AWS and partner tools
  - Strategy recommendations for each application
  - Integration with Application Discovery Service
- **Use Case**: Monitor and coordinate large-scale migrations with multiple workloads
- **Best Practice**: Use Migration Hub as your single source of truth for migration status and metrics

#### **AWS Control Tower**
- **Purpose**: Sets up and governs a secure, multi-account AWS environment
- **Key Features**:
  - Automated account provisioning
  - Pre-configured guardrails for security and compliance
  - Dashboard for governance visibility
- **Use Case**: Establish a well-architected landing zone before migration
- **Best Practice**: Deploy Control Tower early in the mobilize phase to ensure consistent governance

#### **AWS Service Catalog**
- **Purpose**: Create and manage catalogs of approved IT services
- **Key Features**:
  - Self-service portal for users
  - Version control and governance
  - Cost tracking and budgets
- **Use Case**: Standardize deployments and maintain control during migration
- **Best Practice**: Pre-build service catalog portfolios for common migration patterns

#### **AWS Migration Playbook**
- **Purpose**: Structured guidance for large-scale migrations
- **Key Components**:
  - Initial assessment and planning
  - Wave planning methodology
  - Implementation steps and best practices
- **Use Case**: Follow proven methodologies for enterprise migrations
- **Best Practice**: Adapt the playbook to your organization's specific needs and compliance requirements

---

### 🚀 **Workload Migration**

#### **AWS Application Migration Service (MGN)**
- **Purpose**: Automates "lift-and-shift" (rehost) migrations with minimal downtime
- **Key Features**:
  - Continuous block-level replication
  - Automated conversion and launch
  - Cutover with minutes of downtime
  - Supports physical, virtual, and cloud-based servers
- **Migration Types**: Rehost (lift-and-shift)
- **Use Case**: Migrate servers from VMware, Hyper-V, physical servers, or other clouds to AWS
- **Best Practice**: Test cutover windows in non-production environments first; use MGN's built-in testing capabilities

#### **Amazon Elastic VMware Service (Amazon EVS)**
- **Purpose**: Run VMware workloads natively on AWS
- **Key Features**:
  - VMware Cloud Foundation on AWS infrastructure
  - Hybrid cloud integration
  - Use existing VMware tools and skills
- **Use Case**: Migrate VMware environments without refactoring
- **Best Practice**: Ideal for organizations with significant VMware investments and expertise

---

### 💾 **Data Migration**

#### **AWS Database Migration Service (DMS)**
- **Purpose**: Migrate relational databases, data warehouses, NoSQL databases, and other data stores
- **Key Features**:
  - Homogeneous migrations (e.g., Oracle to Oracle)
  - Heterogeneous migrations (e.g., SQL Server to Aurora)
  - Continuous data replication for minimal downtime
  - Schema conversion with AWS Schema Conversion Tool (SCT)
- **Supported Sources**: Oracle, SQL Server, MySQL, PostgreSQL, MongoDB, SAP, and more
- **Supported Targets**: Amazon RDS, Aurora, Redshift, DynamoDB, S3, and more
- **Use Case**: Database migrations with near-zero downtime
- **Best Practice**: Use DMS with Schema Conversion Tool for heterogeneous migrations; test thoroughly with production-like data volumes

#### **AWS DataSync**
- **Purpose**: Simplifies and accelerates moving large amounts of data to AWS
- **Key Features**:
  - Up to 10x faster than open-source tools
  - Automated scheduling and monitoring
  - Data verification and integrity checks
  - Supports NFS, SMB, HDFS, and object storage
- **Use Case**: Migrate file storage, big data lakes, or media workflows
- **Best Practice**: Use DataSync for ongoing data synchronization during migration windows

#### **AWS Storage Gateway**
- **Purpose**: Hybrid cloud storage with on-premises caching
- **Key Features**:
  - File Gateway for NFS/SMB access to S3
  - Volume Gateway for block storage
  - Tape Gateway for backup applications
- **Use Case**: Bridge on-premises applications with cloud storage during migration
- **Best Practice**: Use as a transitional architecture during phased migrations

#### **AWS Transfer Family**
- **Purpose**: Fully managed file transfer service
- **Key Features**:
  - Support for SFTP, FTPS, and FTP protocols
  - Direct integration with Amazon S3 and EFS
  - Built-in authentication (Active Directory, custom identity providers)
- **Use Case**: Migrate file transfer workflows without changing client applications
- **Best Practice**: Ideal for replacing legacy FTP servers with managed cloud services

#### **AWS Snow Family**
- **Purpose**: Physical data migration devices for large-scale or offline data transfers
- **Products**:
  - **Snowcone**: 8 TB usable storage for edge computing and data transfer
  - **Snowball Edge**: 80 TB or 210 TB for data transfer and edge computing
  - **Snowmobile**: Exabyte-scale data transfer (up to 100 PB per Snowmobile)
- **Use Case**: Migrate petabytes of data when network transfer is impractical
- **Best Practice**: Use Snow Family when data volume exceeds 10 TB or network bandwidth is limited

---

### 🌐 **Connectivity**

#### **AWS Direct Connect**
- **Purpose**: Establishes dedicated, private network connection from on-premises to AWS
- **Key Features**:
  - Consistent network performance
  - Reduced bandwidth costs
  - Private connectivity to VPCs
  - Speeds from 50 Mbps to 100 Gbps
- **Use Case**: High-throughput data migration and hybrid cloud architectures
- **Best Practice**: Establish Direct Connect early in the mobilize phase for large data migrations; use with VPN for redundancy

---

### 📊 **Tracking and Governance**

#### **AWS Systems Manager**
- **Purpose**: Unified interface for operational management
- **Key Features**:
  - Inventory and patch management
  - Automation runbooks
  - Session Manager for secure access
  - Parameter Store for configuration management
- **Use Case**: Manage both on-premises and AWS resources during migration
- **Best Practice**: Deploy SSM agents on source servers for better visibility and automation

#### **Amazon CloudWatch**
- **Purpose**: Monitoring and observability service
- **Key Features**:
  - Metrics, logs, and alarms
  - Application and infrastructure monitoring
  - Custom dashboards
- **Use Case**: Monitor migration progress and application performance
- **Best Practice**: Set up CloudWatch dashboards before migration to establish performance baselines

---

## Migration Strategies (The 7 Rs)

1. **Rehost** (Lift-and-shift) - AWS MGN, VMware on AWS
2. **Replatform** (Lift-tinker-and-shift) - AWS MGN + minor optimizations
3. **Repurchase** (Drop-and-shop) - Move to SaaS
4. **Refactor/Re-architect** - Rebuild using cloud-native services
5. **Retire** - Decommission unnecessary applications
6. **Retain** - Keep in source environment
7. **Relocate** - Move to AWS without changes (VMware Cloud on AWS)

---

## Amazon Q Integration for Cloud Migration

**Amazon Q** is AWS's generative AI-powered assistant that can significantly accelerate your cloud migration journey:

### **Amazon Q for Migration Planning**
- Ask natural language questions about AWS migration services
- Get personalized recommendations based on your workload characteristics
- Receive guidance on best practices and migration strategies
- Troubleshoot migration issues with contextual assistance

### **Example Amazon Q Queries**
- "What's the best way to migrate a SQL Server database to AWS with minimal downtime?"
- "How do I set up AWS Migration Hub for tracking multiple application migrations?"
- "What are the prerequisites for using AWS Application Migration Service?"
- "Compare AWS DataSync vs AWS Transfer Family for my use case"
- "Generate a migration plan for a VMware environment with 200 VMs"

### **Amazon Q Developer**
- Automate code generation for migration scripts
- Generate Infrastructure as Code (CloudFormation, Terraform) for landing zones
- Code reviews and security scanning for migrated applications
- Assist with application modernization and refactoring

### **Best Practice**: Leverage Amazon Q throughout your migration journey for real-time guidance, documentation lookup, and troubleshooting assistance.

---

## Migration Best Practices

### **1. Start Small, Think Big**
- Begin with a pilot migration (low-risk workload)
- Learn from the pilot before scaling
- Build confidence and refine processes

### **2. Use Migration Hub as Central Command**
- Track all migrations in one place
- Maintain visibility across teams
- Generate reports for stakeholders

### **3. Automate Everything Possible**
- Use AWS MGN for server migrations
- Leverage AWS DMS for database migrations
- Implement Infrastructure as Code (IaC) with CloudFormation or Terraform

### **4. Plan for Security and Compliance**
- Use AWS Control Tower for governance
- Implement AWS Config rules
- Enable AWS CloudTrail for audit logging
- Validate compliance requirements before migration

### **5. Test, Test, Test**
- Perform test migrations in non-production
- Validate application functionality post-migration
- Test rollback procedures
- Conduct performance benchmarking

### **6. Establish a Landing Zone First**
- Set up AWS Control Tower
- Configure networking (VPC, subnets, Direct Connect)
- Implement identity and access management
- Enable monitoring and logging

### **7. Create Migration Waves**
- Group applications by dependencies
- Prioritize based on business value and risk
- Plan cutover windows carefully
- Have rollback plans ready

### **8. Invest in Training**
- Complete AWS migration training courses
- Consider AWS Migration Competency Partners
- Leverage AWS Professional Services or partners
- Use Amazon Q for on-demand learning

---

## Migration Phases - Detailed Workflow

### **Phase 1: Assess (2-6 weeks)**
1. Deploy AWS Application Discovery Service
2. Run Migration Evaluator for business case
3. Complete Migration Readiness Assessment
4. Identify migration strategies for each application
5. Build initial TCO and migration roadmap

### **Phase 2: Mobilize (4-12 weeks)**
1. Design and deploy landing zone with AWS Control Tower
2. Establish connectivity (Direct Connect, VPN)
3. Set up AWS Migration Hub
4. Create migration factory processes
5. Train teams and establish governance
6. Build migration wave plans

### **Phase 3: Migrate and Modernize (3-18+ months)**
1. Execute pilot migration
2. Refine processes based on lessons learned
3. Execute migration waves
4. Validate applications post-migration
5. Decommission on-premises resources
6. Optimize and modernize workloads

---

## Key Performance Indicators (KPIs)

Track these metrics to measure migration success:

- **Migration velocity**: Number of workloads migrated per week
- **Downtime**: Actual vs. planned downtime during cutover
- **Cost savings**: TCO reduction vs. baseline
- **Application performance**: Response times before and after migration
- **Security posture**: Compliance and security findings
- **Staff productivity**: Time to perform operational tasks

---

## Common Migration Challenges and Solutions

| Challenge | Solution |
|-----------|----------|
| Network bandwidth limitations | Use AWS Snow Family or Direct Connect |
| Legacy application dependencies | Use Application Discovery Service for dependency mapping |
| Database migration complexity | Leverage AWS DMS with Schema Conversion Tool |
| Downtime constraints | Implement continuous replication with AWS MGN/DMS |
| Lack of cloud skills | Invest in training, use Amazon Q, engage AWS partners |
| Security and compliance concerns | Deploy Control Tower, enable Config rules, use AWS Audit Manager |

---

## Getting Started

### **Step 1: Assess Your Environment**
```bash
# Deploy AWS Application Discovery Service agent
# Or use agentless discovery via connector
```

### **Step 2: Build Your Business Case**
- Request a Migration Evaluator assessment
- Calculate TCO using AWS Pricing Calculator
- Identify quick wins and long-term goals

### **Step 3: Design Your Landing Zone**
- Deploy AWS Control Tower
- Set up organizational units and accounts
- Configure networking and security baselines

### **Step 4: Execute Pilot Migration**
- Select a low-risk, low-complexity workload
- Use AWS MGN or AWS DMS as appropriate
- Document lessons learned

### **Step 5: Scale Migration**
- Apply learnings from pilot
- Execute migration waves
- Continuously optimize and modernize

---

## Additional Resources

- **AWS Migration Hub**: https://aws.amazon.com/migration-hub/
- **AWS Prescriptive Guidance**: https://aws.amazon.com/prescriptive-guidance/
- **AWS Migration Acceleration Program (MAP)**: https://aws.amazon.com/migration-acceleration-program/
- **AWS Training**: https://aws.amazon.com/training/
- **Amazon Q**: https://aws.amazon.com/q/

---

## Conclusion

AWS provides a comprehensive portfolio of migration tools and services designed to support every phase of your cloud journey. By following the structured Assess-Mobilize-Migrate framework, leveraging Amazon Q for real-time assistance, and utilizing purpose-built services like AWS MGN, DMS, and Migration Hub, organizations can achieve successful migrations with reduced risk, minimized downtime, and optimized costs.

**Remember**: Every migration is unique. Tailor this portfolio to your specific requirements, and don't hesitate to engage AWS Professional Services or AWS Migration Competency Partners for additional support.

---

*Document Version: 1.0*  
*Last Updated: November 12, 2025*  
*Maintained by: AWS Cloud Migration Team*
