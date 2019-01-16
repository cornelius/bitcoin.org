{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/listunspent.md" %}

##### ListUnspent
{% include helpers/subhead-links.md %}

{% assign summary_listUnspent="returns array of unspent transaction outputs
with between minconf and maxconf (inclusive) confirmations." %}

{% autocrossref %}

The `listunspent` RPC {{summary_listUnspent}}

Optionally filter to only include txouts paid to specified addresses.

*Parameter #1---minconf*

{% itemplate ntpd1 %}
- n: "minconf"
  t: "number (int)"
  p: "Optional<br>Default=1"
  d: "The minimum confirmations to filter"

{% enditemplate %}

*Parameter #2---maxconf*

{% itemplate ntpd1 %}
- n: "maxconf"
  t: "number (int)"
  p: "Optional<br>Default=9999999"
  d: "The maximum confirmations to filter"

{% enditemplate %}

*Parameter #3---addresses*

{% itemplate ntpd1 %}
- n: "addresses"
  t: "string"
  p: "Required"
  d: "A json array of bitcoin addresses to filter"

{% enditemplate %}

{% endautocrossref %}

    [
      "address"     (string) bitcoin address
      ,...
    ]

{% autocrossref %}

*Parameter #4---include_unsafe*

{% itemplate ntpd1 %}
- n: "include_unsafe"
  t: "bool"
  p: "Optional<br>Default=true"
  d: "Include outputs that are not safe to spend
       See description of \"safe\" attribute below."

{% enditemplate %}

*Parameter #5---query_options*

{% itemplate ntpd1 %}
- n: "query_options"
  t: "json"
  p: "Optional"
  d: "JSON with query options"

{% enditemplate %}

{% endautocrossref %}

    {
      "minimumAmount"    (numeric or string, default=0) Minimum value of each UTXO in BTC
      "maximumAmount"    (numeric or string, default=unlimited) Maximum value of each UTXO in BTC
      "maximumCount"     (numeric or string, default=unlimited) Maximum number of UTXOs
      "minimumSumAmount" (numeric or string, default=unlimited) Minimum sum value of all UTXOs in BTC
    }

{% autocrossref %}

*Result*

{% endautocrossref %}

    [                   (array of json object)
      {
        "txid" : "txid",          (string) the transaction id
        "vout" : n,               (numeric) the vout value
        "address" : "address",    (string) the bitcoin address
        "label" : "label",        (string) The associated label, or "" for the default label
        "account" : "account",    (string) DEPRECATED. This field will be removed in V0.18. To see this deprecated field, start bitcoind with -deprecatedrpc=accounts. The associated account, or "" for the default account
        "scriptPubKey" : "key",   (string) the script key
        "amount" : x.xxx,         (numeric) the transaction output amount in BTC
        "confirmations" : n,      (numeric) The number of confirmations
        "redeemScript" : n        (string) The redeemScript if scriptPubKey is P2SH
        "spendable" : xxx,        (bool) Whether we have the private keys to spend this output
        "solvable" : xxx,         (bool) Whether we know how to spend this output, ignoring the lack of keys
        "safe" : xxx              (bool) Whether this output is considered safe to spend. Unconfirmed transactions
                                  from outside keys and unconfirmed replacement transactions are considered unsafe
                                  and are not eligible for spending by fundrawtransaction and sendtoaddress.
      }
      ,...
    ]

{% autocrossref %}

*Example*

{% highlight bash %}
bitcoin-cli listunspent
{% endhighlight %}
{% highlight bash %}
bitcoin-cli listunspent 6 9999999 "[\"1PGFqEzfmQch1gKD3ra4k18PNj3tTUUSqg\",\"1LtvqCaApEdUGFkpKMM4MstjcaL4dKg8SP\"]"
{% endhighlight %}
{% highlight bash %}
bitcoin-cli listunspent 6 9999999 '[]' true '{ "minimumAmount": 0.005 }'
{% endhighlight %}

*See also*

* [ListTransactions][rpc listtransactions]: {{summary_listTransactions}}
* [LockUnspent][rpc lockunspent]: {{summary_lockUnspent}}

{% endautocrossref %}
