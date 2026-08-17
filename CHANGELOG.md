# HV-Desk Changelog

All notable user-visible changes to HV-Desk are documented in this file.  
The newest version is listed first.

---
## v0.20.24

- VM disk management has been expanded with disk moves, resize, removal, and more reliable QoS handling.
- VHD/VHDX management now includes compact, convert, and merge operations.
- DVD/ISO handling and storage safety checks have been improved.
- Host storage inventory and health reporting now cover volumes, disks, partitions, physical disks, pools, virtual disks, and reliability data.

## v0.20.23

- English translations across the networking area have been completed.
- Networking error handling and capability states are now presented more consistently.
- Networking frontend coverage and consistency have been hardened.

## v0.20.22

- Advanced physical network adapter settings now include RSS, RSC, LSO, checksum and segmentation offloads, QoS/DCB, and adapter bindings where supported.
- Advanced IP interface settings such as automatic metrics, forwarding, weak-host behavior, and router discovery can now be managed.
- Virtual switch configuration has been expanded with extensions, bandwidth settings, notes, SR-IOV, and Packet Direct options.
- VM network adapter management now includes trunk VLANs, bandwidth weight, device naming, and teaming support.

## v0.20.21

- VM network adapter creation and VLAN configuration have been made more reliable.
- Virtual switches are now selected using stable identifiers when adding or editing VM network adapters.
- VM network adapter editing no longer reconnects the switch unless a switch change was explicitly requested.

## v0.20.20

- Host network data is now refreshed consistently after network changes, with clear warnings if a refresh fails.
- Virtual switch uplink validation and adapter selection have been hardened.
- Virtual switch operations now provide more consistent task and audit tracking.

## v0.20.19

- NIC Teaming (LBFO) now shows team status, teaming mode, load-balancing mode, and member status.
- LBFO adapter detection has been improved across the host networking view.
- LBFO remains read-only, while existing SET member management remains fully available.

## v0.20.18

- Host and management interfaces can now use multiple IPv4 and IPv6 addresses.
- Additional addresses can be added or removed individually without replacing existing configuration.
- Address changes include stronger validation and post-change verification.

## v0.20.17

- Management VLAN configuration now supports Untagged, Access, and Trunk modes.
- Physical adapter VLAN settings can be managed when the adapter exposes a reliable VLAN capability.
- VLAN validation, adapter identification, and network safety checks have been hardened.

## v0.20.16

- Connection-specific DNS suffixes and DNS registration settings can now be managed per host interface.
- The host-wide DNS suffix search list can now be configured from HV-Desk.
- DNS configuration handling and post-change verification have been hardened.

## v0.20.15

- Wake-on-LAN using Magic Packet can now be configured on supported physical adapters.
- Network gateway verification has been hardened to handle multiple default routes more reliably.

## v0.20.14

- Physical network adapters used directly by the host can now be configured with IPv4, IPv6, DNS, gateways, DHCPv4, and interface metrics.
- Direct host network changes use the same management connectivity safeguards as existing host networking.
- Interface identification and post-change verification have been hardened.

## v0.20.13

- Physical adapters can now be added to or removed from existing Switch Embedded Teaming (SET) switches.
- SET changes include safeguards against invalid adapter assignments, removing the final team member, and disrupting management connectivity.

## v0.20.12

- Host networking now presents virtual switches, uplinks, management adapters, routing, and VM usage as a connected network topology.
- Physical adapters show how they are currently used, including SET, LBFO, switch uplink, and direct host usage.
- Host network editing and routing navigation have been consolidated for a more consistent workflow.

## v0.20.11

- Host networking now includes a dedicated routing view for IPv4 and IPv6 routes.
- Default routes can be managed directly from the host networking area.
- Static IPv4 and IPv6 routes can be added, updated, and removed where Windows reports them as safely manageable.
- IPv4 and IPv6 interface metrics can now be configured independently.
- Routing changes include safeguards against disconnecting the active management path.

## v0.20.10

- Host management network adapters can now be created, renamed, moved between virtual switches, and removed.
- IPv6 address, prefix, gateway, and DNS configuration is now available for host management adapters.
- Interface metrics can be configured for host management adapters.
- Network changes that could interrupt the active management connection are blocked automatically.

## v0.20.9

- Virtual switches can now be managed directly from the host networking view.
- External, internal, and private virtual switches can be created, renamed, configured, and removed.
- External switch uplinks can be selected and changed from HV-Desk.
- Switch Embedded Teaming (SET) can be configured when creating a switch with multiple supported uplinks.
- Switch changes now include stronger checks for VM usage and host management connectivity.

