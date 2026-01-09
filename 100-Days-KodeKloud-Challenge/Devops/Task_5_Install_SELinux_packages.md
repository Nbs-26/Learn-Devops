[Solution](https://www.nbtechsupport.co.in/2021/01/selinux-installation-kodekloud-engineer.html)

SELinux(Security-Enhanced Linux) is a Mandatory Access Control (MAC) system, developed by the NSA. 
SELinux was developed as a replacement for Discretionary Access Control (DAC) that ships with most Linux distributions.

The difference between DAC and MAC is how users and applications gain access to machines. 
Traditionally, the command sudo gives a user the ability to heighten permissions to root-level. Root access on a DAC system gives the person or program access to all programs and files on a system.

A person with root access should be a trusted party. But if security has been compromised, so too has the system. SELinux and MACs resolve this issue by both confining privileged processes and automating security policy creation.

SELinux defaults to denying anything that is not explicitly allowed.
SELinux has two global modes, permissive and enforcing.
Permissive mode allows the system to function like a DAC system, while logging every violation to SELinux. 
The enforcing mode applies a strict denial of access to anything that isn’t explicitly allowed. To explicitly allow certain behavior on a machine, the system administrator have to write policies that allow it. 
