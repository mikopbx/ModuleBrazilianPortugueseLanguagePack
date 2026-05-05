# ModuleBrazilianPortugueseLanguagePack

Complete Brazilian Portuguese language pack for MikoPBX including UI translations and voice prompts.

## What's Included

- **Voice Prompts**: Brazilian Portuguese voice prompts for system menus, greetings, and notifications
- **UI Translations**: Complete Brazilian Portuguese translation of MikoPBX admin interface
- **Text Mapping**: `Sounds/core-sounds-pt-br.txt` — list of TTS-generated prompts with their text

## Installation

1. Download and install the module from MikoPBX Marketplace
2. Enable the module in **Modules** section
3. Go to **General Settings** and select Brazilian Portuguese (Português (Brasil)) as the system language

## Requirements

- MikoPBX 2025.1.1 or later

## TTS Attribution

The full set of Brazilian Portuguese voice prompts (~570 phrases) was synthesized
using neural Text-to-Speech to provide a consistent native-voice experience and
to replace legacy `.gsm` files with high-quality 22 kHz `.wav` audio:

- **Engine**: [Piper TTS](https://github.com/rhasspy/piper)
- **Voice model**: `pt_BR-faber-medium` (from [rhasspy/piper-voices](https://huggingface.co/rhasspy/piper-voices))
- **Sample rate**: 22050 Hz
- **Format**: WAV (PCM signed 16-bit, mono)

A small number of telephony tones (`beep`, `beeperr`, `ascending-2tone`,
`descending-2tone`, `confbridge-join`, `confbridge-leave`) and `silence/*` files
are non-spoken audio; tones are decoded losslessly from the original Asterisk
`.gsm` source, and silence files are generated as digital silence.

The text for each TTS-generated prompt is stored in `Sounds/core-sounds-pt-br.txt`
for reference and regeneration.

On module installation, MikoPBX automatically converts WAV files to all Asterisk
formats (ulaw, alaw, gsm, g722, sln) for optimal codec compatibility.

## License

- Module code: GNU General Public License v3.0
- Sound files: CC BY-SA 4.0 (Asterisk Sound Files)
- TTS engine: Piper TTS (https://github.com/rhasspy/piper)

## Copyright

- Module development: © 2017-2026 Alexey Portnov and Nikolay Beketov
- Voice prompts: From official Asterisk release (CC BY-SA 4.0)
- Voice synthesis (missing prompts): Generated using open-source TTS models