## v0.20.8

- Physical network adapter settings have been expanded.
- VMQ and RDMA can be enabled or disabled on supported adapters.
- MTU, Jumbo Frames, and interface metrics can be managed when supported by the adapter.
- Adapter settings are shown only when HV-Desk can determine that the capability is available.

## v0.20.7

- Disabled physical network adapters are now detected more reliably and can be re-enabled from HV-Desk.
- Physical adapter status now distinguishes more clearly between connected, disconnected, disabled, unavailable, and unknown states.
- Physical adapters now have a dedicated settings view with hardware and connection details.
- Adapter renaming has been moved into the settings view for a more consistent workflow.

## v0.20.6

- Physical host network adapters can now be enabled, disabled, and renamed from HV-Desk.
- Adapter actions account for virtual switch, teaming, management, and cluster dependencies.
- Physical adapter state and availability are displayed more accurately.

## v0.20.5

- Core host networking settings can now be managed directly from HV-Desk.
- IPv4 addresses, DNS servers, default gateways, DHCP, and management VLAN settings can be changed from the host view.
- Network changes are checked before execution to reduce the risk of losing management access.
- Updated settings are read back from the host after changes are applied.

## v0.20.4

- The host networking view now brings together physical adapters, virtual switches, management adapters, and IP configuration.
- Physical adapter to virtual switch relationships are shown, including Switch Embedded Teaming (SET).
- Host management adapter details include IP addresses, DNS, gateways, DHCP, and VLAN information.
- Adapter capabilities such as VMQ, RDMA, and SR-IOV are displayed when available.

## v0.20.3

- A dedicated operating system section is now available on host detail pages.
- Windows, hostname, domain membership, and related host information are easier to review.
- Hostnames and supported domain membership settings can be managed from HV-Desk.
- Changes that require a restart are clearly indicated instead of restarting the host automatically.

## v0.20.2

- Host detail pages have been reorganized to support the expanding host administration features.
- Host sections now use a more stable navigation structure while keeping existing information and actions available.

## v0.20.1

- Host settings are displayed more consistently when Windows does not support or return a value.
- Editing multiple host settings provides clearer feedback when individual settings cannot be changed.
- Live Migration settings are reported more reliably across the host view.

## v0.20.0

- Hyper-V host settings can now be viewed and managed directly from HV-Desk.
- Default VM and virtual disk paths, Live Migration, Storage Migration, NUMA, and related host settings are available from the host detail page.
- Unsupported or read-only settings are clearly identified instead of displaying misleading values.
- Changes are validated and read back from the host after they are applied.
- Potentially disruptive host setting changes require explicit confirmation.

## v0.19.10

- User sessions now react more consistently when an account is disabled.
- Authentication state, permissions, and active sessions have been made more consistent.

## v0.19.9

- Role and permission handling has been hardened across Administration and cluster views.
- Users can no longer grant permissions that they do not hold themselves.
- Cluster detail access now respects scoped permissions more consistently.
- The currently signed-in user is displayed in the sidebar.

## v0.19.8

- The interface now hides or disables areas and actions that the current user is not allowed to use.
- Host- and cluster-scoped permissions are reflected directly in navigation and action availability.
- Changes to a user's role are reflected without requiring a new sign-in.
- Loading of larger application areas has been improved.

## v0.19.7

- Roles can now be assigned globally or only to selected hosts and clusters.
- Users can be limited to the infrastructure they are responsible for.
- Global and scoped role assignments can be combined.
- Administration tables remain usable at narrower window sizes.

## v0.19.6

- Custom roles can now be created in addition to the built-in roles.
- Permissions can be selected individually for custom roles.
- Custom roles can be assigned to users and edited later.
- Roles that are still in use are protected from accidental deletion.
- Kerberos host access and Active Directory configuration reliability have been improved.

## v0.19.5

- HV-Desk now includes built-in Administrator, Operator, and Viewer roles.
- User roles can be viewed and changed from Administration.
- A dedicated Roles area shows the permissions available to each role.
- The last remaining administrator account is protected from accidental removal of administrative access.

## v0.19.4

- Multiple Kerberos profiles can now be managed for different domains or host environments.
- Hosts and clusters can be assigned to the appropriate Kerberos profile when they are added.
- Kerberos profiles can be created, tested, disabled, and removed from Administration.
- Cluster nodes inherit the profile assigned to their cluster.

## v0.19.3

