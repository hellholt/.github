# ๐ฅ Hellholt ๐ฅ

Hellholt is my homelab.  This is where, after a long day of beating my head against other people's infrastructure, I beat my head against my own.

## ๐คฉ Latest Stuff
- Set up PCIe passthrough, though I need to fully parameterize this.
- Revamped Torrent client orchestrator.
- Finished transitioning dotfiles from Ansible-based workflow to YADM.
- Got SSH certificates working!  Instead of yeeting pubkeys into `~/.ssh/authorized_keys`, the setup process now takes slightly longer because of all the slurping and signing!
- Cluster-wide Traefik reverse proxy with LetsEncrypt, instead of manually adding hosts and certs in HAProxy on my router/firewall.
- Per-host Traefik reverse proxy, rather than having to futz with the node ports.
- Refactored massively, since the old IaC was a nightmare.
- Added Bash command for more easily executing the Ansible roles where the ๐ชmagic๐งโโ๏ธ happens.
- Each host gets a MOTD of a coat of arms and colorful Bash prompt complete with appropriate emoji corresponding to their house.
- Added Organizr so I know how to get to all of this crap.
- Much better renders of the shields for MOTD.

## ๐ด Stuff I've Learned
- Yeah, hosting your blog on Kubernetes is a joke, but... really... Kubernetes is overkill and unnecessary complexity for a homelab and I wouldn't be bothering with it if it weren't for work.  Now learning this for a second time.
- Cert-Manager's pattern of using secrets to store certs introduces complexity for backup/restore I don't really want to bother with.  It's easier just to do TLS termination outside Kubernetes clusters with Traefik and persist generated certs in the filesystem.
- I never really need to SSH from one host to another; just from my local/control machine into one host or another.  The various mucking around I've done with SSH (first orchestrating SSH pub key circulation, and then SSH certificates) has been really unnecessary.  I just like the idea.

## ๐ฎ Future Stuff
- Move Traefik to Marbrand (Firewall), shift sitewide proxy configuration into separate role.
- Maybe shift SSH certificate management to something like HashiCorp Vault.
- Continue splitting out stuff from huge hellholt.setup_host Ansible role into more focused roles.
- Install Code-Server on each LXC container.
- Improve how I handle BorgBackup stuff, add a BorgBase description, split out config, etc.
- Set up Raspberry Pi cluster.
- Revamp my Reddit archiving.
- Shift Device archives from Dayne to Lefford.
- Add second 6x12TB RAIDZ2 to Lefford.
- Move Home Assistant from a VM to an LXC container.
- Add Musicbrainz mirror.
- Make Last Will and Testament, lol, so my wife knows how to dismantle and sell this crap when I die.
- Docker pullthrough registry.
- Install SAS HDDs on Ryswell or Celtigar for lulz
- Wireguard
- Improve Download management.
- Kubernetes apps, extend and refine GitOps, etc.

## ๐ป (Partial) Inventory:
- ๐ด Ryswell: Dell R720 SFF/128GB/1TB NVMe/Proxmox
- ๐ฆ Celtigar: Dell R720 SFF/128GB/1TB NVMe/Proxmox
- โ๏ธ Lefford: Dell R720XD LFF/128GB/1TB NVMe/6x12TB RAIDZ2/Proxmox
- ๐ซ Dayne: Synology DS1813+/6GB/8x12TB Ext4 SHR-2/DSM
- ๐ฅ Uller: Synology DS2415+/16GB/12x12TB BtrFs SHR-2/DSM
- ๐ Fossoway: Apple 2015 MacBook Pro/16GB/1TB/macOS

<!--

**Here are some ideas to get you started:**

๐โโ๏ธ A short introduction - what is your organization all about?
๐ Contribution guidelines - how can the community get involved?
๐ฉโ๐ป Useful resources - where can the community find your docs? Is there anything else the community should know?
๐ฟ Fun facts - what does your team eat for breakfast?
๐ง Remember, you can do mighty things with the power of [Markdown](https://guides.github.com/features/mastering-markdown/)
-->
