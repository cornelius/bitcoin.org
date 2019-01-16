{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/getaccountaddress.md" %}

##### GetAccountAddress
{% include helpers/subhead-links.md %}

{% assign summary_getAccountAddress="does GetAccountAddress." %}

{% autocrossref %}

The `getaccountaddress` RPC {{summary_getAccountAddress}}

*Parameters: none*

*Result---`null` on success*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null` when the command was successfull or a JSON with an error field on error."

{% enditemplate %}

*See also*

* [GetNewAddress][rpc getnewaddress]: {{summary_getNewAddress}}
* [GetRawChangeAddress][rpc getrawchangeaddress]: {{summary_getRawChangeAddress}}
* [GetAddressesByAccount][rpc getaddressesbyaccount]: {{summary_getAddressesByAccount}}

{% endautocrossref %}
