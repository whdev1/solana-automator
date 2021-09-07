# Solana Automator

This is a command-line wrapper for the [Solana CLI](https://docs.solana.com/cli) that allows for the automated distribution of [SPL tokens](https://spl.solana.com/token) to any number of Solana wallets.

The source is presented in both Python and Node.js, with both versions of the program providing identical functionality.

**PLEASE NOTE: Both versions of this program are provided freely without any warranties and no guarantee of fitness for a particular purpose. Solana transactions are final, so ensure that the wallet and token addresses as well as the amounts to transfer are correct. Use this utility at your own risk.**

## Setup

First, ensure that you have installed the [Solana CLI](https://docs.solana.com/cli) and installed it in your shell's PATH variable. Then, install either [Node.js](https://nodejs.dev/learn/how-to-install-nodejs) or [Python 3](https://realpython.com/installing-python/) depending on which version of this utility that you want to run.

Once you have done this, run the following commands to clone this repo:
```
git clone https://github.com/whdev1/solana-automator.git
cd solana-automator
```

## Usage

The automator utility expects both a Solana ```keypair.json``` file as well as a CSV containing the tokens and amounts you want to transfer and the recipient wallets. This CSV file is of the format:

| AMOUNT | SPL_TOKEN_ADDRESS | RECIPIENT_WALLET_ADDRESS |
|--------|-------------------|--------------------------|

**Note that the CSV file should contain a header with these three descriptors on its first line.** Once you have your `keypair.json` file and have created your CSV, you may run the utility with either of the following commands.

```
node transfer.js
python transfer.py
```

The utility can also take the two necessary filenames as parameters. Run it with the `-?` switch to see all of the possible options.
