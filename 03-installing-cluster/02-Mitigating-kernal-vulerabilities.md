# Mitigating Kernel Vulnerabilities

- Blocking Dynamic Module
- Kernal.Modules disabled
- Adaptive Stack Layout Randomization
- Hardware Security Features
- No (eXecute)
- ExecShield
- Vt-d Virtualization
- Trusted Platform Module (TPM) (https://trustedcomputinggroup.org/resources/?)[https://trustedcomputinggroup.org/resources/?]
- Trusted Executed Technology (TXT)
- Integrity Management
    - Integrity Measurement Architecture (IMA)
- Integrity Management with dm-verity
    - check the device tempering
    - this check the hash block by block
- Linux Security Modules (LSM)
    - This is API which hooks all the security apis
    - The following LSMs have been incorporated into the mainline Linux kernel:
        - AppArmor: To restrict capabilities of an application.
        - SELinux: Implements MAC (Mandatory Access Control)
        - Smack (Simplified Mandatory Access Control Kernel)
        - TOMOYO: MAC implementation and system analysis.
- Seccomp (Secure Code Mode)
    - Secure computing mode (seccomp) is a mechanism which restricts access to system calls by processes.
    - its called mode1 and provide only access for write(), read(), exit(), sigreturn
    - mode2 written for google chrome
    