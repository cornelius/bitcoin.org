{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/rpcs/sendfrom.md" %}

##### SendFrom
{% include helpers/subhead-links.md %}

{% assign summary_sendFrom="does SendFrom." %}

{% autocrossref %}

The `sendfrom` RPC {{summary_sendFrom}}

*Parameters: none*

*Result---`null` on success*

{% itemplate ntpd1 %}
- n: "`result`"
  t: "null"
  p: "Required<br>(exactly 1)"
  d: "JSON `null` when the command was successfull or a JSON with an error field on error."

{% enditemplate %}

*See also*

* [SendToAddress][rpc sendtoaddress]: {{summary_sendToAddress}}
* [SendMany][rpc sendmany]: {{summary_sendMany}}

{% endautocrossref %}
