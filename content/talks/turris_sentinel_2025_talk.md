+++
title = 'Turris Sentinel - Sentinel Report Q2-Q3 of 2025 talk (presentation)'
date = 2025-10-04
+++

# Turris Sentinel - Sentinel Report Q2-Q3 of 2025 talk

At LinuxDays 2025, the largest Czech Linux and open-source conference held on
October 4–5 at the Faculty of Information Technology of CTU in Prague-Dejvice,
I co-presented the *Turris News* talk with Michal Hrušecký on Saturday,
October 4, in room 111. Michal covered the unveiling of the new Turris router
and the state of Turris OS 9, while I presented Turris Sentinel, our internet
security research program.

Turris Sentinel gathers anonymized attack data from opt-in Turris routers via
minimal honeypots (HTTP, FTP, SMTP, Telnet, plus an SSH honeypot on our
servers) and firewall logs. My talk included the Sentinel report for Q2–Q3 of
2025: total incidents over IPv4 grew by 86.57% to over 3.1 billion in Q3, while
the number of unique attackers dropped by 22.41%—fewer attackers, but far more
active ones. IPv6 remained a marginal attack surface, accounting for well under
one per mille of incidents.

SMTP was the most targeted trap (over 2.7 billion incidents in Q3), while
Telnet lost attractiveness yet still drew the most unique attackers. I also
highlighted the most attacked ports, the Hall of Fame/Shame of top attacking
IP addresses and ASNs, and the most common credentials tried by attackers,
with `root`/`admin` and `123456`/`password` unsurprisingly dominating.

The talk concluded with standard advice: stop using default passwords, prefer
IPv6, and if you own a Turris device, enable Sentinel.

A recording of the talk is available:

{{< youtube "PmbxCu-Yt7Q">}}

## Resources

- [Turris Sentinel](https://view.sentinel.turris.cz) - Live security data visualization
- [Turris Project](https://www.turris.com/en/) - Open-source router platform
