# vlucash-wallet

A GUI wallet for [VluCash](https://github.com/VluCash/VluCash-Coin), based on `walletd`.

## Getting Started

To get started, install the prerequisites as detailed below, then look at the "Running" section

### Prerequisites

This program is written using Python 2.7.

It requires [PyGObject](https://pygobject.readthedocs.io/en/latest/getting_started.html) to be installed.

It also has the following prerequisites, installed via `pip`

* psutil
* requests
* tzlocal

Note that these have only been tested on ubuntu, let me know if anything else is required on Windows.

### Running

Getting this wallet running is easy.

Before starting, make sure `walletd` is running and **fully synced**.

An example launch command for `walletd` that means you do not have to start the daemon (ie, `Turtlecoind`) alongside it would be as follows:
```
./walletd -w <wallet file name> -p <wallet password> --local
```

**Note: opening your wallet with `walletd` renders it no longer readable by `simplewallet`. Please make a backup, as always.**

Having installed the prerequisites and made sure `walletd` is running, you can start it from a terminal

```
python start.py
```

And everything should start up as intended, provided you installed everything correctly.


## Building an executable

This project can be built with `pyinstaller`, if required. This will most likely be the case for full releases.

## Contributing

Feel free to submit a pull request, it will be reviewed and feedback given.

**Things that need doing**
* Hooking up of UI for sending TRTL (ui done, just needs backend doing)
* Automatically launching and closing walletd
* Settings
* About page
* Things marked with TODO in the code

## Authors

* **CodIsAFish** - *Initial work* - [CaptainMeatloaf](https://github.com/CaptainMeatloaf)

## License

This project is licensed under the LGPLv3 License.

## Acknowledgments

* RockSteady, for pointing me at the right docs
