# FVAMPay exit page

A single web page that lets an FVAMPay customer move all their money out of their account with their **recovery key**
alone: no fvampay.com, no FVAMPay servers. It runs in any browser, from this address or from a copy saved on your own
computer.

**Open it:** https://fvampay.github.io/exit/

**Save a copy:** download [fvampay-exit.html](fvampay-exit.html) and keep it somewhere you'll find it. It works offline.

## Check your copy is the real one

The page's SHA-256 fingerprint is:

```
1431bf0e8ae582cff2a0649b80ee79cb56fa2446ca3459bd58ba68b12d56b4a7
```

On a Mac or Linux: `shasum -a 256 fvampay-exit.html`. On Windows: `certutil -hashfile fvampay-exit.html SHA256`.
The result must match exactly. If it doesn't, don't use that copy.

## Networks

This version covers **Base Sepolia**, the test network. The Base version is published here when FVAMPay goes live
on Base, with its own fingerprint.

## What it does

It reads your account's recovery state from the chain, and once your recovery key's waiting period (7 days) is over,
it moves your money to the wallet you chose, signed by your recovery key. Your passkey can cancel a recovery at any
time during those 7 days. The page loads nothing from anywhere else and talks only to the network address (RPC) you
choose.
