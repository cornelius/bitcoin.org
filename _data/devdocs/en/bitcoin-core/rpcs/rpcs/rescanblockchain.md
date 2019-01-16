{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/rescanblockchain.md" %}

##### RescanBlockChain
{% include helpers/subhead-links.md %}

{% assign summary_rescanBlockChain="rescan the local blockchain for wallet related transactions." %}

{% autocrossref %}

The `rescanblockchain` RPC {{summary_rescanBlockChain}}

*Parameter #1---start_height*

{% itemplate ntpd1 %}
- n: "start_height"
  t: "number (int)"
  p: "Optional"
  d: "block height where the rescan should start"

{% enditemplate %}

*Parameter #2---stop_height*

{% itemplate ntpd1 %}
- n: "stop_height"
  t: "number (int)"
  p: "Optional"
  d: "the last block height that should be scanned"

{% enditemplate %}

*Result*

{% endautocrossref %}

    {
      "start_height"     (numeric) The block height where the rescan has started. If omitted, rescan started from the genesis block.
      "stop_height"      (numeric) The height of the last rescanned block. If omitted, rescan stopped at the chain tip.
    }

{% autocrossref %}

*Example*

{% highlight bash %}
bitcoin-cli rescanblockchain 100000 120000
{% endhighlight %}

*See also*

{% endautocrossref %}
