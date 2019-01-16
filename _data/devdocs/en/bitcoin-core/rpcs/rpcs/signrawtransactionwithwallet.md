{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/signrawtransactionwithwallet.md" %}

##### SignRawTransactionWithWallet
{% include helpers/subhead-links.md %}

{% assign summary_signRawTransactionWithWallet="sign inputs for raw transaction (serialized, hex-encoded)." %}

{% autocrossref %}

The `signrawtransactionwithwallet` RPC {{summary_signRawTransactionWithWallet}}

The second optional argument (may be null) is an array of previous transaction outputs that
this transaction depends on but may not yet be in the block chain.

*Parameter #1---hexstring*

{% itemplate ntpd1 %}
- n: "hexstring"
  t: "string"
  p: "Required<br>(exactly 1)"
  d: "The transaction hex string"

{% enditemplate %}

*Parameter #2---prevtxs*

{% itemplate ntpd1 %}
- n: "prevtxs"
  t: "string"
  p: "Optional"
  d: "An json array of previous dependent transaction outputs"

{% enditemplate %}

{% endautocrossref %}

     [                              (json array of json objects, or 'null' if none provided)
       {
         "txid":"id",               (string, required) The transaction id
         "vout":n,                  (numeric, required) The output number
         "scriptPubKey": "hex",     (string, required) script key
         "redeemScript": "hex",     (string, required for P2SH or P2WSH) redeem script
         "amount": value            (numeric, required) The amount spent
       }
       ,...
    ]

{% autocrossref %}

*Parameter #3---sighashtype*

{% itemplate ntpd1 %}
- n: "sighashtype"
  t: "string"
  p: "Optional<br>Default=ALL"
  d: "The signature hash type. Must be one of
       \"ALL\"
       \"NONE\"
       \"SINGLE\"
       \"ALL|ANYONECANPAY\"
       \"NONE|ANYONECANPAY\"
       \"SINGLE|ANYONECANPAY\""

{% enditemplate %}

*Result*

{% endautocrossref %}

    {
      "hex" : "value",                  (string) The hex-encoded raw transaction with signature(s)
      "complete" : true|false,          (boolean) If the transaction has a complete set of signatures
      "errors" : [                      (json array of objects) Script verification errors (if there are any)
        {
          "txid" : "hash",              (string) The hash of the referenced, previous transaction
          "vout" : n,                   (numeric) The index of the output to spent and used as input
          "scriptSig" : "hex",          (string) The hex-encoded signature script
          "sequence" : n,               (numeric) Script sequence number
          "error" : "text"              (string) Verification or signing error related to the input
        }
        ,...
      ]
    }

{% autocrossref %}

*Example*

{% highlight bash %}
bitcoin-cli signrawtransactionwithwallet "myhex"
{% endhighlight %}

*See also*

{% endautocrossref %}
