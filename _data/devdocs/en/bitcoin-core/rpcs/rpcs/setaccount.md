{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/setaccount.md" %}

##### SetAccount
{% include helpers/subhead-links.md %}

{% assign summary_setAccount="does SetAccount." %}

{% autocrossref %}

The `setaccount` RPC {{summary_setAccount}}

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
* [ListAccounts][rpc listaccounts]: {{summary_listAccounts}}
* [GetAddressesByAccount][rpc getaddressesbyaccount]: {{summary_getAddressesByAccount}}

{% endautocrossref %}
