# Pause listening samples

Voice `nl_BE-nathalie-medium`, rendered with the dengjen CLI (lazy mode, with ZirekHQ/dengjen#558 and #559 applied), noise_scale and noise_w at 0. Listener: an experienced NVDA user who normally reads with eSpeak NG at about 440 words per minute.

## 1. Pause length at 1.95x (engine rate 29, about 440 words per minute)

Text: "Ik bleef de hele dag binnen, omdat het buiten veel te koud was om te fietsen. Druk op enter om het bestand te openen, of gebruik de pijltjestoetsen om door de lijst te bladeren. De winkel ging pas open, nadat de laatste leverancier zijn spullen had gebracht."

- `1a`: unchanged. The model's pauses (about 100, 80 and 175 ms at 1x) come out at 40 to 85 ms.
- `1b`: every silent stretch of at least 35 ms after sonic made 2x as long (zeros inserted in its middle).
- `1c`: the same, 3x. Preferred. Costs about 5% in words per minute.

## 2. Everything together at about 360 words per minute

Text: four sentences, two with a clause boundary without a comma ("... binnen omdat ...", "... strand hoewel ...").

- `2a`: sonic only (engine rate 22).
- `2b`: a comma inserted before unambiguous Dutch subordinating conjunctions (omdat, hoewel, nadat ...), pauses after sonic 2.5x, 150 ms between sentences.
- `2c`: as 2b, but the speed-up split between length_scale 0.74 and sonic 1.3x (engine rate 16), at the same overall length. Preferred.
