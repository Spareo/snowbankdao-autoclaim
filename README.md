# greets
```sh

 ❆ ❈ ❇ ❊ ❅ ❉ ❆ ❈ ❇ ❊ ❅ ❉ ❆ ❈ ❇ ❊ ❅ ❉ ❆ ❈ ❇ ❊ ❅ ❉ ❆ ❈ ❇ ❊ ❅ ❉ ❆ ❈
 ❅                                   __         __             ❅
 ❊ .-----.-----.-----.--.--.--.----.|  |.---.-.|__|.--------.  ❊
 ❇ |__ --|     |  _  |  |  |  |  __||  ||  _  ||  ||        |  ❇
 ❈ |_____|__|__|_____|________|____||__||___._||__||__|__|__|  ❈
 ❅                                                             ❅
 ❆ ❆ ❈ ❇ ❊ ❅ ❉ ❆ ❈ ❇ ❊ ❅ ❉ ❆ ❈ ❇ ❊ ❅ ❉ ❆ ❈ ❇ ❊ ❅ ❉ ❆ ❈ ❇ ❊ ❅ ❉ ❆

                      "ice to meet you"
```

Simple scripts to claim and restake vested tokens from [SnowbankDAO](https://dapp.snowbank.finance/#/mints)

Since Snowbank is a fork of [OlympusDAO](https://www.olympusdao.finance/), it would be simple to adapt this for your fork of choice too

## Setup

```sh
yarn install
```

Setup the `.env` file:

```sh
cp .env.sample .env
```

Edit .env and put in your own values for:

- WALLET_ADDRESS – the wallet that actually owns the SB tokens and is earning the rewards
- PRIVATE_KEY - for a wallet that will execute the `bond()` call on the Snowbank contract. Make sure this wallet has some AVAX


## Usage

Get some info about your bond (`bondInfo()`):

```sh
yarn stats
```

Claim your rewards (`redeem()`):

```sh
yarn redeem
```

To run that every 8 hours, you could use cron, systemd or just a lazy bash loop:

```sh
while [ true ]; do
  yarn redeem
  sleep $((60*60*8))
done
```

Or just run it yourself, I don't care

## License

MIT

Pull requests & bug reports welcome

Please direct donations to the [Center For Artistic Activism](https://c4aa.org/) and [Electronic Frontier Foundation](https://www.eff.org/)


## Thanks

Shoutout to the OUE CREW for hot tips

Shoutout to [avalanche-smart-contract-quickstart](https://github.com/ava-labs/avalanche-smart-contract-quickstart), on which this repo is based

Shoutout to my kids, love y'all

Shoutout to you, for reading this

![Speed project approved: 1 hour](http://www.fffff.at/widgets/speed-project/images/time_60.png)
