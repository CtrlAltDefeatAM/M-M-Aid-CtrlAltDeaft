# Privacy Design

The starter website is local-first.

It does not include:
- user accounts;
- a character database;
- analytics;
- telemetry;
- advertising integrations;
- external API calls;
- a character-file upload endpoint.

The browser reads the selected file using `File.text()` and parses it in memory.

Future features that transmit or persist character data must be explicitly documented before being enabled.
