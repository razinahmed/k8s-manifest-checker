# K8s Manifest Checker

![Security](https://img.shields.io/badge/Security-Tool-red)
![Bash](https://img.shields.io/badge/Bash-Script-green)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Security-blue)
![License](https://img.shields.io/badge/License-MIT-blue)

A Kubernetes manifest security linter that analyzes YAML deployment files for misconfigurations, privilege escalation risks, and security policy violations before they reach your cluster.

## Description

K8s Manifest Checker scans Kubernetes manifests (Deployments, Pods, Services, etc.) for security issues such as running containers as root, missing resource limits, overly permissive RBAC roles, and insecure volume mounts. Integrates into CI/CD pipelines to enforce security policies at the manifest level.

## Features

- Static analysis of Kubernetes YAML manifests
- Detection of containers running as root or with privileged mode
- Resource limits and requests validation
- RBAC role and ClusterRole permission auditing
- Network policy and service exposure checks
- SecurityContext and PodSecurityPolicy validation
- Missing readiness/liveness probe detection
- Makefile-based build and test workflow

## Tech Stack

- **Language:** Bash
- **Platform:** Kubernetes
- **Tools:** kubectl, yq (YAML parser)
- **Target OS:** Linux / macOS
- **Build Tool:** GNU Make

## Quick Start

```bash
# Clone the repository
git clone https://github.com/razinahmed/k8s-manifest-checker.git
cd k8s-manifest-checker

# Review the checker
make build
make test

# Scan a Kubernetes manifest
# bash scripts/check.sh /path/to/deployment.yaml
```

## Usage

```bash
# Build and test
make build
make test
```

## Project Structure

```
k8s-manifest-checker/
  styles/
    theme.css          # UI theme configuration
  Makefile             # Build and test automation
  SECURITY.md          # Security policy
  LICENSE              # MIT License
```

## Contributing

Contributions are welcome. Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
