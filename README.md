# TouchWorkstation

**Your developer workstation. From anywhere.**

TouchWorkstation turns an Ubuntu computer into a touch-first development workstation you can use from a phone, tablet, or browser.

Your projects, terminals, GitHub credentials, Docker containers, development servers, desktop applications, and coding agents stay on **your own computer**. TouchWorkstation gives you a mobile control surface for them.

> **Alpha software:** TouchWorkstation is actively being tested. Expect bugs. If something breaks, please open an issue — those reports directly shape the next build.

## Why TouchWorkstation?

Remote desktop works, but it was never designed around a phone. SSH works, but it doesn't give you one place for projects, previews, GitHub, Docker, graphical apps, and coding agents.

TouchWorkstation is being built around a different idea:

**Your existing Linux workstation is the server. Your phone is the control surface.**

## Current alpha features

- Touch-first mobile interface
- Persistent `tmux`-backed terminal sessions
- Project discovery and management
- Local development-server launching and previews
- Git and GitHub CLI workflows
- Docker container controls and logs
- Managed graphical Ubuntu desktop through noVNC
- Files scoped to the workstation user's home directory
- Tailscale-oriented remote-access setup
- Agent workspaces for tools such as Claude Code, Codex, Hermes, and local runtimes
- Agent task-board and chat experiments
- Installable PWA for iPhone/iPad

## What TouchWorkstation is NOT

TouchWorkstation is not an AI subscription and does not sell tokens or inference.

Coding agents and services run using software and credentials installed on **your workstation**. TouchWorkstation is the interface and orchestration layer.

## Supported system

The current alpha package targets:

- Ubuntu 24.04
- amd64 / x86_64

Other distributions and architectures have not been validated yet.

## Install the current alpha

Download the latest `.deb` from **Releases**.

Then run:

```bash
sudo apt install ./touchworkstation_1.0.0-beta.28_amd64.deb
```

After installation:

```bash
touchworkstation-status
sudo touchworkstation-credentials
```

Open the address printed by `touchworkstation-status`.

### Remote access

The alpha is intended for LAN/private-VPN use.

**Do not expose TouchWorkstation, VNC, or development-server ports directly to the public internet.**

Tailscale or another private VPN is recommended for remote testing.

## Help test it

I am looking for developers, homelab users, Linux users, and people who genuinely try to work from a phone or tablet.

You do **not** need to write a formal bug report. If something feels confusing, slow, broken, clunky, or pointless, tell me.

Useful feedback includes:

- What device/browser you used
- Ubuntu version
- What you were trying to do
- What you expected
- What actually happened
- Screenshot or terminal output if available

[Open a bug report](../../issues/new?template=bug_report.yml) or [request a feature](../../issues/new?template=feature_request.yml).

## Known alpha priorities

The current focus is not adding dozens of new features. It is making the core workflow dependable:

1. Persistent mobile terminal + usable scrollback
2. Reliable agent terminal/chat interaction
3. Projects and localhost previews
4. GitHub workflow
5. Docker workflow
6. Installation and upgrades
7. Mobile UX and reconnect behavior

See [ROADMAP.md](ROADMAP.md) for more.

## Security

TouchWorkstation can execute commands on the host workstation. Install it only on a computer you control and keep access behind your LAN or a private VPN during the alpha.

Please **do not post security vulnerabilities publicly**. See [SECURITY.md](SECURITY.md).

## Source code

The application is currently **source-available to the development team but not published in this public alpha repository** while licensing and commercialization are being finalized.

This repository is the public home for releases, documentation, testing, issues, feedback, and the roadmap.

## The goal

I built TouchWorkstation because I wanted the horsepower and environment of my real Ubuntu workstation with me without rebuilding my entire development life in the cloud.

The alpha now needs real users more than it needs assumptions.

If that problem sounds familiar, install it, break it, and tell me what needs to change.
