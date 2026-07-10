+++
title = 'Turris Sentinel - What has 2024 brought (blogpost)'
date = '2025-05-16'
+++

# Turris Sentinel - What has 2024 brought blogpost

Turris Sentinel, which has been reliably collecting attack data for nearly five
years since replacing the older uCollect monitoring system, became part of the
stable Turris OS (TOS) branch with version 5.1.0 released on August 29, 2020,
and fully replaced uCollect by April 2022. Beyond data collection,
Turris Sentinel also helps prevent internet attacks by regularly updating a
dynamic firewall on Turris devices, with the greylist freely available on
Sentinel View for public review. The project shares anonymized data with the
Czech National Security Team (CSIRT.CZ) for further analysis. Daily, Sentinel
processes around 23 million incident records from connected devices—nearly 1
million incidents per hour or 16,000 per minute—while also incorporating
minimalized honeypots (minipots) that simulate services like SMTP, HTTP, FTP,
and Telnet to capture attack attempts such as login attempts, connections,
message transmissions, or port scans. Between February 2024 and February 2025,
Sentinel recorded 8.3 billion incidents originating from 6.2 million unique
attackers across 232 countries and territories, with SMTP minipots attracting
79% of attacks, followed by Telnet (16%), HTTP (3%), and FTP (2%). The project
also logged 3.2 million unique passwords and 318,000 unique usernames attempted
by attackers. Most recorded actions were connection attempts (71%), followed by
small port scans (10.6%), message transmissions (9.6%), login attempts (7.7%),
and large port scans (1.1%). Geographical analysis, adjusted for internet user
density, revealed that while absolute attack numbers were highest in India,
China, the U.S., Brazil, and Taiwan, relative attack rates per 1,000 internet
users were most pronounced in Cape Verde, French Polynesia, Singapore, Greece,
and Hong Kong. In the past year, UDP protocol attacks dominated, with the most
targeted ports being 5353 (mDNS), 5678 (Neighbor discovery for MikroTik
routers), 51413 (BitTorrent Transmission), 10002 (Documentum software), and 67
(DHCP servers). Commonly attempted logins included *root*, *admin*, *user*,
*support*, and *test*, while frequently used passwords were *123456*,
*password*, *1qaz2wsx*, *p@ssw0rd*, and *12345*. The most common login-password
combinations were *enable/system*, *sh/shell*, *admin/admin*, *root/root*, and
*root/admin*. In December 2024, Turris OS 7.1 introduced IPv6 support via
nftables, enabling Sentinel to collect attack data over IPv6. Between January
and March 2025, the system recorded 667 million incidents, of which only
396,000 (0.59‰) originated from IPv6 addresses, with a similar proportion
(0.65‰) of unique IPv6 attackers. The data suggests significantly lower attack
activity over IPv6 compared to IPv4, highlighting its potential for enhanced
security against attacks.

Read the full post on CZ.NIC's blog: [Turris Sentinel - Co přinesl rok 2024](https://blog.nic.cz/2025/05/16/turris-sentinel-co-prinesl-rok-2024/)