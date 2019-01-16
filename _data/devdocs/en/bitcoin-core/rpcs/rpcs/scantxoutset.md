{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/scantxoutset.md" %}

##### ScanTxOutSet
{% include helpers/subhead-links.md %}

{% assign summary_scanTxOutSet="eXPERIMENTAL warning: this call may be removed or changed in future releases." %}

{% autocrossref %}

The `scantxoutset` RPC {{summary_scanTxOutSet}}

Scans the unspent transaction output set for entries that match certain output descriptors.

*Parameters: none*

*Result---`null` on success*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null` when the command was successfull or a JSON with an error field on error."

{% enditemplate %}

*Example*

    addr(<address>)                      Outputs whose scriptPubKey corresponds to the specified address (does not include P2PK)

    raw(<hex script>)                    Outputs whose scriptPubKey equals the specified hex scripts

    combo(<pubkey>)                      P2PK, P2PKH, P2WPKH, and P2SH-P2WPKH outputs for the given pubkey

    pkh(<pubkey>)                        P2PKH outputs for the given pubkey

    sh(multi(<n>,<pubkey>,<pubkey>,...)) P2SH-multisig outputs for the given threshold and pubkeys

In the above, <pubkey> either refers to a fixed public key in hexadecimal notation, or to an xpub/xprv optionally followed by one

or more path elements separated by "/", and optionally ending in "/*" (unhardened), or "/*'" or "/*h" (hardened) to specify all

unhardened or hardened child keys.

In the latter case, a range needs to be specified by below if different from 1000.

For more information on output descriptors, see the documentation in the doc/descriptors.md file.

Arguments:

1. "action"                       (string, required) The action to execute

                                      "start" for starting a scan

                                      "abort" for aborting the current scan (returns true when abort was successful)

                                      "status" for progress report (in %) of the current scan

2. "scanobjects"                  (array, required) Array of scan objects

    [                             Every scan object is either a string descriptor or an object:

        "descriptor",             (string, optional) An output descriptor

        {                         (object, optional) An object with output descriptor and metadata

          "desc": "descriptor",   (string, required) An output descriptor

          "range": n,             (numeric, optional) Up to what child index HD chains should be explored (default: 1000)

        },

        ...

    ]

Result:

{

  "unspents": [

    {

    "txid" : "transactionid",     (string) The transaction id

    "vout": n,                    (numeric) the vout value

    "scriptPubKey" : "script",    (string) the script key

    "amount" : x.xxx,             (numeric) The total amount in BTC of the unspent output

    "height" : n,                 (numeric) Height of the unspent transaction output

   }

   ,...], 

 "total_amount" : x.xxx,          (numeric) The total amount of all found unspent outputs in BTC

]


*See also*

{% endautocrossref %}
