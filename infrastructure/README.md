# Infrastructure & DevOps


User Management
- automated provisioning scripts for onboarding/offboarding
- integrates with LDAP

Python for DevOps ideas (from "Python for DevOps" book):
- testinfra for infrastructure testing: https://testinfra.readthedocs.io/
  - check if services are running, ports are open, files exist
  - way better than bash scripts
- mixing Python with bash:
  - subprocess module for when you need shell commands: use `subprocess.run()` with `capture_output=True`
  - or calling python inside bash script
- load testing with molotov: https://molotov.readthedocs.io/
  - async load testing framework

General approach:
- automate repetitive tasks (if you do it twice, script it)
- logging > print statements for deployed scripts
- use argparse or click for CLI interfaces
- schedule with cron or systemd timers, not while True loops