- Workgroup hosts can now be added and managed securely using local credentials.
- The identity of a Workgroup host must be explicitly trusted when it is added. Connections are blocked automatically if the identity changes later.
- Workgroup hosts are prevented from being used accidentally for high-availability VMs, host-to-host migrations, or cluster maintenance operations.
- Unsupported file and virtual disk downloads from Workgroup hosts are now rejected clearly, and unavailable actions are hidden in the interface.
- Acknowledged dashboard issues are hidden once no active issue remains. Pending Windows updates and restart-required warnings can also be acknowledged on the host details page.

## v0.19.2

- Active Directory users can sign in alongside existing local users.
- Authorized AD users are created automatically in HV-Desk during their first successful sign-in.
- User authentication and technical access to managed hosts are now separated more reliably.
- AD sign-in reliability and diagnostics have been improved.
- The VM creation wizard now supports cluster-aware storage selection and can be opened globally from the sidebar.
- VM creation no longer fails when default automatic start or stop behavior is left unchanged.
- Storage warnings can be acknowledged and restored across the dashboard and storage views.
- Acknowledged warnings are no longer included in alert counters or warning badges.
- Cluster network information is displayed more clearly in the audit log.

## v0.19.1

- A complete local user management area is now available under Administration.
- Local users can be created, edited, activated, and deactivated.
- Administrators can reset passwords for local accounts.
- Existing Active Directory sign-in remains available.

## v0.19.0

- The Settings area has been reorganized and renamed to Administration.
- Hosts, clusters, policies, language, appearance, system information, and licensing information are easier to find.
- Clusters can be added again after previously being removed.
- Acknowledged or resolved failed tasks are displayed consistently across the dashboard and task views.
- Administration pages now use the available screen width more effectively.
- Browser reloads on nested application pages no longer lead to an empty error page.
- The system disk of a running VM can no longer be detached accidentally.
- Excluded cluster hosts no longer appear as false offline warnings.
- Cluster terminology and checkpoint naming are now more consistent throughout the interface.
- Cluster Shared Volumes show their current owner correctly in storage and host views.
- The Administration overview now includes CPU and memory information for the HV-Desk server.
- Open-source license information has been expanded to include system-level dependencies used by HV-Desk.

## v0.18.8

- Cluster nodes can now be prepared for maintenance through a controlled evacuation workflow.
- Highly available VMs are moved individually to suitable nodes before maintenance begins.
- Local VMs block automated evacuation and are never moved or stopped automatically.
- A preview shows affected VMs, planned targets, and possible blockers before execution.
- Evacuation progress and failures are visible while the operation is running.
- Other cluster roles and Cluster Shared Volumes are moved and verified before a node is paused.
- A cluster node can only be shut down after evacuation has completed successfully.

## v0.18.7

- Highly available VMs now use the dedicated cluster migration workflow.
- Network and storage compatibility checks focus on the resources actually used by the VM.
- VM ownership is updated immediately after migration or failover across all views.
- Uncertain migration results are reported as warnings instead of being shown as successful.
- Migration task details now include the checked networks, storage locations, and confirmed owner change.

## v0.18.6

- Highly available VMs can be started, stopped, restarted, paused, resumed, and forcibly powered off through cluster-aware actions.
- Live Migration and Quick Migration between cluster nodes are now available.
- Cluster VM actions include progress tracking and audit history.
- Cluster and VM views refresh automatically after operations complete.
- Dialogs close promptly while long-running work continues in the background.
- Newly added clusters are shown only after onboarding is complete.
- Duplicate VM and storage entries have been corrected.
- Cluster issues can now be acknowledged with an optional reason.
- Host removal reports storage records that could not be cleaned up automatically.

## v0.18.5

- A dedicated cluster diagnostics view now covers connectivity, node state, quorum, roles, shared storage, networks, VM ownership, and inventory freshness.
- Cluster diagnostics can be started manually and are tracked as tasks.
- Unknown, outdated, and unavailable states are clearly distinguished from healthy results.
- Cluster actions verify inventory freshness before they begin.
- Cluster and storage status are displayed more consistently.
- Cluster endpoints now show the name of the responding node where appropriate.
- Logical network configuration uses detected virtual switches instead of free-text input.
- New cluster nodes can be discovered immediately from Administration.
- Discovered nodes can be accepted, excluded, or restored later.
- Cluster onboarding now handles cluster addresses separately from physical hosts.
- Removed datastores no longer return automatically.
- Clusters can be removed independently of their hosts.
- Dashboard issue panels expand only when a problem exists, while a compact status bar remains visible at all times.

