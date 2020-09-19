---
title: 'Bitcoin Optech Newsletter #116'
permalink: /en/newsletters/2020/09/23/
name: 2020-09-23-newsletter
slug: 2020-09-23-newsletter
type: newsletter
layout: newsletter
lang: en
---
This week's newsletter ...

## Action items

## News

## Releases and release candidates

*New releases and release candidates for popular Bitcoin infrastructure
projects.  Please consider upgrading to new releases or helping to test
release candidates.*

## Notable code and documentation changes

*Notable changes this week in [Bitcoin Core][bitcoin core repo],
[C-Lightning][c-lightning repo], [Eclair][eclair repo], [LND][lnd repo],
[Rust-Lightning][rust-lightning repo], [libsecp256k1][libsecp256k1 repo],
[Hardware Wallet Interface (HWI)][hwi], [Bitcoin Improvement Proposals
(BIPs)][bips repo], and [Lightning BOLTs][bolts repo].*

- [Bitcoin Core #16378][] adds a new `send` RPC method to the wallet. This new
  RPC method is designed for maximum flexibility and includes options such as
  multiple outputs (allowing [payment batching][]), [coin selection][topic coin
  selection], manual or automatic feerates, and [PSBT format][topic psbt]. It is
  intended to unify the functionality of the `sendtoaddress` and `sendmany` RPC
  methods, which may be deprecated in a future release. For the full list of
  options see the [RPC help text][send rpc help].

{% include references.md %}
{% include linkers/issues.md issues="16378" %}

[payment batching]: https://github.com/bitcoinops/scaling-book/blob/master/x.payment_batching/payment_batching.md
[send rpc help]: https://github.com/bitcoin/bitcoin/blob/831b0ecea9156447a2b6a67d28858bc26d302c1c/src/wallet/rpcwallet.cpp#L3876-L3933
