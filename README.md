# SC-300 - Study Notes  

## Implement identities in Azure AD (20–25%)

### Configure and manage an Azure AD tenant

    * ****Configure and manage Azure AD roles
        Business Case: Need to delegate specific administrative tasks to different teams within the organization.
        Product Solution: Azure AD Role-Based Access Control (RBAC).
        Pros: Granular control, segregation of duties, enhanced security.
        Cons: Complexity in managing numerous roles, potential misconfiguration.
        Licensing: Available in Azure AD Free, advanced features in Premium P1.

    * **Configure delegation by using administrative units**
        Business Case: A large organization wants to delegate admin tasks to different departments without giving full control.
        Product Solution: Azure AD Administrative Units.
        Pros: Improved delegation, better control, reduced risk of unauthorized access.
        Cons: Can be complex to set up, requires careful planning.
        Licensing: Requires Azure AD Premium P1.

    * **Analyze Azure AD role permissions**
        Business Case: Regularly review and audit role permissions to comply with internal policies and regulatory requirements.
        Product Solution: Azure AD Access Reviews.
        Pros: Ensures compliance, identifies excessive permissions, enhances security.
        Cons: Requires ongoing management, potential complexity.
        Licensing: Requires Azure AD Premium P2.

    * **Configure and manage custom domains**
        Business Case: A company wants to use its branded domain name for user identities.
        Product Solution: Azure AD Custom Domains.
        Pros: Branding alignment, professional appearance, trust-building.
        Cons: Requires DNS management, potential complexity in configuration.
        Licensing: Available in Azure AD Free.

    * **Configure tenant-wide settings**
        Business Case: Implementing organization-wide security policies and configurations.
        Product Solution: Azure AD Tenant Settings.
        Pros: Consistency across the organization, centralized control.
        Cons: Potential for over-restriction, careful planning required.
        Licensing: Available in Azure AD Free, advanced features in Premium P1/P2

### Create, configure, and manage Azure AD identities

    * **Create, configure, and manage users**
        Business Case: Onboarding a large number of employees after a company merger.
        Product Solution: Azure AD Bulk User Management.
        Pros: Efficient, reduces manual errors, scalable.
        Cons: Requires proper CSV formatting, potential for bulk errors.
        Licensing: Available in Azure AD Free, advanced features in Premium P1.

    * **Create, configure, and manage groups**
        Business Case: Segmenting users by department for resource access.
        Product Solution: Azure AD Groups.
        Pros: Organized resource access, easier management.
        Cons: Can become complex with nested groups, requires regular auditing.
        Licensing: Available in Azure AD Free.

    * **Configure and manage device join and registration, including writeback**
        Business Case: Allowing employees to use their personal devices for work.
        Product Solution: Azure AD Device Registration.
        Pros: Flexibility, potential cost savings, enhanced productivity.
        Cons: Security concerns, requires robust device management policies.
        Licensing: Requires Azure AD Premium P1 for advanced features.

    * **Assign, modify, and report on licenses**
        Business Case: Ensuring all employees have the necessary software licenses.
        Product Solution: Azure AD License Management.
        Pros: Centralized management, cost tracking, compliance.
        Cons: Requires regular updates, potential for over or under-licensing.
        Licensing: Available in Azure AD Free, advanced features in Premium P1.

### Implement and manage external identities

    * **Manage external collaboration settings in Azure AD**
        Business Case: Collaborating with external partners on a project.
        Product Solution: Azure AD B2B Collaboration.
        Pros: Secure collaboration, resource sharing without creating internal accounts.
        Cons: Requires management of external identities, potential security concerns.
        Licensing: Requires Azure AD Premium P1 for advanced features.

    * **Invite external users, individually or in bulk**
        Business Case: Inviting attendees for a large external webinar.
        Product Solution: Azure AD B2B Invitations.
        Pros: Scalable, efficient, secure.
        Cons: Requires proper email addresses, potential for bulk invitation errors.
        Licensing: Requires Azure AD Premium P1.

    * **Manage external user accounts in Azure AD**
        Business Case: Offboarding external consultants after project completion.
        Product Solution: Azure AD External Identity Management.
        Pros: Centralized management, ensures security by removing unnecessary access.
        Cons: Requires regular auditing, potential for oversight.
        Licensing: Requires Azure AD Premium P1.

    * **Configure identity providers, including SAML or WS-fed**
        Business Case: Integrating a third-party SaaS application for single sign-on.
        Product Solution: Azure AD SAML/WS-Federation Integration.
        Pros: Seamless user experience, enhanced security, centralized authentication.
        Cons: Requires configuration on both ends, potential for integration errors.
        Licensing: Requires Azure AD Premium P1.

   ### Create, configure, and manage Azure AD identities

    * **Create, configure, and manage users**
        Business Case: Onboarding new employees and managing user access across the organization.
        Product Solution: Azure AD User Management.
        Pros: Centralized management, automation capabilities, integration with other systems.
        Cons: Requires proper planning and governance, potential complexity.
        Licensing: Available in Azure AD Free, advanced features in Premium P1.

    * **Create, configure, and manage groups**
        Business Case: Managing access to resources for different teams or departments.
        Product Solution: Azure AD Groups.
        Pros: Simplifies permission management, enhances collaboration.
        Cons: Can become complex if not properly managed, potential for permission overlap.
        Licensing: Available in Azure AD Free, advanced features in Premium P1.

    * **Configure and manage device join and registration, including writeback**
        Business Case: Enabling employees to use their devices to access company resources securely.
        Product Solution: Azure AD Device Management.
        Pros: Enhances mobility, improves security, supports BYOD policies.
        Cons: Requires robust security policies, potential complexity in management.
        Licensing: Requires Azure AD Premium P1.

    * **Assign, modify, and report on licenses**
        Business Case: Managing software licenses for different users and departments.
        Product Solution: Azure AD License Management.
        Pros: Cost control, compliance with licensing agreements, flexibility.
        Cons: Requires ongoing monitoring, potential complexity.
        Licensing: Available in Azure AD Free, advanced features in Premium P1.

### Implement and manage external identities

    * **Manage external collaboration settings in Azure AD**
        Business Case: Collaborating with external partners or vendors on projects.
        Product Solution: Azure AD B2B Collaboration.
        Pros: Secure collaboration, simplified access management, scalability.
        Cons: Requires governance policies, potential complexity.
        Licensing: Consumption-based pricing for external users.

    * **Invite external users, individually or in bulk**
        Business Case: Inviting external collaborators for a specific project or event.
        Product Solution: Azure AD B2B Invitations.
        Pros: Streamlined process, secure access, integration with existing tools.
        Cons: Requires monitoring and management, potential security considerations.
        Licensing: Consumption-based pricing for external users.

    * **Manage external user accounts in Azure AD**
        Business Case: Managing access for external contractors, vendors, or partners.
        Product Solution: Azure AD External Identity Management.
        Pros: Centralized control, enhanced security, flexibility.
        Cons: Requires proper planning and governance, potential complexity.
        Licensing: Consumption-based pricing for external users.

    * **Configure identity providers, including SAML or WS-fed**
        Business Case: Integrating with third-party identity providers for SSO.
        Product Solution: Azure AD Identity Providers.
        Pros: Simplifies authentication, enhances user experience, supports various protocols.
        Cons: Requires proper configuration and testing, potential compatibility issues.
        Licensing: Requires Azure AD Premium P1.