## v0.18.4

- Adding a host or cluster endpoint is now tracked as a visible task with connection, discovery, and result details.
- Cluster addresses are recognized automatically and no longer appear as ordinary hosts.
- Cluster pages now focus on cluster-wide information, while host hardware remains on the host detail page.
- New sidebar layouts are available for cluster-centered, node-centered, and standalone views.

## v0.18.3

- The VM creation wizard can register a new VM as a highly available cluster role.
- Cluster membership, shared storage, and network compatibility are checked before HA creation begins.
- Cluster nodes now have a dedicated maintenance workflow.
- Controlled node shutdown is available after maintenance requirements are satisfied.
- HA creation, maintenance, and node shutdown are tracked through tasks and audit history.

## v0.18.2

- Logical cluster networks can be defined and checked across all managed nodes.
- The VM creation wizard now supports multiple network adapters and virtual disks.
- VLAN, MAC address, controller position, DVD drive, boot order, and Secure Boot options are available during creation.
- Invalid VM configurations are detected before any incomplete VM is created.
- Task filters now distinguish open, running, acknowledged, historical failures, and successful tasks.
- Completed or superseded failures no longer remain in the active error counter.

## v0.18.1

- Host and VM detail pages now finish loading with a clear success, partial-success, or error state.
- Network information distinguishes between unavailable, outdated, and not-yet-loaded data.
- Orphaned datastores can be removed from HV-Desk from all relevant views.
- The Administration area is now fully available in German and English.

## v0.18.0

- Cluster summaries remain visible when individual refresh operations fail.
- Failover cluster discovery is used consistently across cluster views.
- Cluster roles, quorum, and witness information are now visible.
- Outdated or unavailable cluster data is clearly marked.
- VM creation on a cluster node clearly explains when the VM is not being registered as highly available.
- Cluster views are available in German and English.

## v0.17.4

- Orphaned datastore records can be removed safely from HV-Desk.
- Removing a datastore record never deletes real storage, files, CSVs, or cluster objects.
- Orphaned datastores are shown correctly as warnings on the dashboard and storage pages.
- Host removal previews which datastore records may become orphaned.
- Shared cluster storage is considered orphaned only when no node of the cluster remains managed.
- Storage pages are available in German and English.

## v0.17.3

- Physical adapters, virtual switches, and VM network adapters now show clearer diagnostics for inconsistent or outdated states.
- Failed network refreshes create a visible warning with a retry option.
- VM detail pages are protected against outdated responses when switching quickly between VMs.

## v0.17.2

- VM network adapters are identified by stable IDs instead of display names.
- Ambiguous network adapters are rejected safely instead of modifying the wrong device.
- VLAN and advanced network options are validated before changes are applied.
- Existing bandwidth limits are no longer reset accidentally.
- Network changes on cluster nodes are clearly identified as host-specific.

## v0.17.1

- Virtual switch management is now available for creating, editing, and deleting switches.
- Network changes refresh more reliably.
- File operations on Cluster Shared Volumes are better protected.

## v0.17.0

- Network and virtual switch features have been reviewed and aligned across the interface and backend.
- Advanced VM network settings are now applied and displayed correctly.
- Unavailable virtual switch actions are clearly marked instead of failing silently.
- Existing physical adapter and virtual switch views remain available.

## v0.16.1

- The foundation for a multilingual interface has been introduced.
- German remains the default language, with English available as an option.
- Core navigation, settings, and action labels are translated.

## v0.16.0

- HV-Desk now also represents “Hybrid Virtualization Desk.”
- The product identity has been added to the About section.
- Existing Hyper-V features and behavior remain unchanged.

## v0.15.10

- File browsing and file operations have been expanded.
- Large file and VHDX downloads are more reliable.
- VM and checkpoint-related errors have been corrected.
- Sign-in and server diagnostics have been improved.
- PowerShell and storage failures are handled more robustly.

## v0.15.9

- Host memory usage is displayed correctly again.
- VM deletion confirmation no longer blocks until deletion is complete.
- File upload and download are now available in permitted directories.
- Destructive file operations remain unavailable.

## v0.15.8

- Datastore navigation and usability have been improved.
- VMs and virtual disks are linked directly from storage views.
- A file browser is now available within datastore views.
- Storage browsing remains read-only.

## v0.15.7

- Local storage on standalone Hyper-V hosts is detected and displayed.
- Datastore diagnostics have been improved.
- Storage collection errors caused by malformed PowerShell output have been corrected.

