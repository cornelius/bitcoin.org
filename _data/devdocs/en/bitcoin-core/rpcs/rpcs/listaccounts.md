{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/listaccounts.md" %}

##### ListAccounts
{% include helpers/subhead-links.md %}

{% assign summary_listAccounts="does ListAccounts." %}

{% autocrossref %}

The `listaccounts` RPC {{summary_listAccounts}}

*Parameters: none*

*Result---`null` on success*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null` when the command was successfull or a JSON with an error field on error."

{% enditemplate %}

*See also*

* [GetAccount][rpc getaccount]: {{summary_getAccount}}
* [GetAddressesByAccount][rpc getaddressesbyaccount]: {{summary_getAddressesByAccount}}
* [ListReceivedByAccount][rpc listreceivedbyaccount]: {{summary_listReceivedByAccount}}

{% endautocrossref %}
