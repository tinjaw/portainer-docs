
# :fontawesome-solid-users-cog: Roles

<div class="container">
<iframe src="//www.youtube.com/embed/6LjWqlHP2ME" 
frameborder="0" allowfullscreen class="video"></iframe>
</div>


## Description of Roles

Portainer Business come with Role-Based Access Control features that refines the access privileges available natively within Portainer. The RBAC feature allows you to create fine-grained access for users across all resources and all endpoints defined within Portainer.

## Basics Understanding

* Role is a predefined set of privileges.
* Privileges define rights to perform actions.
* Users are assigned roles and each role has specific privileges.
* To assign privileges, you pair a user or team with a role and associate that pairing with an endpoint or endpoint group.
* A single user or team can have different roles for different endpoints in the Portainer inventory.

## Built-in Roles

There are several types of roles:

* <b>Endpoint Administrator</b> has complete control over the resources deployed within a given endpoint, but is not able to make any changes to the infrastructure that underpins an endpoint (i.e. no host management), nor are they able to make any changes to Portainer internal settings.

* <b>Operator</b> has operational control over the resources deployed within a given endpoint. Operator is able to Update/Re-deploy/Start/Stop Containers/Services, check logs and console into containers but is not able to create any resources.

* <b>Helpdesk</b> has read-only access over the resources deployed within a given endpoint but is not able to make any changes to any resource, nor open a console to a container, or make changes to a container’s volumes.

* <b>Standard User</b> has complete control over the resources that a user deploys, or if the user is a member of a team, complete control over the resources that users of that team deploy.

* <b>Read-Only User</b> has read-only access over the resources they are entitled to see (resources created by members of their team, and public resources).

The <b>Administrator</b> role sits outside of these four roles, and effectively acts as a “Global Admin”. A user assigned this role has complete control over Portainer settings, and all resources on every endpoint under Portainer control.

## Docker vs Kubernetes

As Docker does not natively provide role-based access control, Portainer implements our own role management to provide this functionality. On a Kubernetes environment, we leverage the RBAC functionality built into Kubernetes alongside our own role management to provide security and flexibility to roles and access.

For more advanced details on how we map Portainer roles to Kubernetes roles, refer to our [Roles and Bindings](/v2.0-be/users/k8s-roles/) documentation.

<br>
## :material-note-text: Notes

[Contribute to these docs](https://github.com/portainer/portainer-docs/blob/master/contributing.md){target=_blank}