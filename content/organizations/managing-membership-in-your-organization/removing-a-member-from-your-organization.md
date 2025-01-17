---
title: Removing a member from your organization
intro: 'If members of your organization no longer require access to any repositories owned by the organization, you can remove them from the organization.'
redirect_from:
  - /articles/removing-a-member-from-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/removing-a-member-from-your-organization
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Remove a member
permissions: Organization owners can remove members from an organization.
---

{% ifversion fpt or ghec %}

{% warning %}

**Warning:** When you remove members from an organization:
- The paid license count does not automatically downgrade. To pay for fewer licenses after removing users from your organization, follow the steps in "[AUTOTITLE](/billing/managing-billing-for-your-github-account/downgrading-your-github-subscription)."
- Removed members will lose access to private forks of your organization's private repositories, but they may still have local copies. However, they cannot sync local copies with your organization's repositories. Their private forks can be restored if the user is [reinstated as an organization member](/organizations/managing-membership-in-your-organization/reinstating-a-former-member-of-your-organization) within three months of being removed from the organization. Ultimately, you are responsible for ensuring that people who have lost access to a repository delete any confidential information or intellectual property.
- When private repositories are forked to other organizations, those organizations are able to control access to the fork network. This means users may retain access to the forks even after losing access to the original organization because they will still have explicit access via a fork. 
{%- ifversion ghec %}
-  Removed members will also lose access to private forks of your organization's internal repositories, if the removed member is not a member of any other organization owned by the same enterprise account. For more information, see "[AUTOTITLE](/admin/overview/about-enterprise-accounts)."
{%- endif %}
- Any organization invitations sent by a removed member, that have not been accepted, are canceled and will not be accessible.

{% endwarning %}

{% else %}

{% warning %}

**Warning:** When you remove members from an organization:
 - Removed members will lose access to private forks of your organization's private repositories, but may still have local copies. However, they cannot sync local copies with your organization's repositories. Their private forks can be restored if the user is [reinstated as an organization member](/organizations/managing-membership-in-your-organization/reinstating-a-former-member-of-your-organization) within three months of being removed from the organization. Ultimately, you are responsible for ensuring that people who have lost access to a repository delete any confidential information or intellectual property.
- Removed members will also lose access to private forks of your organization's internal repositories, if the removed member is not a member of any other organization in your enterprise.
 - Any organization invitations sent by the removed user, that have not been accepted, are canceled and will not be accessible.

{% endwarning %}

{% endif %}

{% ifversion fpt or ghec %}

To help the person you're removing from your organization transition and help ensure they delete confidential information or intellectual property, we recommend sharing a checklist of best practices for leaving your organization. For an example, see "[AUTOTITLE](/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-your-personal-account/best-practices-for-leaving-your-company)."

{% endif %}

{% data reusables.organizations.data_saved_for_reinstating_a_former_org_member %}

## Revoking the user's membership

{% data reusables.profile.access_org %}
{% data reusables.user-settings.access_org %}
{% data reusables.organizations.people %}
4. Select the member or members you'd like to remove from the organization.
  ![List of members with two members selected](/assets/images/help/teams/list-of-members-selected-bulk.png)
5. Above the list of members, use the drop-down menu, and click **Remove from organization**.
  ![Drop-down menu with option to remove members](/assets/images/help/teams/user-bulk-management-options.png)
6. Review the member or members who will be removed from the organization, then click **Remove members**.
  ![List of members who will be removed and Remove members button](/assets/images/help/teams/confirm-remove-members-bulk.png)

## Further reading

- "[AUTOTITLE](/organizations/organizing-members-into-teams/removing-organization-members-from-a-team)"{% ifversion remove-enterprise-members %}
- "[AUTOTITLE](/admin/user-management/managing-users-in-your-enterprise/removing-a-member-from-your-enterprise)"{% endif %}
