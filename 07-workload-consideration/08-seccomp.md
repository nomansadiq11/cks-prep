# seccomp

Secure Computing Mode

- this is linux kernal feature that can be used to restrict the actions available within the container
- first iteration provide read(), write(), exit(), sigreturn()
- method2 BPF or eBFP program can be written and every system call go thourhg it
- in kubernetes serveral feataures available, such as syscall auditing and denial of disallowed

```yaml
spec:
  securityContext:
    seccomProfile:
      type: Localhost
      localhostProfile: profiles/audit.json
```
