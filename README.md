# AWS VPC with Public & Private Subnets + NAT Gateway 🚀

A secure cloud networking architecture built using **Amazon VPC** containing:
- Public Subnet → Internet access using Internet Gateway (IGW)
- Private Subnet → Outbound-only internet access using NAT Gateway
- Secure EC2 connectivity using Session Manager (no public IP)

🔗 GitHub Repo: https://github.com/Srimaha02/aws-vpc-nat-project

---



## 🛠️ Services Used

| AWS Service | Purpose |
|------------|---------|
| VPC | Secure private network |
| Public + Private Subnets | Segregated network tiers |
| Internet Gateway | Internet for public subnet |
| NAT Gateway | Internet for private subnet (no inbound) |
| EC2 Instances | Testing network access |
| SSM Session Manager | Private EC2 access w/o keys |
| Route Tables | Traffic routing |

---


## 🔒 Security Highlights

✔ Private instance **cannot** be accessed from Internet  
✔ Outbound internet only via NAT  
✔ SSH only allowed from Public EC2 → Private EC2  
✔ Private EC2 accessible via SSM (no key needed)

---

## 🧪 Test Performed

On **private EC2**, executed:

```bash
curl https://www.google.com
Result: HTML response from Google → NAT working ✔

🧹 Cleanup (to avoid charges)
✔ Terminate EC2 instances
✔ Delete NAT Gateway
✔ Release Elastic IPs
✔ Delete VPC + components

🎯 Key Learnings
How to build a secure network in AWS

Routing logic with NAT Gateway + IGW

Private workload security best practices

EC2 Session Manager access method (no SSH keys)

🔮 Future Enhancements
✨ Add Load Balancer and 2-tier app
✨ Add monitoring (CloudWatch)
✨ Use Terraform to automate architecture deployment

👩‍💻 Author
Srimahalakshmi R
Cloud Enthusiast | AWS Learner
📍 India
🔗 LinkedIn: https://www.linkedin.com/in/sri-mahalakshmi-922901336
