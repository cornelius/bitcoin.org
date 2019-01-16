{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/getreceivedbyaccount.md" %}

##### GetReceivedByAccount
{% include helpers/subhead-links.md %}

{% assign summary_getReceivedByAccount="does GetReceivedByAccount." %}

{% autocrossref %}

The `getreceivedbyaccount` RPC {{summary_getReceivedByAccount}}

*Parameters: none*

*Result---`null` on success*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null` when the command was successfull or a JSON with an error field on error."

{% enditemplate %}

*See also*

* [GetReceivedByAddress][rpc getreceivedbyaddress]: {{summary_getReceivedByAddress}}
* [GetAddressesByAccount][rpc getaddressesbyaccount]: {{summary_getAddressesByAccount}}
* [ListAccounts][rpc listaccounts]: {{summary_listAccounts}}

{% endautocrossref %}
