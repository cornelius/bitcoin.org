{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/move.md" %}

##### Move
{% include helpers/subhead-links.md %}

{% assign summary_move="does Move." %}

{% autocrossref %}

The `move` RPC {{summary_move}}

*Parameters: none*

*Result---`null` on success*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null` when the command was successfull or a JSON with an error field on error."

{% enditemplate %}

*See also*

* [ListAccounts][rpc listaccounts]: {{summary_listAccounts}}
* [SendFrom][rpc sendfrom]: {{summary_sendFrom}}
* [SendToAddress][rpc sendtoaddress]: {{summary_sendToAddress}}

{% endautocrossref %}