## v0.15.6

- ISO and installation media information is displayed more clearly.
- Mounted ISO files are associated with their VMs more reliably.
- VM detail pages show improved media information.

## v0.15.5

- Storage health information and capacity warnings have been introduced.
- Low and critically low free-space conditions are reported.
- Storage issues are now represented on the dashboard.

## v0.15.4

- VM-to-datastore assignment is more accurate.
- Virtual disk and checkpoint detection has been improved.
- Provisioned and used storage are displayed more precisely.

## v0.15.3

- The task bar reacts faster after user actions.
- Checkpoint tasks appear immediately.
- Task entries now include the affected VM.

## v0.15.2

- A live task bar has been added to the main interface.
- The task bar can be collapsed and resized.
- Progress is displayed when available.
- The complete task history is accessible from the task bar.

## v0.15.1

- Datastore detail pages now show related VMs and disks.
- Virtual switch selection during VM creation and adapter configuration has been corrected.
- iSCSI operations are now represented as tasks.

## v0.15.0

- The storage and datastore model has been introduced.
- Local paths, Cluster Shared Volumes, media paths, and VM disks are collected in read-only mode.
- A dedicated storage page is now available.

## v0.14.4

- Cluster health evaluation has been improved.
- Cluster, node, shared storage, and highly available VM states are classified more accurately.

## v0.14.3

- Basic read-only Cluster Shared Volume information is now available.
- CSV name, state, owner node, path, and capacity are displayed when available.

## v0.14.2

- Highly available VMs are associated with their cluster roles and owner nodes more reliably.

## v0.14.1

- Cluster information is now visible in the existing interface.
- Host details identify whether a host is standalone or part of a cluster.

## v0.14.0

- The host and cluster foundation has been introduced.
- Standalone hosts and failover cluster nodes are now distinguished.

## v0.13.8

- Task management has been refined.
- Task and audit relationships have been prepared.
- Task badges and history retention have been improved.

## v0.13.7

- Running tasks now show percentage progress when real progress information is available.

## v0.13.6

- Additional VM operations are represented as tasks.
- Checkpoint, ISO, disk, and VM settings operations are more reliable.
- Removing DVD drives, disks, controllers, and network adapters has been stabilized.

## v0.13.5

- Powered-off VMs no longer show false health warnings.
- Guest and integration service checks are not treated as errors while a VM is powered off.

## v0.13.4

- Navigation and information architecture have been improved.
- VM, host, cluster, task, and audit areas are easier to distinguish.

## v0.13.3

- A structured versioning system has been introduced.
- Version information is now visible in the application.

## v0.13.0–v0.13.2

- The task management foundation has been introduced.
- More VM operations are tracked as tasks.
- Dashboard task visibility has been expanded.

## patch-10.12

- VM details now include a compact health and status summary.
- Host VM tables show consistent health, resource, network, checkpoint, and integration information.
- Unknown values are displayed consistently instead of appearing empty.
- Host warning badges open a complete warning list.
- Checkpoint warning thresholds can be configured globally and per host.
- Accepted checkpoints no longer generate warnings.
- Views react to live status changes without requiring manual reloads.

## patch-10.11

- Missing VM operations are now available from the interface.
- Replication that is not configured is displayed as an informational state.
- VM security information such as TPM and shielding is visible in read-only mode.
- Checkpoint actions now show clear success and error feedback.
- Integration Services status is displayed correctly.
- Large ISO uploads are handled more safely.
- Network adapter information distinguishes unavailable data from zero adapters.

## patch-10.10c

- Volume Shadow Copy is no longer reported as critical simply because the service is idle.
- A disabled or genuinely faulty VSS service is still reported appropriately.

## patch-10.10b.2

- Structured audit details no longer cause the audit page to fail.
- Host and VM filters in the audit log work correctly.

## patch-10.10b

- General stability and API completeness have been improved.

## patch-10.10a

- A dashboard crash after the first start has been fixed.
- Volume purposes can now be saved correctly.

## patch-10.10

- Clear states such as unavailable, unknown, pending, and not configured have replaced empty or cryptic values.
- VM health now distinguishes healthy, warning, critical, and unknown states.
- Checkpoint age is evaluated and shown as a warning or critical condition.
- Virtual disk allocation and actual usage are displayed separately.
- Integration Services are grouped into important and optional services.
- VM networking shows connection, IP, VLAN, and security features.
- VM settings include contextual guidance.
- Host details now include a structured issue list.
- Page-level failures show a recoverable error panel instead of a blank screen.

