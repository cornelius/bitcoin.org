{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/getaccount.md" %}

##### GetAccount
{% include helpers/subhead-links.md %}

{% assign summary_getAccount="does GetAccount." %}

{% autocrossref %}

The `getaccount` RPC {{summary_getAccount}}

*Parameters: none*

*Result---`null` on success*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null` when the command was successfull or a JSON with an error field on error."

{% enditemplate %}

*See also*

* [GetAddressesByAccount][rpc getaddressesbyaccount]: {{summary_getAddressesByAccount}}

{% endautocrossref %}
