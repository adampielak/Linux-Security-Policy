# Linux-Security-Policy

The Linux Audit system provides a way to track security-relevant information on your system. Based on pre-configured rules, Audit generates log entries to record as much information about the events that are happening on your system as possible. This information is crucial for mission-critical environments to determine the violator of the security policy and the actions they performed. Audit does not provide additional security to your system; rather, it can be used to discover violations of security policies used on your system.

Properly configuring your audit rules is critical to meeting compliance requirements and ensuring that you have the relevant logs to detect security incidents. The following scripts will automatically back up your current audit rules and pull down and configure a larger, more complete list of audit rules. It's recommended that you review the rules prior to implementation to ensure that you aren't duplicating any logging you may already be recieving from other sources, such as a SIEM agent.

The following scripts will automatically configure advanced auditing of changes and modifications to:
* Date and Time
* Users and Groups
* Network Environments
* Mandatory Access Controls
* Login and Logout
* Session Initiation
* Discretionary Access Controls
* Unsuccessful Unauthorized File Access Attempts
* Use of Privleged Commands
* Successful File System Mounts
* File Deletion Events by Users
* System Administration Scope
* System Administrator Actions
* Kernel Module Loading and Unloading

## CentOS7/RHEL7

```
curl https://raw.githubusercontent.com/Starke427/Linux-Security-Policy/master/auditd_setup_el7.sh > auditd_setup_el7.sh
chmod 700 auditd_setup_el7.sh
./auditd_setup_el7.sh
```

## Debian8/Ubuntu16

```
curl https://raw.githubusercontent.com/Starke427/Linux-Security-Policy/master/auditd_setup_ubuntu16.sh > auditd_setup_ubuntu16.sh
chmod 700 auditd_setup_ubuntu16.sh
./auditd_setup_ubuntu16.sh
```
