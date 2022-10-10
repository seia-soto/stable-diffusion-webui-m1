# stable-diffusion-webui-m1

```sh
curl -sL https://raw.githubusercontent.com/seia-soto/stable-diffusion-webui-m1/master/aacontrols.sh > aacontrols.sh
chmod +x ./aacontrols.sh

./aacontrols.sh
```

```
A helper utility for ARM based macs to initiate AUTOMATIC1111/stable-diffusion-webui

Install prerequisites: $1 -i
Start server: $1 -s
Clean up directory: $1 -c

----

The following stacks will be installed and used.
- Rust via Rustup
- Python 3 and venv via Pyenv
- Homebrew and the following packages: 'cmake protobuf git wget'

Copyright 2022 HoJeong Go. All rights reserved.
At the any time, you can modify, or fork and redistribute the script.
```

## References

- https://github.com/AUTOMATIC1111/stable-diffusion-webui
