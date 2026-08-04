# HV-Desk

**HV-Desk is a web-based management platform for virtualized infrastructure.**

The project aims to provide a central, modern, and easy-to-use interface for managing virtualization hosts, virtual machines, clusters, storage, and related administrative workflows.

The first major release will focus on **Microsoft Hyper-V**. Support for **Proxmox VE** and additional virtualization platforms is planned for future major versions.

## Why I Built HV-Desk

Because managing Hyper-V — especially in a cluster — is way more painful than it needs to be.

Too many everyday tasks are scattered across different tools, buried in menus, hidden behind PowerShell, or give you little to no useful feedback while something is happening.
Coming from VMware vSphere, I wanted something that feels less like fighting the administration layer all day and more like actually managing the environment.

HV-Desk started because I wanted:
- one place to manage hosts, clusters, VMs, storage, and related tasks
- clear progress instead of "something is happening, probably"
- useful errors instead of vague failures
- less jumping between GUIs, consoles, and PowerShell
- fewer repetitive CLI commands for normal day-to-day work
- a smoother transition for people used to vSphere-style infrastructure management
- an interface that actually tells you what is going on

In short: I got tired of spending more time managing the management tools than managing the infrastructure.

## Project Goals

* Centralized management of virtualization environments
* Clear host, cluster, and virtual machine management
* Secure support for different authentication environments
* Role-based access control
* Task tracking and audit history
* Reliable installation, updates, and recovery
* A consistent web interface for daily administration
* An extensible architecture for additional virtualization platforms

## Platform Roadmap

### Initial Platform

The first major version will focus on Microsoft Hyper-V, including:

* Standalone Hyper-V hosts
* Windows Failover Clusters
* Virtual machine management
* Migration and maintenance workflows
* Storage and media management
* Domain and workgroup environments

### Future Platforms

Proxmox VE is planned as the next virtualization platform supported by HV-Desk.

Additional virtualization platforms may follow in later major versions as the project and its architecture evolve.

The long-term goal is to manage different virtualization technologies through a consistent interface while preserving their platform-specific capabilities.

## Technology

HV-Desk is currently built with:

- Node.js for backend services and APIs
- React and Vite for the web interface
- PostgreSQL for persistent data
- PowerShell and WinRM for virtualization host management
- Kerberos for domain-based host access
- LDAP/LDAPS for Active Directory user authentication

The architecture is being developed with future support for additional virtualization platforms in mind.

## Development Status

HV-Desk is currently under active development and is not yet production-ready.

The source code, installation instructions, documentation, and release packages will be published at a later stage.

## Disclaimer

HV-Desk is an independent project and is not affiliated with, endorsed by, or sponsored by Microsoft or Proxmox Server Solutions GmbH.

Microsoft, Windows, Hyper-V, Active Directory, PowerShell, Proxmox, and Proxmox VE are trademarks of their respective owners.
