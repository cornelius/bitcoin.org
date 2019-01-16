{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/listreceivedbyaccount.md" %}

##### ListReceivedByAccount
{% include helpers/subhead-links.md %}

{% assign summary_listReceivedByAccount="does ListReceivedByAccount." %}

{% autocrossref %}

The `listreceivedbyaccount` RPC {{summary_listReceivedByAccount}}

*Parameters: none*

*Result---`null` on success*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null` when the command was successfull or a JSON with an error field on error."

{% enditemplate %}

*See also*

* [ListReceivedByAddress][rpc listreceivedbyaddress]: {{summary_listReceivedByAddress}}
* [GetReceivedByAccount][rpc getreceivedbyaccount]: {{summary_getReceivedByAccount}}
* [GetReceivedByAddress][rpc getreceivedbyaddress]: {{summary_getReceivedByAddress}}

{% endautocrossref %}
