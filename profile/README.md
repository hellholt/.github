# 🔥 Hellholt 🔥

Hellholt is my homelab.  This is where, after a long day of beating my head against other people's infrastructure, I beat my head against my own.

## 🤩 Latest Stuff
- Got SSH certificates working!  Instead of yeeting pubkeys into `~/.ssh/authorized_keys`, the setup process now takes slightly longer because of all the slurping and signing!
- Cluster-wide Traefik reverse proxy with LetsEncrypt, instead of manually adding hosts and certs in HAProxy on my router/firewall.
- Per-host Traefik reverse proxy, rather than having to futz with the node ports.
- Refactored massively, since the old IaC was a nightmare.
- Added Bash command for more easily executing the Ansible roles where the 🪄magic🧙‍♂️ happens.
- Setup SyncTube for YouTube archiving.
- Setup Komga for Comics.
- Each host gets a MOTD of a coat of arms and colorful Bash prompt complete with appropriate emoji corresponding to their house.

## 👴 Stuff I've Learned
- Yeah, hosting your blog on Kubernetes is a joke, but... really... Kubernetes is overkill and unnecessary complexity for a homelab and I wouldn't be bothering with it if it weren't for work.  Now learning this for a second time.
- Cert-Manager's pattern of using secrets to store certs introduces complexity for backup/restore I don't really want to bother with.  It's easier just to do TLS termination outside Kubernetes clusters with Traefik and persist generated certs in the filesystem.
- I never really need to SSH from one host to another; just from my local/control machine into one host or another.  The various mucking around I've done with SSH (first orchestrating SSH pub key circulation, and then SSH certificates) has been really unnecessary.  I just like the idea.

## 🔮 Future Stuff
- Improve how I handle BorgBackup stuff, add a BorgBase description, split out config, etc.
- Set up Raspberry Pi cluster.
- Finish transitioning dotfiles from Ansible-based workflow to YADM.
- Revamp my Reddit archiving.
- Shift Books from Dayne to Lefford, set up book server (probably Ubooquity).
- Shift Device archives from Dayne to Lefford.
- Add second 6x12TB RAIDZ2 to Lefford.
- Revamp Torrent client orchestrator.
- Move Home Assistant from a VM to an LXC container.
- Add Musicbrainz mirror.
- Make Last Will and Testament, lol, so my wife knows how to dismantle and sell this crap when I die.
- Docker pullthrough registry.
- Install SAS HDDs on Ryswell or Celtigar for lulz
- Wireguard
- Organizr
- Shift Documents from Dayne to Lefford.
- Improve Download management.
- Move Games from Dayne to Lefford (these are RPGs, etc), consider a document management system or something similar.
- Move Images from Dayne to Lefford, consider some kind of image management system.
- Move Magazines from Dayne to Lefford, consider a magazine management system (Ubooquity?).
- Move Photos from Dayne to Lefford, consider some kind of photo management system.
- Move Plunking (TL;DR: all of my music books) from Dayne to Lefford, consider a document management system.
- Move Podcasts from Dayne to Lefford, revamp podcast archiving.
- Move Software from Dayne to Lefford.
- Move Tech (tech-specific books) from Dayne to Lefford, set up another book server (probably Ubooquity).
- Move Text from Dayne to Lefford -- is there a textfile management system?
- Move VideoGames from Dayne to Lefford (these are binary files -- ROMs and such), consider... something.  Launchbox?  IDK.
- Kubernetes apps, extend and refine GitOps, etc.

## 💻 (Partial) Inventory:
- 🐴 Ryswell: Dell R720 SFF/128GB/1TB NVMe/Proxmox
- 🦀 Celtigar: Dell R720 SFF/128GB/1TB NVMe/Proxmox
- ☀️ Lefford: Dell R720XD LFF/128GB/1TB NVMe/6x12TB RAIDZ2/Proxmox
- 💫 Dayne: Synology DS1813+/6GB/8x12TB Ext4 SHR-2/DSM
- 🔥 Uller: Synology DS2415+/16GB/6x12TB BtrFs SHR-2/6x3TB BtrFs SHR-2/DSM
- 🍎 Fossoway: Apple 2015 MacBook Pro/16GB/1TB/macOS

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://guides.github.com/features/mastering-markdown/)
-->
