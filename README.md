# Rate-split listening samples

Three renders of the same two Dutch sentences at about 2.5x speed (4.9 to 5.0 s each), for a Dengjen feature request about how the NVDA rate setting is applied.

- `a_sonic_only_2.5x.wav`: length_scale 1.0, sonic 2.5x (engine rate 40). This is how Dengjen applies NVDA rate 100% today.
- `b_length_scale_0.74_sonic_2.0x.wav`: length_scale 0.74, sonic 2.0x (engine rate 30).
- `c_length_scale_0.45_sonic_1.6x.wav`: length_scale 0.45, sonic 1.6x (engine rate 22).

Voice: `nl_BE-nathalie+RT-medium`. Rendered with the dengjen CLI in realtime mode (chunk_size 55), with ZirekHQ/dengjen#558 and #559 applied, and noise_scale and noise_w at 0 so the three files differ only in how the speed-up is split.

Text: "Als we dit doel willen bereiken is een duidelijke en ondubbelzinnige tekst noodzakelijk, zeker wanneer er veel mensen bij betrokken zijn en de tijd begint te dringen. Druk op enter om het bestand te openen, of gebruik de pijltjestoetsen om door de lijst te bladeren."
