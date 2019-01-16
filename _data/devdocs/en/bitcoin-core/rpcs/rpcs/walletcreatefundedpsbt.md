{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/walletcreatefundedpsbt.md" %}

##### WalletCreatefundedPsbt
{% include helpers/subhead-links.md %}

{% assign summary_walletCreatefundedPsbt="creates and funds a transaction in the Partially Signed Transaction format." %}

{% autocrossref %}

The `walletcreatefundedpsbt` RPC {{summary_walletCreatefundedPsbt}}

Inputs will be added if supplied inputs are not enough
Implements the Creator and Updater roles.

*Parameter #1---inputs*

{% itemplate ntpd1 %}
- n: "inputs"
  t: "array"
  p: "Required<br>(exactly 1)"
  d: "A json array of json objects"

{% enditemplate %}

{% endautocrossref %}

    [
      {
        "txid":"id",      (string, required) The transaction id
        "vout":n,         (numeric, required) The output number
        "sequence":n      (numeric, optional) The sequence number
      } 
      ,...
    ]

{% autocrossref %}

*Parameter #2---outputs*

{% itemplate ntpd1 %}
- n: "outputs"
  t: "array"
  p: "Required<br>(exactly 1)"
  d: "a json array with outputs (key-value pairs), where none of the keys are duplicated."

{% enditemplate %}

{% endautocrossref %}

    [
     {
       "address": x.xxx,    (obj, optional) A key-value pair. The key (string) is the bitcoin address, the value (float or string) is the amount in BTC
     },
     {
       "data": "hex"        (obj, optional) A key-value pair. The key must be "data", the value is hex encoded data
     }
     ,...                     More key-value pairs of the above form. For compatibility reasons, a dictionary, which holds the key-value pairs directly, is also
                              accepted as second parameter.
    ]

{% autocrossref %}

*Parameter #3---locktime*

{% itemplate ntpd1 %}
- n: "locktime"
  t: "number (int)"
  p: "Optional<br>Default=0"
  d: "Raw locktime. Non-0 value also locktime-activates inputs
       Allows this transaction to be replaced by a transaction with higher fees. If provided, it is an error if explicit sequence numbers are incompatible."

{% enditemplate %}

*Parameter #4---options*

{% itemplate ntpd1 %}
- n: "options"
  t: "object"
  p: "Optional"
  d: ""

{% enditemplate %}

{% endautocrossref %}

    {
      "changeAddress"          (string, optional, default pool address) The bitcoin address to receive the change
      "changePosition"         (numeric, optional, default random) The index of the change output
      "change_type"            (string, optional) The output type to use. Only valid if changeAddress is not specified. Options are "legacy", "p2sh-segwit", and "bech32". Default is set by -changetype.
      "includeWatching"        (boolean, optional, default false) Also select inputs which are watch only
      "lockUnspents"           (boolean, optional, default false) Lock selected unspent outputs
      "feeRate"                (numeric, optional, default not set: makes wallet determine the fee) Set a specific fee rate in BTC/kB
      "subtractFeeFromOutputs" (array, optional) A json array of integers.
                               The fee will be equally deducted from the amount of each specified output.
                               The outputs are specified by their zero-based index, before any change output is added.
                               Those recipients will receive less bitcoins than you enter in their corresponding amount field.
                               If no outputs are specified here, the sender pays the fee.
                                   [vout_index,...]
      "replaceable"            (boolean, optional) Marks this transaction as BIP125 replaceable.
                               Allows this transaction to be replaced by a transaction with higher fees
      "conf_target"            (numeric, optional) Confirmation target (in blocks)
      "estimate_mode"          (string, optional, default=UNSET) The fee estimate mode, must be one of:
          "UNSET"
          "ECONOMICAL"
          "CONSERVATIVE"
    }

{% autocrossref %}

*Parameter #5---bip32derivs*

{% itemplate ntpd1 %}
- n: "bip32derivs"
  t: "boolean"
  p: "Optional<br>Default=false"
  d: "If true, includes the BIP 32 derivation paths for public keys if we know them"

{% enditemplate %}

*Result*

{% endautocrossref %}

    {
      "psbt": "value",        (string)  The resulting raw transaction (base64-encoded string)
      "fee":       n,         (numeric) Fee in BTC the resulting transaction pays
      "changepos": n          (numeric) The position of the added change output, or -1
    }

{% autocrossref %}

*Example*

Create a transaction with no inputs

{% highlight bash %}
bitcoin-cli walletcreatefundedpsbt "[{\"txid\":\"myid\",\"vout\":0}]" "[{\"data\":\"00010203\"}]"
{% endhighlight %}

*See also*

{% endautocrossref %}
