# Implement Identities in Azure AD (20–25%)

## Configure and Manage an Azure AD Tenant

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Configure and manage Azure AD roles | Role-based access control | Azure AD RBAC | Fine-grained access control | Complexity in role management | Inappropriate role assignments | Free, P1, P2 |  |
| Configure delegation using administrative units | Delegating admin tasks within organizational units | Azure AD Administrative Units | Delegation of control | Limited to specific tasks and roles | Delegation to untrusted entities | P1, P2 | Ensure that the group has a group owner. |
| Analyze Azure AD role permissions | Ensuring proper permissions alignment | Azure AD roles and permissions analysis | Insight into permissions | Requires specialized tools | Overly permissive roles |  | Typical questions about least privilege. [Link](https://learn.microsoft.com/en-us/azure/active-directory/roles/delegate-by-task) |
| Configure and manage custom domains | Aligning Azure AD with organizational domain names | Azure AD custom domain configuration | Brand alignment | DNS management complexity | Domain-related vulnerabilities | Free, P1, P2 | Typical questions around verification, primary domain, and domain removal. Understand terms like CNAME, TXT, MX, A/AAAA, etc. |
| Configure tenant-wide settings | Global configuration for tenant behavior | Azure AD tenant-wide settings configuration | Centralized control | Limited flexibility | Misconfiguration affecting entire tenant |  |  |

## Create, Configure, and Manage Azure AD Identities

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Create, configure, and manage users | Managing user identities | Azure AD user management | Centralized identity management | Complexity in managing users | Unauthorized access, identity theft | Free, P1, P2 |  |
| Create, configure, and manage groups | Managing group access | Azure AD group management | Group-based access control | Complexity in managing groups | Unauthorized group access | Free, P1, P2 |  |
| Configure and manage device join and registration | Device management | Azure AD device management | Device control, Conditional Access | Complexity in device management | Unauthorized device access | P1, P2 |  |
| Assign, modify, and report on licenses | License management | Azure AD license management | Efficient license allocation | Complexity in license management | License misuse | P1, P2 | Management of licenses in groups. PowerShell commands like “Set-MsolUserLicense”. |

## Implementing and Managing External Identities

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Manage external collaboration settings in Azure AD | External collaboration | Azure AD B2B collaboration | Collaboration enablement | Complexity in management | External collaboration risks | Free, P1, P2 |  |
| Invite external users, individually or in bulk | Inviting external users | Azure AD invitations | Bulk invitations | Managing external users | Security risks with external users | Free, P1, P2 |  |
| Manage external user accounts in Azure AD | Managing external user accounts | Azure AD external user management | Control over external users | Complexity in managing | Unauthorized external access | Free, P1, P2 |  |
| Configure identity providers, including SAML or WS-fed | Identity federation | Azure AD identity providers | Identity federation | Complexity in configuration | Federation vulnerabilities | P1, P2 |  |

## Implementing and Managing Hybrid Identity

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Implement and manage Azure AD Connect | Hybrid identity | Azure AD Connect | Integration with on-premises | Complexity in setup | Synchronization errors | Free, P1, P2 |  |
| Implement and manage Azure AD Connect cloud sync | Cloud synchronization | Azure AD Connect cloud sync | Cloud-based synchronization | Complexity in setup | Synchronization errors | Free, P1, P2 | Preferred method going forward. |
| Implement and manage Password Hash Synchronization (PHS) | Password synchronization | Azure AD PHS | On-premises password synchronization + High availability | Additional infrastructure requiring the same protection level as DC | Password-related vulnerabilities | Free, P1, P2 | Limitation: Doesn’t work if additional User-level security policies are required. |
| Implement and manage Pass-Through Authentication (PTA) | Authentication management | Azure AD PTA | On-premises authentication | Complexity in management | Authentication-related vulnerabilities, Denial of Service | Free, P1, P2 | Should be used with PHS for failover or DR. (This is not automatic) |
| Implement and manage seamless Single Sign-On (SSO) | Single sign-on | Azure AD SSO | Seamless authentication | Complexity in setup | SSO-related vulnerabilities | Free, P1, P2 |  |
| Implement and manage Federation | Federation management | Azure AD Federation | Federation with other identity providers + custom attributes | Complexity in setup | Federation-related vulnerabilities | P1, P2 | Should be used with PHS for failover or DR. (This is not automatic) |
| Implement and manage Azure AD Connect Health | Health monitoring | Azure AD Connect Health | Monitoring and insights | Complexity in setup | Misconfiguration risks | P1, P2 |  |
| Troubleshoot synchronization errors | Error troubleshooting | Azure AD troubleshooting tools | Tools for diagnosing synchronization errors | Complexity in troubleshooting | Misconfiguration risks |  |  |

# Implement Authentication and Access Management (25–30%)

## Planning, Implementing, and Managing Azure Multifactor Authentication (MFA) and Self-Service Password Reset

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Plan Azure MFA deployment, excluding MFA Server | Enhancing security with 2-factor authentication | Conditional Access/ Windows Hello/ Windows Hello for Business | Increased security | Complexity in setup | MFA bypass risks | Free, P1, P2 |  |
| Configure and deploy self-service password reset | Allowing users to reset passwords themselves | Azure AD self-service password reset (SSPR) | User convenience | Potential abuse | Account compromise if not properly secured | Free, P1, P2 |  |
| Implement and manage Azure MFA settings | Customizing MFA for organizational needs | Azure MFA settings | Flexibility in MFA configuration | Complexity in management | Misconfiguration risks | P1, P2 |  |
| Manage MFA settings for users | Individual user MFA settings | Azure MFA user settings | User-specific MFA settings | Complexity in managing users | Inconsistent user settings | P1, P2 | Smart Lockout: Locks out a user after 10 attempts - same password does not count.  |
| Extend Azure AD MFA to third-party and on-premises devices | Extending MFA to other systems | Azure MFA extensions | MFA across various platforms | Integration challenges | Security risks with third-party integrations | P1, P2 |  |
| Monitor Azure AD MFA activity | Monitoring MFA usage and activity | Azure AD MFA monitoring | Insights into MFA usage | Complexity in monitoring | Lack of monitoring may lead to unnoticed issues | P1, P2 |  |

## Planning, Implementing, and Managing Azure AD Conditional Access

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Plan conditional access policies | Planning access controls | Azure AD conditional access planning | Strategic alignment with access needs | Complexity in planning | Inadequate planning leads to access issues | P1, P2 | Remember to turn off Security Defaults. |
| Implement conditional access policy assignments | Assigning access policies | Azure AD conditional access assignments | Fine-grained access control | Complexity in assignments | Misassignment risks | P1, P2 |  |
| Implement conditional access policy controls | Controlling access based on policies | Azure AD conditional access controls | Dynamic access control | Complexity in controls | Misconfiguration risks | P1, P2 |  |
| Test and troubleshoot conditional access policies | Testing access policies | Azure AD conditional access testing | Ensuring policy effectiveness | Complexity in testing | Ineffective policies if not tested | P1, P2 |  |
| Implement session management | Managing user sessions | Azure AD session management | Control over user sessions | Complexity in management | Session hijacking risks | P1, P2 |  |
| Implement device-enforced restrictions | Device-based access restrictions | Azure AD device restrictions | Device-level access control | Complexity in restrictions | Device-related access risks | P1, P2 |  |
| Implement continuous access evaluation | Continuous access checks | Azure AD continuous access evaluation | Real-time access evaluation | Complexity in implementation | Lack of continuous evaluation leads to risks | P1, P2 |  |
| Create a conditional access policy from a template | Using templates for access policies | Azure AD conditional access templates | Simplified policy creation | Limited customization | Template-related risks | P1, P2 |  |

## Managing Azure AD Identity Protection

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Implement and manage a user risk policy | Managing risks associated with users | Azure AD user risk policy | Proactive risk management | Complexity in management | Unmanaged user risks | P2 |  |
| Implement and manage sign-in risk policy | Managing sign-in risks | Azure AD sign-in risk policy | Protection against suspicious sign-ins | Complexity in management | Unmanaged sign-in risks | P2 |  |
| Implement and manage MFA registration policy | Enforcing MFA registration | Azure AD MFA registration policy | Enhanced security with MFA | Complexity in policy enforcement | Lack of MFA registration risks | P2 |  |
| Monitor, investigate, and remediate risky users | Monitoring and managing risky users | Azure AD risky user monitoring | Identification and remediation of risky users | Complexity in monitoring | Unnoticed risky users | P2 |  |
| Implement security for workload identities | Securing workloads | Azure AD workload identity security | Security alignment with workloads | Complexity in implementation | Workload-related security risks | P2 |  |

## Implement Access Management for Azure Resources

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Assign Azure roles | Role-based access to Azure resources | Azure RBAC | Fine-grained access control | Complexity in role assignments | Misassignment risks | Free, P1, P2 |  |
| Configure custom Azure roles | Customizing roles for specific needs | Azure custom RBAC roles | Tailored access control | Complexity in custom roles | Custom role-related risks | Free, P1, P2 |  |
| Create and configure managed identities | Managing identities for services | Azure managed identities | Simplified identity management for services | Complexity in configuration | Misconfiguration risks | Free, P1, P2 |  |
| Use managed identities to access Azure resources | Using managed identities for access | Azure managed identity access | Secure and simplified access | Complexity in usage | Misuse of managed identities | Free, P1, P2 |  |
| Analyze Azure role permissions | Analyzing role-based permissions | Azure role permission analysis | Insight into role permissions | Complexity in analysis | Inadequate analysis leads to permission issues | Free, P1, P2 |  |
| Configure Azure Key Vault RBAC and policies | Managing access to Azure Key Vault | Azure Key Vault RBAC and policies | Secure control over secrets and keys | Complexity in configuration | Key Vault access risks | Free, P1, P2 |  |

# Implement Access Management for Applications (15–20%)

## Manage and Monitor Application Access using Microsoft Defender for Cloud Apps

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Discover and manage apps using Microsoft Defender for Cloud Apps | Discovering unauthorized cloud apps in the network | Microsoft Defender for Cloud Apps | Visibility into shadow IT | Complexity in management | Unauthorized app risks | E5 |  |
| Configure connectors to apps | Connecting to various cloud apps | Microsoft Defender connectors | Integration with various apps | Complexity in configuration | Connector-related risks | E5 |  |
| Implement application-enforced restrictions | Enforcing app-specific restrictions | Microsoft Defender app restrictions | Fine-grained app control | Complexity in enforcement | Misconfiguration risks | E5 |  |
| Configure conditional access app control | Conditional access to apps | Azure AD conditional access app control | Dynamic access control | Complexity in configuration | Conditional access risks | E3, E5 |  |
| Create access and session policies in Microsoft Defender for Cloud Apps | Managing access and sessions | Microsoft Defender access policies | Control over access and sessions | Complexity in policy creation | Policy-related risks | E5 |  |
| Implement and manage policies for OAuth apps | Managing OAuth app policies | Microsoft Defender OAuth policies | Control over OAuth apps | Complexity in policy management | OAuth-related risks | E5 |  |

## Plan, Implement, and Monitor Integration of Enterprise Applications

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Configure and manage user and admin consent | Managing consent for app access | Azure AD consent management | Control over app access consent | Complexity in management | Consent-related risks | Free, P1, P2 |  |
| Discover apps using ADFS application activity reports | Discovering app usage | ADFS activity reports | Insights into app usage | Complexity in reporting | Unnoticed app activity risks | Free, P1, P2 |  |
| Design and implement access management for apps | Designing app access controls | Azure AD app access management | Strategic app access control | Complexity in design | Access control risks | Free, P1, P2 |  |
| Design and implement app management roles | Designing roles for app management | Azure AD app management roles | Role-based app management | Complexity in role design | Role-related risks | Free, P1, P2 |  |
| Monitor and audit activity in enterprise applications | Monitoring app activity | Azure AD app activity monitoring | Visibility into app activity | Complexity in monitoring | Unnoticed app activity risks | Free, P1, P2 |  |
| Design and implement integration for on-premises apps using Azure AD Application Proxy | Integrating on-premises apps | Azure AD Application Proxy | Secure integration with on-premises apps | Complexity in integration | Integration risks | P1, P2 |  |
| Design and implement integration for SaaS apps | Integrating SaaS apps | Azure AD SaaS app integration | Seamless SaaS app integration | Complexity in integration | SaaS integration risks | Free, P1, P2 |  |
| Provision and manage users, groups, and roles on Enterprise applications | Managing identities in Enterprise apps | Azure AD Enterprise app management | Centralized identity management | Complexity in management | Identity-related risks | Free, P1, P2 |  |
| Create and manage application collections | Organizing apps into collections | Azure AD app collections | Organized app management | Complexity in collection management | Collection-related risks | Free, P1, P2 |  |

## Plan and Implement Application Registrations

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Plan for application registrations | Planning app registrations | Azure AD app registration planning | Strategic alignment with app needs | Complexity in planning | Inadequate planning leading to unauthorized access | P1, P2 |  |
| Implement application registrations | Registering apps | Azure AD app registrations | Control over app registrations | Complexity in implementation | Registration-related risks | P1, P2 |  |
| Configure application permissions | Setting app permissions | Azure AD app permissions | Fine-grained permission control | Complexity in configuration | Permission-related risks | P1, P2 |  |
| Implement application authorization | Authorizing apps | Azure AD app authorization | Secure app authorization | Complexity in implementation | Authorization-related risks | P1, P2 |  |
| Plan and configure multi-tier application permissions | Multi-tier app permissions | Azure AD multi-tier permissions | Complex permission structures | Complexity in configuration | Multi-tier permission risks | P1, P2 |  |
| Manage and monitor applications using App governance | Managing and monitoring apps | Azure AD App governance | Oversight and control over apps | Complexity in governance | Governance-related risks | P1, P2 |  |

## Plan and Implement Entitlement Management

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Plan entitlements | Planning access to resources | Azure AD Entitlement Management | Strategic alignment with access needs | Complexity in planning | Inadequate planning leading to unauthorized access | P1, P2 |  |
| Create and configure catalogs | Organizing resources | Azure AD Catalogs | Structured resource management | Complexity in configuration | Misconfiguration leading to exposure of sensitive resources | P1, P2 | Catalogs are a collection of resources and access packages |
| Create and configure access packages | Packaging access for users | Azure AD Access Packages | Simplified access provisioning | Complexity in package creation | Incorrect packaging leading to excessive permissions | P1, P2 |  |
| Manage access requests | Handling access requests | Azure AD Access Requests | Controlled access management | Complexity in request management | Unmanaged requests leading to unauthorized access | P1, P2 |  |
| Implement and manage terms of use | Enforcing terms of use | Azure AD Terms of Use | Legal compliance | Complexity in implementation | Non-compliance with legal requirements | P1, P2 |  |
| Manage the lifecycle of external users in Azure AD Identity Governance settings | External user management | Azure AD Identity Governance | Lifecycle management of external identities | Complexity in lifecycle management | Unmanaged external users leading to potential breaches | P1, P2 |  |
| Configure and manage connected organizations | Managing connected organizations | Azure AD Connected Organizations | Collaboration across organizations | Complexity in connection management | Connection-related risks, such as data leakage | P1, P2 |  |
| Review per-user entitlements using Azure AD Entitlement management | Reviewing user entitlements | Azure AD Entitlement Review | Insight into user entitlements | Complexity in review process | Unreviewed entitlements leading to excessive access | P1, P2 |  |

## Plan, Implement, and Manage Access Reviews

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Plan for access reviews | Planning regular access reviews | Azure AD Access Reviews | Strategic alignment with compliance needs | Complexity in planning | Inadequate planning leading to compliance failures | P1, P2 |  |
| Create and configure access reviews for groups and apps | Reviewing access to groups and apps | Azure AD Group/App Access Reviews | Controlled access to groups and apps | Complexity in review creation | Unreviewed access leading to unauthorized access | P1, P2 |  |
| Create and configure access review programs | Structured access review process | Azure AD Access Review Programs | Organized review process | Complexity in program configuration | Misconfigured programs leading to review failures | P1, P2 |  |
| Monitor access review activity | Monitoring review process | Azure AD Access Review Monitoring | Visibility into review activities | Complexity in monitoring | Unmonitored activities leading to unnoticed issues | P1, P2 |  |
| Respond to access review activity, including automated and manual responses | Responding to review findings | Azure AD Access Review Responses | Timely response to review outcomes | Complexity in response management | Delayed or incorrect responses leading to security risks | P1, P2 |  |

## Plan and Implement Privileged Access

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Plan and manage Azure roles in Privileged Identity Management (PIM) | Role management in PIM | Azure PIM Roles | Fine-grained role control | Complexity in role management | Mismanaged roles leading to unauthorized access | P2 |  |
| Plan and manage Azure resources in PIM | Resource management in PIM | Azure PIM Resources | Controlled resource access | Complexity in resource management | Mismanaged resources leading to potential breaches | P2 |  |
| Plan and configure Privileged Access groups | Planning privileged access | Azure Privileged Access Groups | Strategic privileged access control | Complexity in configuration | Misconfiguration leading to excessive privileges | P2 |  |
| Manage PIM requests and approval process | Managing PIM requests | Azure PIM Requests | Controlled privilege elevation | Complexity in request management | Uncontrolled privilege elevation leading to security risks | P2 |  |
| Monitor PIM roles and activity | Monitoring privileged roles | Azure PIM Role Monitoring | Visibility into privileged role activities | Complexity in monitoring | Unmonitored activities leading to unnoticed issues | P2 |  |
| Configure and manage PIM alerts | Alert management for privileged roles | Azure PIM Alerts | Timely alerts for privileged role activities | Complexity in alert configuration | Lack of alerts leading to delayed response | P2 |  |
| Manage PIM access reviews | Reviewing privileged access | Azure PIM Access Reviews | Controlled review process | Complexity in review management | Mismanaged reviews leading to compliance issues | P2 |  |
| Review PIM role settings and activity | Reviewing PIM role configurations | Azure PIM Role Reviews | Visibility into role configurations | Complexity in review process | Misconfigured roles leading to security risks | P2 |  |
| Implement and manage PIM for Azure AD roles | Role management for Azure AD | Azure AD PIM Roles | Fine-grained role control | Complexity in role management | Mismanaged roles leading to unauthorized access | P2 |  |

## Implement Secure Cloud Solutions (10–15%)

## Manage Security Operations for Identity and Access

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Plan and implement security alerts for identity and access | Managing identity and access alerts | Azure Security Center alerts | Timely alerting for security events | Complexity in planning | Lack of alerting leading to delayed response | P1, P2 |  |
| Respond to and mitigate identity and access security incidents | Incident response for security events | Azure Security Center incident response | Timely incident response | Complexity in response | Ineffective response leading to security breaches | P1, P2 |  |
| Plan and implement security policies for identity and access | Implementing security policies | Azure Security Center policies | Improved security posture | Complexity in policy implementation | Misconfigured policies leading to security gaps | P1, P2 |  |
| Monitor identity and access security by using Azure Security Center | Monitoring identity and access security | Azure Security Center monitoring | Visibility into security events | Complexity in monitoring | Lack of monitoring leading to unnoticed security incidents | P1, P2 |  |
| Monitor security by using Azure Monitor | Monitoring security with Azure Monitor | Azure Monitor | Comprehensive security monitoring | Complexity in monitoring | Lack of monitoring leading to unnoticed security incidents | P1, P2 |  |

## Implement Privileged Identity Management (PIM)

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Activate PIM | Activating PIM for Azure AD roles | Azure AD PIM | Controlled privilege elevation | Complexity in activation | Uncontrolled privilege elevation | P2 |  |
| Configure PIM roles | Role configuration in PIM | Azure AD PIM Roles | Fine-grained role control | Complexity in configuration | Misconfigured roles leading to unauthorized access | P2 |  |
| Configure PIM security settings | Security settings for PIM | Azure AD PIM Security Settings | Enhanced PIM security | Complexity in configuration | Misconfigured settings leading to security risks | P2 |  |
| Monitor PIM | Monitoring PIM activities | Azure AD PIM Monitoring | Visibility into PIM activities | Complexity in monitoring | Lack of monitoring leading to unnoticed issues | P2 |  |

## Implement Azure AD B2B Collaboration

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Manage partner guest accounts | Managing partner guest access | Azure AD B2B Collaboration | Controlled partner access | Complexity in management | Unauthorized partner access | Free, P1, P2 |  |
| Manage Azure B2B Collaboration settings | B2B Collaboration management | Azure AD B2B Collaboration settings | Centralized collaboration settings | Complexity in management | Misconfiguration leading to unauthorized access | Free, P1, P2 |  |

## Implement Azure AD B2C Collaboration

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Manage B2C settings | B2C settings management | Azure AD B2C settings | Centralized B2C settings | Complexity in management | Misconfiguration leading to unauthorized access | P1, P2 |  |
| Manage B2C user accounts | B2C user account management | Azure AD B2C user management | Controlled B2C user management | Complexity in management | Unauthorized B2C access | P1, P2 |  |
| Implement and manage custom policies for B2C | Custom B2C policies | Azure AD B2C custom policies | Tailored B2C policies | Complexity in policy implementation | Misconfigured policies leading to unauthorized access | P1, P2 |  |

## Implement Azure AD PIM for Privileged Access to Azure Resources

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Activate PIM for Azure | Activating PIM for Azure resources | Azure AD PIM for Azure | Controlled privilege elevation | Complexity in activation | Uncontrolled privilege elevation | P2 |  |
| Configure PIM roles for Azure | Role configuration in PIM | Azure AD PIM Roles for Azure | Fine-grained role control | Complexity in configuration | Misconfigured roles leading to unauthorized access | P2 |  |
| Monitor PIM for Azure | Monitoring PIM activities | Azure AD PIM Monitoring for Azure | Visibility into PIM activities | Complexity in monitoring | Lack of monitoring leading to unnoticed issues | P2 |  |

## Implement Management and Governance for Azure Resources

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Configure and manage resource policies | Resource policy management | Azure Policy | Centralized resource policy management | Complexity in policy management | Misconfigured policies leading to security gaps | Free, P1, P2 |  |
| Configure and manage resource locks | Resource lock management | Azure Resource Locks | Prevent accidental deletion/modification | Complexity in lock management | Lack of resource locks leading to accidents | Free, P1, P2 |  |
| Apply and manage resource tags | Resource tag management | Azure Resource Tags | Organized resource management | Complexity in tag management | Mismanagement of tags leading to disorganization | Free, P1, P2 |  |
| Create a shared image gallery | Shared image gallery creation | Azure Shared Image Gallery | Centralized image management | Complexity in creation | Image-related risks | P2 |  |

## Implement Applications and User Authentication

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Design and implement authentication | Authentication design | Azure AD authentication | Secure user authentication | Complexity in design | Insecure authentication leading to breaches | P1, P2 |  |
| Implement authentication for applications | Application authentication implementation | Azure AD app authentication | Secure app authentication | Complexity in implementation | Insecure app authentication leading to breaches | P1, P2 |  |
| Configure and manage authentication options | Authentication option management | Azure AD authentication options | Flexible authentication methods | Complexity in configuration | Misconfigured options leading to security gaps | P1, P2 |  |
| Configure and manage authentication for users | User authentication management | Azure AD user authentication | Controlled user authentication | Complexity in management | Unauthorized user access | P1, P2 |  |
| Configure authentication for password reset | Password reset authentication configuration | Azure AD password reset | Secure password reset | Complexity in configuration | Insecure password reset leading to unauthorized access | P1, P2 |  |
| Configure and manage Azure AD Multi-Factor Authentication (MFA) settings | MFA settings configuration | Azure AD MFA settings | Enhanced security with MFA | Complexity in configuration | Misconfigured MFA leading to security gaps | P1, P2 |  |

## Implement Data Storage for Azure Resources

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Implement Azure Backup for Azure resources | Backup implementation | Azure Backup | Data protection and recovery | Complexity in implementation | Inadequate backups leading to data loss | P1, P2 |  |
| Implement Azure Site Recovery | Disaster recovery implementation | Azure Site Recovery | Business continuity and data recovery | Complexity in implementation | Inadequate disaster recovery leading to data loss | P1, P2 |  |

## Implement Cloud Infrastructure Monitoring

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Configure and manage Azure Monitor metrics | Azure Monitor metrics management | Azure Monitor metrics | Visibility into infrastructure performance | Complexity in configuration | Inadequate monitoring leading to unnoticed issues | Free, P1, P2 |  |
| Configure log analytics | Log analytics configuration | Azure Log Analytics | Comprehensive infrastructure monitoring | Complexity in configuration | Inadequate monitoring leading to unnoticed issues | Free, P1, P2 |  |
| Configure Azure Monitor logs | Azure Monitor logs configuration | Azure Monitor logs | Centralized log management | Complexity in configuration | Inadequate monitoring leading to unnoticed issues | Free, P1, P2 |  |
| Configure Application Insights | Application Insights configuration | Application Insights | Application performance monitoring | Complexity in configuration | Inadequate monitoring leading to unnoticed issues | Free, P1, P2 |  |
| Implement Azure Monitor solutions | Azure Monitor solution implementation | Azure Monitor solutions | Tailored monitoring solutions | Complexity in implementation | Inadequate monitoring leading to unnoticed issues | Free, P1, P2 |  |

## Implement VMs for Windows and Linux

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Configure high availability | High availability configuration | Azure high availability | Improved application uptime | Complexity in configuration | Inadequate high availability leading to downtime | Free, P1, P2 |  |
| Configure storage and networking | Storage and networking configuration | Azure storage and networking | Efficient resource utilization | Complexity in configuration | Misconfigured settings leading to security risks | Free, P1, P2 |  |

## Implement Containers for Azure Resources

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Configure Azure Kubernetes Service (AKS) | AKS configuration | Azure Kubernetes Service (AKS) | Managed Kubernetes clusters | Complexity in configuration | Misconfigured AKS leading to security risks | Free, P1, P2 |  |

## Implement Azure Active Directory (Azure AD)

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Configure Azure AD for workloads | Azure AD configuration | Azure AD | Centralized identity management | Complexity in configuration | Misconfigured settings leading to security risks | Free, P1, P2 |  |

## Implement and Manage Azure Governance Solutions

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Create and manage hierarchical structure for management groups | Hierarchical management group structure | Azure Management Groups | Organized resource management | Complexity in management | Mismanaged structure leading to disorganization | Free, P1, P2 |  |
| Create and manage Azure policies | Azure policy management | Azure Policy | Centralized policy management | Complexity in policy management | Misconfigured policies leading to security gaps | Free, P1, P2 |  |
| Configure Azure Policy compliance settings | Policy compliance configuration | Azure Policy compliance settings | Improved compliance reporting | Complexity in configuration | Non-compliance risks | Free, P1, P2 |  |

## Manage Security and Compliance

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Configure and manage Azure Security Center settings | Azure Security Center configuration | Azure Security Center settings | Centralized security management | Complexity in configuration | Misconfigured settings leading to security gaps | Free, P1, P2 |  |
| Configure security policies by using Azure Security Center | Security policy configuration | Azure Security Center security policies | Improved security posture | Complexity in policy configuration | Misconfigured policies leading to security gaps | Free, P1, P2 |  |
| Configure security settings by using Azure Security Center | Security settings configuration | Azure Security Center security settings | Enhanced security configurations | Complexity in configuration | Misconfigured settings leading to security gaps | Free, P1, P2 |  |
| Monitor security by using Azure Security Center | Security monitoring with Azure Security Center | Azure Security Center monitoring | Comprehensive security monitoring | Complexity in monitoring | Lack of monitoring leading to unnoticed security issues | Free, P1, P2 |  |

## Configure and Manage Azure AD Identity Protection

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Create and manage risk policies | Risk policy management | Azure AD Identity Protection risk policies | Proactive risk management | Complexity in policy management | Unmanaged risks | P2 |  |
| Create and manage conditional access policies for Azure AD Identity Protection | Conditional access policy management | Azure AD Identity Protection conditional access policies | Controlled access based on risk | Complexity in policy management | Misconfigured policies leading to access issues | P2 |  |
| Configure and manage user risk policy | User risk policy configuration | Azure AD Identity Protection user risk policy | Managed access based on user risk | Complexity in configuration | Misconfigured settings leading to access issues | P2 |  |
| Configure and manage sign-in risk policy | Sign-in risk policy configuration | Azure AD Identity Protection sign-in risk policy | Managed access based on sign-in risk | Complexity in configuration | Misconfigured settings leading to access issues | P2 |  |

## Manage Azure AD Privileged Identity Management (PIM)

| Task | Business Case | Product/Service/Method | Pros | Cons | Security Risks | License Needed | Additional Information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Manage directory roles | Directory role management | Azure AD Privileged Identity Management roles | Fine-grained privilege control | Complexity in management | Mismanaged roles leading to unauthorized access | P2 |  |
| Activate PIM | Activating PIM for directory roles | Azure AD Privileged Identity Management | Controlled privilege elevation | Complexity in activation | Uncontrolled privilege elevation | P2 |  |
| Configure just-in-time (JIT) access | JIT access configuration | Azure AD Privileged Identity Management JIT | Temporary privilege elevation | Complexity in configuration | Misconfigured settings leading to unauthorized access | P2 |  |
| Monitor privileged access | Monitoring privileged access | Azure AD Privileged Identity Management monitoring | Visibility into privileged activities | Complexity in monitoring | Unmonitored activities leading to unnoticed issues | P2 |  |
| Review privileged access | Reviewing privileged access | Azure AD Privileged Identity Management reviews | Controlled review process | Complexity in review management | Mismanaged reviews leading to compliance issues | P2 |  |
