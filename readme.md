# SpAIder

## Bitnet

### Virtualization

Relies on podman by default, docker should work in the same manner.

Build image.

```bash
$ ./bitnet build
```

Build image using docker specifically.

```bash
$ VIRTUALIZATION=docker ./bitnet build
```

Run shell inside image.

```bash
$ ./bitnet run
```

Inside container either use history file or these calls

```bash
# Activate virtual environment
$ . ${HOME}/miniconda3/bin/activate && conda activate venv-bitnet
# Run inference call on the reduced model
$ python run_inference.py -m models/bitnet_b1_58-large/ggml-model-i2_s.gguf -p "You are a helpful assistant"
```
