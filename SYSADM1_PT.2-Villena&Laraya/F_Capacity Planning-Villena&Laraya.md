
![SYSADM PT Header](https://github.com/user-attachments/assets/7a268670-5951-4417-b890-e85918c2e16b)

# **SYSADM1 – Capacity Management & Planning**

**Part 2\. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the expected surge in traffic, analyze the provided network topology diagram. Identify potential bottlenecks and areas where scalability might be a concern. Propose specific strategies to improve the network's scalability and performance to ensure a seamless user experience during the peak traffic period. Consider factors such as increased user demand, new applications, and security threats.

![image](https://github.com/user-attachments/assets/6c71c0d5-8d70-4b2e-b5fc-181339b21041)

**Documented Report: E-Commerce Network Scalability Analysis**

**Network Analysis**

The old network topology was a straightforward design that connected a single internet gateway to one router, which served as the central point for all network traffic. This router was linked to a core/distribution switch that handled traffic routing and distribution across the network. From there, the core switch connected to three access switches, each dedicated to a specific VLAN. VLAN 1 hosted three servers, each paired with two PCs, while VLANs 2 and 3 each contained two servers, also paired with two PCs each. However, this design had several limitations. It relied heavily on a single router and core switch, creating a single point of failure that could disrupt the entire network if either device failed. The lack of redundancy made it prone to downtime, while the core switch became a bottleneck for inter-VLAN traffic during high usage periods. Additionally, the absence of firewalls or a DMZ zone left servers exposed to potential security threats. This nonflexible structure, with each switch statically assigned to a VLAN, also limited scalability and efficient resource allocation. Overall, while functional for basic operations, the old topology struggled to meet the demands of scalability, security, and fault tolerance.

**Scalability Planning**

To address these challenges, we propose the following solutions:

* **Link Aggregation:** Combine multiple links between core and distribution switches using EtherChannel technology to double or triple the available bandwidth. This solution would cost approximately ₱50,000 to ₱100,000 for additional hardware and configuration.  
    
* **Server Load Balancing**: Install hardware or software-based load balancers in the DMZ zone to distribute user requests across multiple servers. This would improve performance and fault tolerance. Estimated cost is ₱200,000 to ₱300,000, depending on the brand and features.  
    
* **Firewall Upgrade**: We’ve added a new, high-performance firewall to enhance security, with capabilities for DDoS mitigation and advanced threat detection. The cost for this installation ranges from ₱150,000 to ₱250,000.  
    
* **Cloud Integration**: Offload key services like backups and web hosting to a cloud platform such as AWS or Azure, ensuring elastic scalability. Monthly operational costs would range from ₱10,000 to ₱30,000 depending on usage.  
    
* **Quality of Service (QoS)**: Configure QoS policies to prioritize critical traffic like database queries and web traffic, ensuring minimal disruption to essential services. This would primarily require technical expertise, costing ₱20,000 to ₱40,000 for setup.  
    
* **Triple ISP Connection**: Add two more ISP for improved network scalability, reliability, and redundancy. This solution enhances bandwidth, provides automatic failover during outages, and allows better load distribution. The setup cost would depend on the provider but is estimated to range from ₱50,000 to ₱100,000, including installation and configuration.

**Evaluation of Solutions**

To meet growing demands and ensure the network can scale effectively, a combination of hardware upgrades, software configurations, and network optimizations is key. Upgrading to high-performance core and distribution switches will boost the network’s capacity, while adding advanced firewalls with DDoS protection and threat detection will enhance security. Dynamic routing protocols like OSPF or BGP will improve traffic flow and provide redundancy, ensuring the network adapts to changing needs. Introducing VPN services will support secure remote access for an increasingly mobile workforce, and integrating cloud-based solutions for backup and scalability will offer flexibility, reducing reliance on physical infrastructure. Additionally, setting up Quality of Service (QoS) policies will help prioritize critical traffic, improving performance during peak usage times. With an estimated cost of ₱600,000 to ₱1,000,000, these upgrades will strengthen the network’s performance, security, and scalability, providing long-term reliability and positioning the system for future growth.

**Proposed Design Justification**

The proposed network design is well-justified as it incorporates scalability, security, and redundancy to address current and future needs. At the core of the design is a layered architecture that optimizes traffic flow, ensures fault tolerance, and facilitates efficient management. The integration of redundant core switches, dynamic routing protocols such as OSPF or BGP, and VLAN trunking provides the scalability needed to handle traffic surges while maintaining high availability. Security is bolstered with advanced Cisco solutions, including TrustSec for network segmentation, Secure Group Tags (SGTs) for policy enforcement, and Cisco ISE for centralized identity management. The DMZ is enhanced with dual firewalls, load balancers, and intrusion prevention systems (IPS), safeguarding critical services like web and DNS servers.

Additionally, the inclusion of a VPN ensures secure remote access, while cloud services offer flexible scalability and automated backups to mitigate the risks of data loss or downtime. Monitoring tools like SolarWinds or Nagios provide proactive management, ensuring real-time insights and rapid response to potential issues. This design is not only robust but also cost-effective, with an estimated investment of ₱800,000 to ₱1,300,000, offering long-term benefits such as reduced downtime, enhanced security, and seamless scalability. It is a future-proof solution that prioritizes reliability, security, and performance to meet the demands of modern networks effectively.

**Proposed Design**  

![Network Topology SS](https://github.com/user-attachments/assets/91fec830-ecd4-4ccf-91b3-2728ed5fe655)

*Figure 1\. Proposed Network Topology Design*

**1\. Network Enhancements:**

* **Core Layer:** Introduce redundant core switches to eliminate single points of failure and configure dynamic routing protocols (OSPF or BGP) for better fault tolerance.  
* **Distribution Layer:** Expand VLAN uplinks using EtherChannel to increase bandwidth and ensure link redundancy.  
* **DMZ Zone:** Add load balancers to distribute traffic efficiently across web, DNS, and application servers.  
* **Triple ISP Connection**: Added 2 additional ISP to the network to increase internet bandwidth, improve redundancy, and ensure failover capabilities. This will allow the network to automatically switch to a backup connection in case one ISP experiences an outage, ensuring continuous uptime and a more resilient infrastructure.  
* **Access Layer:** Upgrade to higher-capacity switches and apply QoS (Quality of Service) policies to prioritize critical services such as payment gateways and remote connections.  
* **VPN Integration:** Implement a Virtual Private Network (VPN) to provide secure and encrypted remote access for employees and partners, ensuring data confidentiality over external connections. Estimated cost: ₱100,000 to ₱150,000.  
* **Cloud Services:**  
  * *Cloud Scalability:* Migrate critical applications to a cloud-based platform to handle peak traffic demands.  
  * *Cloud Backup*: Implement a cloud-based backup solution for all essential data, reducing the risk of data loss and ensuring recovery during disasters. Estimated cost for cloud services: ₱200,000 to ₱300,000 annually.

	

**2\. Implementation Plan:**

* ***Phase 1***: Upgrade core and distribution switches, and implement *VLAN trunking and Spanning Tree Protocol (STP)* to ensure efficient data flow and prevent network loops. This phase also includes the additional two ISP for enhanced redundancy and failover protection. Estimated cost: ₱300,000 to ₱450,000.  
* ***Phase 2***: Install *load balancers, VPN, and IPS systems* in the DMZ zone to optimize traffic distribution and secure access to critical services.. Estimated cost: ₱350,000 to ₱450,000.  
* ***Phase 3***: Migrate applications and data to *the cloud, configure automated cloud backups, and perform system-wide tests* to ensure redundancy and scalability. Estimated cost: ₱200,000 to ₱300,000.

**3\. Security:** 

Enhancing the network's security and performance involves deploying advanced Cisco technologies that cater to modern needs. Cisco TrustSec offers a practical solution by creating scalable, software-defined segmentation based on user and device identities, ensuring secure and efficient traffic flow across the network. To complement this, Secure Group Tags (SGTs) allow for dynamic segmentation, ensuring that traffic is managed and policies are enforced based on specific roles or devices. Cisco Identity Services Engine (ISE) takes this further by centralizing identity management, giving administrators more control over access and enabling policy enforcement tailored to user roles. For protection against threats, Cisco Firepower Threat Defense (FTD) provides real-time threat intelligence and automated responses, keeping the network secure from potential vulnerabilities. To maintain optimal performance and identify issues before they escalate, tools like SolarWinds or Nagios can provide real-time monitoring and actionable insights. These enhancements are estimated to cost between ₱150,000 and ₱250,000, offering a strong balance between security, reliability, and investment value.

	

**Evaluation and Justification**

The proposed network design effectively addresses the key challenges of scalability, security, and redundancy, creating a robust and future-ready infrastructure. By incorporating Cisco technologies like TrustSec, Secure Group Tags (SGT), and Identity Services Engine (ISE), the design ensures that security is tightened through identity-based access control and dynamic segmentation. This setup ensures that only authorized users and devices can access specific parts of the network, significantly reducing the risk of security breaches. A VPN further strengthens data protection by providing encrypted remote access for employees and partners, safeguarding sensitive information during transit. To handle peak traffic, load balancers distribute workloads efficiently across servers, ensuring smooth and uninterrupted performance.

Migrating critical applications to cloud platforms and implementing automated cloud backup solutions enhance disaster recovery and scalability, which are vital for maintaining continuous service in an e-commerce setting. Real-time monitoring tools like SolarWinds or Nagios add another layer of reliability, enabling proactive management by quickly identifying and addressing potential network issues.

Although the estimated cost of ₱800,000 to ₱1,300,000 represents a significant investment, it is justified by the long-term benefits. These upgrades will minimize downtime, boost operational efficiency, improve user satisfaction, and ensure the network can handle future growth with ease. By integrating advanced Cisco technologies, cloud-based solutions, and reliable redundancy measures, the network will deliver high performance and security, even under heavy traffic conditions. This makes it a strategic investment for sustained business success and customer trust.

![image](https://github.com/user-attachments/assets/7bc3f5dc-d3f6-4f04-9633-0e3af5c5d27e)