## patch-10.9a

- Host details now include hardware, BIOS, restart state, Windows updates, services, network throughput, checkpoint information, and top CPU-consuming VMs.
- Volume purposes can be assigned and retained.
- Performance history is recorded for later display.

## patch-10.9

- Host uptime and boot time are visible.
- Host health evaluation and a structured issue list have been introduced.
- Host headers now include health and issue indicators.

## patch-10.8c

- Free memory values are calculated correctly.
- Audit log stability and filtering have been improved.
- Dashboard scrolling and audit presentation have been refined.

## patch-10.8b

- Background data collection has been optimized for different update intervals.
- Dashboard widgets now include heartbeat, memory pressure, disk I/O, and network information.
- Virtual switch changes refresh related data immediately.

## patch-10.8a

- The first dashboard has been introduced with host, VM, checkpoint, and audit information.
- File browser navigation has been corrected.

## patch-10.8

- Hosts can be edited from the settings area.
- Frontend deployment output is handled correctly.

## patch-10.7

- ISO files can be uploaded, mounted, and ejected from VM details.
- Storage warning thresholds are available per host.
- Audit navigation and presentation have been improved.
- A console action is available from VM details.

## patch-10.6

- VM rename, export, and storage migration actions have been added.
- Application settings are now available.
- Network adapter management has been improved.

## patch-10.5

- General stability and service integration have been improved.

## patch-10.4

- Host CPU, uptime, and operating system information are collected more reliably.

## patch-10.3

- The HV-Desk product name is now used consistently throughout the interface.
- VM and host data collection has been stabilized.

## patch-10.2

- File browsing now uses reliable Windows volume information.
- Host headers show CPU, uptime, operating system, and IP details.
- VM details include IDs, notes, network adapter counts, IP addresses, and checkpoint counts.

## patch-10.1

- VM deletion can optionally remove the associated VM directory.
- File browsing is available as a dedicated page and inline view.
- Host summaries and VM tables include more information and export options.

## phase10

- VM security information such as TPM, shielding, and encryption is visible.
- Advanced VM network protection options are available.
- Virtual disk quality-of-service settings can be configured.
- SCSI controllers can be added and removed.
- NUMA and memory priority settings are available.
- VM details include compact resource and uptime summaries.
- VM table columns can be reordered, resized, and exported.
- The first read-only host file browser has been introduced.

## phase9

- Cluster support has been introduced for standalone hosts and cluster nodes.
- New views are available for firmware, Integration Services, replication, and settings.
- Checkpoints are displayed in a dedicated tree view.
- Host tabs, VM tables, and the sidebar have been expanded.
- VMs are listed beneath their hosts for faster navigation.
- VM table columns can be resized.

## phase8

- VM deletion can optionally remove associated files.
- ISO files can be mounted and ejected.
- Virtual disks can be added, detached, and expanded.
- Network adapters can be added, removed, and configured.
- Virtual switches can be created and managed.
- VM states refresh automatically.

## phase7

- The application has been consolidated into a single project structure.
- A guided VM creation wizard has been introduced.
- VM settings are available for CPU, memory, firmware, and checkpoints.
- Multiple VMs can be started, stopped, or migrated together.
- Live Migration is available through a dedicated dialog.

## phase6b

- Automatic background refresh has been introduced.
- VM uptime, network speed, and virtual disk information are displayed more accurately.

## phase6

- VM details now include dedicated network, storage, and services tabs.
- Hosts can be opened to view CPU, memory, storage, and Hyper-V information.
- Checkpoint loading is smoother and no longer causes visible page flicker.

## phase5

- The first web interface for HV-Desk has been introduced.
- Host and VM navigation, VM tables, VM details, and checkpoint views are available.
- Secure sessions, live updates, and remote host communication form the initial application foundation.

## phase4

- The first connected application services and live-update capabilities were introduced.
- HV-Desk could run continuously as a managed server service.
- The foundation for the later web interface was established.

## phase3

- Secure user sessions and domain-based host access were introduced.
- Persistent storage for application data became available.
- Hosts could be registered and managed centrally.
- The initial audit and security foundations were established.

## phase2

- The first application backend and remote host communication were introduced.
- HV-Desk could retrieve basic host and virtual machine information.
- Initial error handling was added for remote operations.

## phase1

- The HV-Desk project was created as a central management interface for virtualized infrastructure.
- The initial concepts for hosts, virtual machines, storage, and daily operations were defined.
- The project roadmap and application architecture were established.
