# 1.1 Compare and contrast various types of security controls

First, there are four categories of security controls, and each one needs the others to be effective.

## 1.1.1 Categories of security controls

### 1.1.1.1 Technical Controls
Technologies, hardware, or software to protect the system and data automatically or through enforced rules.  
*Examples:* Firewalls, VPN, antivirus software, MFA, data encryption.

### 1.1.1.2 Managerial Controls (Administrative Controls)
Human-driven efforts involving guidelines, policies, and procedures to supervise and manage the information system.  
*Examples:* Security awareness training, incident response plans.

### 1.1.1.3 Operational Controls
Rely on people rather than automated systems to protect assets.  
*Examples:* Security guards, user account management, change management.

### 1.1.1.4 Physical Controls
Facilities and hardware that limit physical access to rooms, systems, or devices.  
*Examples:* Locks, alarm systems, surveillance cameras.

---

## 1.1.2 Types of security controls

### 1.1.2.1 Preventive
Blocks access to a resource.  
*Examples:* Firewall rules, security guard checks.

### 1.1.2.2 Deterrent
Makes an attacker think twice.  
*Examples:* Splash screens, warning signs.

### 1.1.2.3 Detective
Identifies or alerts when a breach has occurred.  
*Examples:* Motion detectors, reviewing login reports.

### 1.1.2.4 Corrective
Applies controls after an event to reverse its impact.  
*Examples:* Policies for reporting issues, backup recovery.

### 1.1.2.5 Compensating Controls
Alternative controls when primary controls are not feasible, providing comparable security.  
*Examples:* Additional monitoring, manual processes in place of automated tools.

### 1.1.2.6 Directive Controls
Rules or instructions guiding user behavior to maintain security.  
*Examples:* Acceptable use policies, security guidelines.

---

*Sources:*  
- [infosectrain.com](https://www.infosectrain.com)  
- [professormesser.com](https://www.professormesser.com)
# 1.2 Summarize fundamental security concepts

## 1.2.1 CIA : Confidentiality, Integrity, and Availability
- Confidentiality: means ensure that the information is only accessible to authorized individuals.  
examples: access controls, encrypting the data.  
- Integrity: insuring that the information is complete , consistent , and has not been played with.  
examples: hashing …  
- Availability: ensuring that the information is always accessible when needed.

## 1.2.2 Non-repudation
- It means prevent pesons from denying actions they comit.  
For example digital signatures.

## 1.2.3 Authenticating, Authorization, and Accounting (AAA)

### 1.2.3.1 Authenticating people
- it means verifying the identity of the people who are using the device.  
for example: passwords, biometrics and MFA.

### 1.2.3.2 Authenticating systems
- it means verifying that the devices have the authorisation to access to the network and it can be done by the CAs and the mutual TLS

### 1.2.3.3 Authorization models
- it determine who can and what can do and under what conditions, the most common models are (RBAC) role based access control…

## 1.2.4 Gap analysis
- It’s the process of comparing the current security posture of an organisation against the desires one.  
to make it more simple it is to compare where we are and what we have vs what we want to have .

## 1.2.5 Zero trust

### 1.2.5.1 control plane
- control plane is the part of the network that controls where and how the data should be transferred.  
- adaptive identity: it means when a user tries to gain the access from an unknown network he should verify himself twice than trying to gain access from a known network.  
- Threat scope identity: it means reduce the maximum the access points (the number of systems, users and services) because with more possible access point the risk of being hacked get more, reduce the possible access surface.  
- policy-driven access control: it means u cant access an app unless u have the role to, for example only the finance department staff can access the payroll app, and only the HR department can access the infos of the staff.  
- Policy administrator: it is simply the o power that aplies the laws and the policies that were made by the engine administrator  
- engine administrator : it is te brain or the power that generate the laws and the policies.

### 1.2.5.2 Data plane
- The data plane is the part of the network that actually moves the data packets where the control plane decides.  
- Implicite trust zones : it means the zones and areas of a networkthat are assumed to be trusted by default but in reality its risky because zero trust approach is more recommended.  
- Subject / System: the subject is the who or what wants to access while the system (object) is what is being accessed.  
- Policy Enforcement Point : is the place in a system or a network that applies the access control policies, its like a door guard , he decides who can or can not have the access based on the laws and the policies.
### 1.2.6 Deception and disruption
- **Honeypots technique**: a strategy where you let attackers get access to a fake part of your system so you can know what techniques they are trying to use against you. By the end, you will know exactly how to better protect your system.  
- **Honeynet**: simply a network that is composed of multiple honeypots.  
- **Honeyfiles**: fake important files that attackers may find very interesting. You can name them with names attackers may find interesting, like `passwords.txt`.  
- **Honeytoken**: any fake data that can be tracked when it’s used by the attacker.  

---

### 1.3 Explain the importance of change management processes and the impact to security  

#### 1.3.1 Business processes impacting security operation  

##### 1.3.1.1 Approval process
Before any security or IT change is applied (like a firewall update …) the right authority must approve it.  

##### 1.3.1.2 Ownership
The owners are the ones managing the process. That doesn’t mean they do the change themselves, but it means they stay informed, and once it’s complete, they are responsible for testing their systems.  

##### 1.3.1.3 Stakeholders
They are the individuals or the departments that will be impacted by the changes. It’s not easy because a very small change can affect a large number of staff.  

##### 1.3.1.4 Impact analysis
This means determining the risk value. It can be minor or far-reaching. For example, while trying to apply a change, we may lose everything else. Also, we need to analyze the risk of not doing the change.  

##### 1.3.1.5 Test results
Using a sandbox environment can be useful because we can apply the changes and see if something unexpected happens. Also, we can test the backout plan if anything goes wrong.  

##### 1.3.1.6 Back out plan
Means having a plan to delete the changes and go back to the previous version if anything goes wrong.  

##### 1.3.1.7 Maintenance window
Changes should be applied at specific times when the system has the least amount of use, like weekends and evenings, to minimize disruption.  

---

#### 1.3.2 Technical implications  

##### 1.3.2.1 Allow list / deny list
- **Allow list**: only permits approved apps to work.  
- **Deny list**: all apps are allowed except the ones that are black-listed.  

##### 1.3.2.2 Restricted activities
The organization should decide if there are some specific activities that should be stopped or restricted before, after, or during the changes.  

##### 1.3.2.3 Downtime
A change may cause a blockage for some systems.  

##### 1.3.2.4 Service restart
Some changes require restarting to take effect, for example changes in the database.  

##### 1.3.2.5 App restart
Some changes may need the whole app to restart, not just a service.  

##### 1.3.2.6 Dependencies
All possible dependencies must be identified and documented.  

