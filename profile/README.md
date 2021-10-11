# :fire: Hellholt :fire:

Hellholt is my homelab: a cluster of clusters, some of which contain other clusters, and probably some of those will contain clusters too if they don't already.

## 🤩 Latest Stuff
- Got SSH certificates working!  Instead of yeeting pubkeys into `~/.ssh/authorized_keys`, the setup process now takes slightly longer because of all the slurping and signing!
- Cluster-wide Traefik reverse proxy with LetsEncrypt, instead of manually adding hosts and certs in HAProxy on my router/firewall.
- Refactored massively, since the old IaC was a nightmare.

## 🍦 Cool Stuff
- Each host gets a MOTD and colorful Bash prompt complete with appropriate emoji corresponding to their house.

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://guides.github.com/features/mastering-markdown/)
-->
