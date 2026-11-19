# 00 – Wireshark capture method

**Date:** 2026-11 · **Status:** write-up pending

## Purpose
Establish a repeatable procedure for capturing a clean TCP session to a web server, so that the three-way handshake, TLS handshake and round-trip timing can be read without background noise.

## Setup
- Workstation: macOS, Wireshark, Wi-Fi interface.
- Target: a public website I'm permitted to browse (no active testing beyond normal browsing).

## Procedure (summary)
1. Restart the machine; close every background application; disable any VPN.
2. Start the capture on the active interface with no capture filter.
3. Open a fresh private browser window and load the site; browse two or three pages; stop after ~5 minutes.
4. Save as `.pcapng`, record the date, network and steps in notes.
5. Verify in the capture: `dns.qry.name contains "<site>"`, `ip.addr == <site-ip> && tcp.flags.syn == 1`, `tls.handshake.type == 1`, `tcp.analysis.ack_rtt`.
6. If no SYN appears, the browser reused a connection: close it fully and repeat from step 3.

## What I found / What I learned / Limits
To be completed after the related coursework is graded. Only the method and sanitised excerpts will be published.
