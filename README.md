# stable-diffusion-webui-m1

Many examples of Stable Diffusion use `conda` instead of `venv`.
This is another variant of modified install script to use `venv` and `rustup` as I don't want them to mass up my system.

----

## Installation

I support two version of implementation.
In case of update, you need to run the same command.

### invokeai

See more in https://github.com/invoke-ai/InvokeAI

```sh
curl -sL https://raw.githubusercontent.com/seia-soto/stable-diffusion-webui-m1/master/invokeai.sh > invokeai.sh
chmod +x ./invokeai.sh
```

The default command for invokeai is `python scripts/invoke.py --web --free_gpu_mem;`.

### stable-diffusion-webui

See more in https://github.com/AUTOMATIC1111/stable-diffusion-webui

```sh
curl -sL https://raw.githubusercontent.com/seia-soto/stable-diffusion-webui-m1/master/webui.sh > webui.sh
chmod +x ./webui.sh
```

The default command for webui is `python webui.py --precision full --no-half --opt-split-attention-v1 --use-cpu GFPGAN CodeFormer;`.

## Steps

The scripts are consisted of simple steps.

1. Install prerequisites: `./script.sh -i`
2. Put your model in proper directory.
3. Start the server: `./script.sh -s`, or using custom arguments: `./scripts.sh -s --` (allows you to run as CLI)

> When using the custom arguments, pasting others' code can lead you to run dangerous code.
> The `-s` option at the first will not be passed to the program if any remaining argument exists.

## Options

## Troubleshooting

### Any problem related to Python LZMA module

It's because your `xz` package is not properly set up while building the Python binary.
You'll want to reinstall it.

```sh
eval "$(pyenv init -)";
pyenv uninstall 3.10.0;
```

After the process above, make sure you to restart the shell before running any other scripts.

### Migrating from `aacontrols.sh`

`aacontrols.sh` is for `stable-diffusion-webui`.
Delete it and switch to `webui.sh`.

## License

You can modify or redistribute the script for public good without any permission.
