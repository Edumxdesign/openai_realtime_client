# openai_realtime_client

Build a terminal voice assistant that sends microphone audio to OpenAI's Realtime API and plays back responses. This experimental Python Realtime API client includes manual and Server VAD examples, plus LlamaIndex tool integration for custom assistant actions.

## Features

- Run a voice conversation directly in the terminal with the supplied CLI examples.
- Choose manual voice activity detection or Server VAD to control conversation turns.
- Interrupt the assistant during playback in the streaming example.
- Connect LlamaIndex tools so the assistant can call custom functions.

## Installation

Install the system audio dependencies on macOS:

```bash
brew install ffmpeg portaudio
```

Install the Python package:

```bash
pip install openai-realtime-client
```

Set your OpenAI API key:

```bash
export OPENAI_API_KEY="sk-..."
```

The examples run from a source checkout or an extracted source archive. The package name above comes from the donor project; a separate package publication for this standalone project is not established here.

For the source download below, replace `OWNER` with this project's GitHub owner. The URL requires a published `v0.1.0` tag and downloads the source archive associated with that release.

```bash
curl -L https://github.com/OWNER/openai_realtime_client/archive/refs/tags/v0.1.0.tar.gz -o openai_realtime_client-v0.1.0.tar.gz
```

## Usage

From the project root, run the manual VAD example:

```bash
python ./examples/manual_cli.py
```

Try asking for your phone number to exercise the example's function-calling flow. Read the example before substituting your own tools or personal data.

For Server VAD and interruption support, run the streaming example:

```bash
python ./examples/streaming_cli.py
```

**Use headphones in a quiet environment.** The streaming example is experimental, and its audio interaction can be uneven.

To customize assistant actions, start with the tool definitions in the examples and replace them with your own LlamaIndex tools.

## License

MIT. This project is based on [run-llama/openai_realtime_client](https://github.com/run-llama/openai_realtime_client), which is also MIT-licensed. Retain the original copyright and permission notice in copies or substantial portions of the donor code.

## Related projects

Other repositories supplied as projects from the same author are listed below. Their functionality was not included in the source material, so no feature descriptions are asserted here.

- [leololahe-bot/lastbackend](https://github.com/leololahe-bot/lastbackend): Consult its README for its purpose and usage.
- [Songraf/stagerag](https://github.com/Songraf/stagerag): Consult its README for its purpose and usage.
- [rachmathidayat2021/prometheus](https://github.com/rachmathidayat2021/prometheus): Consult its README for its purpose and usage.

