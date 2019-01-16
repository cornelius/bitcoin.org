{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/createpsbt.md" %}

##### CreatePsbt
{% include helpers/subhead-links.md %}

{% assign summary_createPsbt="creates a transaction in the Partially Signed Transaction format." %}

{% autocrossref %}

The `createpsbt` RPC {{summary_createPsbt}}

Implements the Creator role.

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
  d: "Raw locktime. Non-0 value also locktime-activates inputs"

{% enditemplate %}

*Parameter #4---replaceable*

{% itemplate ntpd1 %}
- n: "replaceable"
  t: "boolean"
  p: "Optional<br>Default=false"
  d: "Marks this transaction as BIP125 replaceable.
       Allows this transaction to be replaced by a transaction with higher fees. If provided, it is an error if explicit sequence numbers are incompatible."

{% enditemplate %}

*Result---`null` on success*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null` when the command was successfull or a JSON with an error field on error."

{% enditemplate %}

*Example*

{% highlight bash %}
bitcoin-cli createpsbt "[{\"txid\":\"myid\",\"vout\":0}]" "[{\"data\":\"00010203\"}]"
{% endhighlight %}

*See also*

{% endautocrossref %}
