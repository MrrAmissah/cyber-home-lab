# Sanitising a capture before committing an excerpt

Raw captures stay out of git. To publish an excerpt:

1. Filter to the flows the write-up needs and export only those packets (`File → Export Specified Packets`).
2. Anonymise addresses: `tcprewrite --seed=<n> --infile=in.pcapng --outfile=out.pcapng` or Wireshark's address-anonymisation tools; map any remaining public IP to the RFC 5737 documentation ranges.
3. Confirm no credentials, cookies or personal data remain (`http`, `tls.handshake.extensions_server_name`, `dns`).
4. Prefer screenshots or text excerpts over whole files. If a file must be shared, keep it under 2 MB and name it `*.sanitized.pcapng` in `evidence/` of the lab folder (raw patterns are ignored; sanitised files are allowed by name).
