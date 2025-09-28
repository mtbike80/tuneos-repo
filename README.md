# TuneOS Repository

This is the official **APT repository** for TuneOS. For the **ISO build files and tooling**, see the [tuneos-build repository](https://github.com/mtbike80/tuneos-build).

TuneOS is a Debian-based distribution tailored for audio production and general, everday use for tech-savvy people. It's built on the premise that this will appeal to those who are musical, and would enjoy expressiving their creativity on an OS that is also easy and robust enough to use exclusively.

TuneOS 1 "Skipjack" is a work-in-progress. The targeted completime timeframe is the end of 2025.


---

## 📦 What’s Inside

- **tuneos-meta** – meta-package that pulls in the TuneOS default applications.
- **tuneos-artwork** – wallpapers, Plymouth, GRUB, KDE splash branding.
- **tuneos-defaults** – OS identity, realtime tweaks, PipeWire/JACK defaults, CPU governor.
- Additional packages maintained by the TuneOS team.

---

## 🔑 Repository Setup

Import the TuneOS signing key and add the repository:

```bash
sudo mkdir -p /usr/share/keyrings
curl -fsSL https://mtbike80.github.io/tuneos-repo/tuneos.gpg | sudo tee /usr/share/keyrings/tuneos.gpg > /dev/null

echo "deb [signed-by=/usr/share/keyrings/tuneos.gpg] https://mtbike80.github.io/tuneos-repo resonance main" | \
  sudo tee /etc/apt/sources.list.d/tuneos.list

sudo apt update
