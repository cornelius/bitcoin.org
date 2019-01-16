{% comment %}
This file is licensed under the MIT License (MIT) available on
http://opensource.org/licenses/MIT.
{% endcomment %}
{% assign filename="_data/devdocs/en/bitcoin-core/rpcs/quick-reference.md" %}

#### Quick Reference {#rpc-quick-reference}
{% include helpers/subhead-links.md %}

{% comment %}
Styling notes: use highly-visible style for upcoming changes (not yet
released) and changes made in the last 6 months.  Use less-visible
style for changes made up to two years ago.  Don't point out
changes made more than two years ago.

Use v0.n.n in abbreviation title to prevent autocrossrefing.
{% endcomment %}

<!-- Deprecated -->
{% assign DEPRECATED='**<abbr title="Deprecated; will be removed in a future version of Bitcoin Core">Deprecated</abbr>**' %}
<!-- Bitcoin Core 0.14.1 April 2017 -->
{% assign UPDATED0_14_1='**<abbr title="Updated in Bitcoin Core v0.14.1">Updated in 0.14.1</abbr>**' %}

<!-- Bitcoin Core 0.14.0 March 2017 -->
{% assign NEW0_14_0='**<abbr title="New in Bitcoin Core v0.14.0">New in 0.14.0</abbr>**' %}
{% assign UPDATED0_14_0='**<abbr title="Updated in Bitcoin Core v0.14.0">Updated in 0.14.0</abbr>**' %}

<!-- Bitcoin Core 0.13.1 September 2016 -->
{% assign UPDATED0_13_1='*<abbr title="Updated in Bitcoin Core v0.13.1">Updated in 0.13.1</abbr>*' %}

<!-- Bitcoin Core 0.13.0 August 2016 -->
{% assign NEW0_13_0='*<abbr title="New in Bitcoin Core v0.13.0">New in 0.13.0</abbr>*' %}
{% assign UPDATED0_13_0='*<abbr title="Updated in Bitcoin Core v0.13.0">Updated in 0.13.0</abbr>*' %}

<!-- Bitcoin Core 0.12.1 April 2016 -->
{% assign UPDATED0_12_1='*<abbr title="Updated in Bitcoin Core v0.12.1">Updated in 0.12.1</abbr>*' %}

<!-- Bitcoin Core 0.12.0 February 2016 -->
{% assign NEW0_12_0='*<abbr title="New in Bitcoin Core v0.12.0">New in 0.12.0</abbr>*' %}
{% assign UPDATED0_12_0='*<abbr title="Updated in Bitcoin Core v0.12.0">Updated in 0.12.0</abbr>*' %}

<!-- Bitcoin Core 0.11.0 July 2015 -->
{% assign NEW0_11_0='*<abbr title="New in Bitcoin Core v0.11.0">New in 0.11.0</abbr>*' %}

<!-- the summaries used below are defined in the files for the
     particular RPC and aggregated into this helper file by the makefile
     function manual-update-summaries-file. For example, to edit the
     summary for GetBestBlockHash, edit
     _includes/rpc/getbestblockhash.md and run `make manual-update-summaries`. -->
{% include helpers/summaries.md %}

#### Blockchain RPCs
{:.no_toc}
<!-- no subhead-links here -->

{% autocrossref %}

* [GetBestBlockHash][rpc getbestblockhash]: {{summary_getBestBlockHash}}
* [GetBlock][rpc getblock]: {{summary_getBlock}} {{UPDATED0_13_0}}
* [GetBlockChainInfo][rpc getblockchaininfo]: {{summary_getBlockChainInfo}} {{UPDATED0_12_1}}
* [GetBlockCount][rpc getblockcount]: {{summary_getBlockCount}}
* [GetBlockHash][rpc getblockhash]: {{summary_getBlockHash}}
* [GetBlockHeader][rpc getblockheader]: {{summary_getBlockHeader}} {{NEW0_12_0}}
* [GetBlockStats][rpc getblockstats]: {{summary_getBlockStats}}
* [GetChainTips][rpc getchaintips]: {{summary_getChainTips}}
* [GetChainTxStats][rpc getchaintxstats]: {{summary_getChainTxStats}}
* [GetDifficulty][rpc getdifficulty]: {{summary_getDifficulty}}
* [GetMemPoolAncestors][rpc getmempoolancestors]: {{summary_getMemPoolAncestors}} {{NEW0_13_0}}
* [GetMemPoolDescendants][rpc getmempooldescendants]: {{summary_getMemPoolDescendants}} {{NEW0_13_0}}
* [GetMemPoolEntry][rpc getmempoolentry]: {{summary_getMemPoolEntry}} {{NEW0_13_0}}
* [GetMemPoolInfo][rpc getmempoolinfo]: {{summary_getMemPoolInfo}} {{UPDATED0_12_0}}
* [GetRawMemPool][rpc getrawmempool]: {{summary_getRawMemPool}} {{UPDATED0_13_0}}
* [GetTxOut][rpc gettxout]: {{summary_getTxOut}}
* [GetTxOutProof][rpc gettxoutproof]: {{summary_getTxOutProof}} {{NEW0_11_0}}
* [GetTxOutSetInfo][rpc gettxoutsetinfo]: {{summary_getTxOutSetInfo}}
* [PreciousBlock][rpc preciousblock]: {{summary_preciousBlock}} {{NEW0_14_0}}
* [PruneBlockChain][rpc pruneblockchain]: {{summary_pruneBlockChain}} {{NEW0_14_0}}
* [SaveMemPool][rpc savemempool]: {{summary_saveMemPool}}
* [ScanTxOutSet][rpc scantxoutset]: {{summary_scanTxOutSet}}
* [VerifyChain][rpc verifychain]: {{summary_verifyChain}}
* [VerifyTxOutProof][rpc verifytxoutproof]: {{summary_verifyTxOutProof}} {{NEW0_11_0}}

{% endautocrossref %}

#### Control RPCs
{:.no_toc}
<!-- no subhead-links here -->

{% autocrossref %}

* [GetMemoryInfo][rpc getmemoryinfo]: {{summary_getMemoryInfo}} {{NEW0_14_0}}
* [Help][rpc help]: {{summary_help}}
* [Logging][rpc logging]: {{summary_logging}}
* [Stop][rpc stop]: {{summary_stop}}
* [Uptime][rpc uptime]: {{summary_uptime}}

{% endautocrossref %}

#### Generating RPCs
{:.no_toc}
<!-- no subhead-links here -->

{% autocrossref %}

* [Generate][rpc generate]: {{summary_generate}} {{NEW0_11_0}}, {{UPDATED0_13_0}}
* [GenerateToAddress][rpc generatetoaddress]: {{summary_generateToAddress}} {{NEW0_13_0}}

{% endautocrossref %}

#### Mining RPCs
{:.no_toc}
<!-- no subhead-links here -->

{% autocrossref %}

* [GetBlockTemplate][rpc getblocktemplate]: {{summary_getBlockTemplate}}
* [GetMiningInfo][rpc getmininginfo]: {{summary_getMiningInfo}} {{UPDATED0_14_0}}
* [GetNetworkHashPs][rpc getnetworkhashps]: {{summary_getNetworkHashPs}}
* [PrioritiseTransaction][rpc prioritisetransaction]: {{summary_prioritiseTransaction}}
* [SubmitBlock][rpc submitblock]: {{summary_submitBlock}}

{% endautocrossref %}

#### Network RPCs
{:.no_toc}
<!-- no subhead-links here -->

{% autocrossref %}

* [AddNode][rpc addnode]: {{summary_addNode}} {{UPDATED0_14_0}}
* [ClearBanned][rpc clearbanned]: {{summary_clearBanned}} {{NEW0_12_0}}
* [DisconnectNode][rpc disconnectnode]: {{summary_disconnectNode}} {{NEW0_12_0}}, {{UPDATED0_14_1}}
* [GetAddedNodeInfo][rpc getaddednodeinfo]: {{summary_getAddedNodeInfo}} {{UPDATED0_14_0}}
* [GetConnectionCount][rpc getconnectioncount]: {{summary_getConnectionCount}}
* [GetNetTotals][rpc getnettotals]: {{summary_getNetTotals}} {{UPDATED0_12_0}}
* [GetNetworkInfo][rpc getnetworkinfo]: {{summary_getNetworkInfo}} {{UPDATED0_13_0}}
* [GetPeerInfo][rpc getpeerinfo]: {{summary_getPeerInfo}} {{UPDATED0_13_0}}
* [ListBanned][rpc listbanned]: {{summary_listBanned}} {{NEW0_12_0}}
* [Ping][rpc ping]: {{summary_ping}}
* [SetBan][rpc setban]: {{summary_setBan}} {{NEW0_12_0}}
* [SetNetworkActive][rpc setnetworkactive]: {{summary_setNetworkActive}} {{NEW0_14_0}}

{% endautocrossref %}

#### Rawtransactions RPCs
{:.no_toc}
<!-- no subhead-links here -->

{% autocrossref %}

* [CombinePsbt][rpc combinepsbt]: {{summary_combinePsbt}}
* [CombineRawTransaction][rpc combinerawtransaction]: {{summary_combineRawTransaction}}
* [ConvertToPsbt][rpc converttopsbt]: {{summary_convertToPsbt}}
* [CreatePsbt][rpc createpsbt]: {{summary_createPsbt}}
* [CreateRawTransaction][rpc createrawtransaction]: {{summary_createRawTransaction}} {{UPDATED0_14_1}}
* [DecodePsbt][rpc decodepsbt]: {{summary_decodePsbt}}
* [DecodeRawTransaction][rpc decoderawtransaction]: {{summary_decodeRawTransaction}} {{UPDATED0_13_0}}
* [DecodeScript][rpc decodescript]: {{summary_decodeScript}}
* [FinalizePsbt][rpc finalizepsbt]: {{summary_finalizePsbt}}
* [FundRawTransaction][rpc fundrawtransaction]: {{summary_fundRawTransaction}} {{NEW0_12_0}}, {{UPDATED0_14_0}}
* [GetRawTransaction][rpc getrawtransaction]: {{summary_getRawTransaction}} {{UPDATED0_14_0}}
* [SendRawTransaction][rpc sendrawtransaction]: {{summary_sendRawTransaction}}
* [SignRawTransaction][rpc signrawtransaction]: {{summary_signRawTransaction}}
* [SignRawTransactionWithKey][rpc signrawtransactionwithkey]: {{summary_signRawTransactionWithKey}}
* [TestmemPoolAccept][rpc testmempoolaccept]: {{summary_testmemPoolAccept}}

{% endautocrossref %}

#### Util RPCs
{:.no_toc}
<!-- no subhead-links here -->

{% autocrossref %}

* [CreateMultiSig][rpc createmultisig]: {{summary_createMultiSig}}
* [EstimateSmartFee][rpc estimatesmartfee]: {{summary_estimateSmartFee}}
* [SignMessageWithPrivKey][rpc signmessagewithprivkey]: {{summary_signMessageWithPrivKey}} {{NEW0_13_0}}
* [ValidateAddress][rpc validateaddress]: {{summary_validateAddress}} {{UPDATED0_13_0}}
* [VerifyMessage][rpc verifymessage]: {{summary_verifyMessage}}

{% endautocrossref %}

#### Wallet RPCs
{:.no_toc}
<!-- no subhead-links here -->

{% autocrossref %}

**Note:** the wallet RPCs are only available if Bitcoin Core was built
with [wallet support][]{:#term-wallet-support}{:.term}, which is the
default.

* [AbandonTransaction][rpc abandontransaction]: {{summary_abandonTransaction}} {{NEW0_12_0}}
* [AbortRescan][rpc abortrescan]: {{summary_abortRescan}}
* [AddMultiSigAddress][rpc addmultisigaddress]: {{summary_addMultiSigAddress}}
* [BackupWallet][rpc backupwallet]: {{summary_backupWallet}}
* [BumpFee][rpc bumpfee]: {{summary_bumpFee}} {{NEW0_14_0}}
* [CreateWallet][rpc createwallet]: {{summary_createWallet}}
* [DumpPrivKey][rpc dumpprivkey]: {{summary_dumpPrivKey}}
* [DumpWallet][rpc dumpwallet]: {{summary_dumpWallet}}
* [EncryptWallet][rpc encryptwallet]: {{summary_encryptWallet}}
* [GetAccount][rpc getaccount]: {{summary_getAccount}}
* [GetAccountAddress][rpc getaccountaddress]: {{summary_getAccountAddress}} {{DEPRECATED}}
* [GetAddressByAccount][rpc getaddressbyaccount]: {{summary_getAddressByAccount}} {{DEPRECATED}}
* [GetAddressesByLabel][rpc getaddressesbylabel]: {{summary_getAddressesByLabel}}
* [GetAddressInfo][rpc getaddressinfo]: {{summary_getAddressInfo}}
* [GetBalance][rpc getbalance]: {{summary_getBalance}}
* [GetNewAddress][rpc getnewaddress]: {{summary_getNewAddress}}
* [GetRawChangeAddress][rpc getrawchangeaddress]: {{summary_getRawChangeAddress}}
* [GetReceivedByAccount][rpc getreceivedbyaccount]: {{summary_getReceivedByAccount}} {{DEPRECATED}}
* [GetReceivedByAddress][rpc getreceivedbyaddress]: {{summary_getReceivedByAddress}}
* [GetTransaction][rpc gettransaction]: {{summary_getTransaction}} {{UPDATED0_12_0}}
* [GetUnconfirmedBalance][rpc getunconfirmedbalance]: {{summary_getUnconfirmedBalance}}
* [GetWalletInfo][rpc getwalletinfo]: {{summary_getWalletInfo}}
* [ImportAddress][rpc importaddress]: {{summary_importAddress}}
* [ImportMulti][rpc importmulti]: {{summary_importMulti}} {{NEW0_14_0}}
* [ImportPrivKey][rpc importprivkey]: {{summary_importPrivKey}}
* [ImportPrunedFunds][rpc importprunedfunds]: {{summary_importPrunedFunds}} {{NEW0_13_0}}
* [ImportPubKey][rpc importpubkey]: {{summary_importPubKey}}
* [ImportWallet][rpc importwallet]: {{summary_importWallet}}
* [KeyPoolRefill][rpc keypoolrefill]: {{summary_keyPoolRefill}}
* [ListAccounts][rpc listaccounts]: {{summary_listAccounts}} {{DEPRECATED}}
* [ListAddressGroupings][rpc listaddressgroupings]: {{summary_listAddressGroupings}}
* [ListLabels][rpc listlabels]: {{summary_listLabels}}
* [ListLockUnspent][rpc listlockunspent]: {{summary_listLockUnspent}}
* [ListReceivedByAccount][rpc listreceivedbyaccount]: {{summary_listReceivedByAccount}} {{DEPRECATED}}
* [ListReceivedByAddress][rpc listreceivedbyaddress]: {{summary_listReceivedByAddress}}
* [ListSinceBlock][rpc listsinceblock]: {{summary_listSinceBlock}}
* [ListTransactions][rpc listtransactions]: {{summary_listTransactions}} {{UPDATED0_12_1}}
* [ListUnspent][rpc listunspent]: {{summary_listUnspent}} {{UPDATED0_13_0}}
* [ListWallets][rpc listwallets]: {{summary_listWallets}}
* [LoadWallet][rpc loadwallet]: {{summary_loadWallet}}
* [LockUnspent][rpc lockunspent]: {{summary_lockUnspent}}
* [Move][rpc move]: {{summary_move}} {{DEPRECATED}}
* [RemovePrunedFunds][rpc removeprunedfunds]: {{summary_removePrunedFunds}} {{NEW0_13_0}}
* [RescanBlockChain][rpc rescanblockchain]: {{summary_rescanBlockChain}}
* [SendFrom][rpc sendfrom]: {{summary_sendFrom}} {{DEPRECATED}}
* [SendMany][rpc sendmany]: {{summary_sendMany}}
* [SendToAddress][rpc sendtoaddress]: {{summary_sendToAddress}}
* [SetAccount][rpc setaccount]: {{summary_setAccount}} {{DEPRECATED}}
* [SetHdSeed][rpc sethdseed]: {{summary_setHdSeed}}
* [SetTxFee][rpc settxfee]: {{summary_setTxFee}}
* [SignMessage][rpc signmessage]: {{summary_signMessage}}
* [SignRawTransactionWithWallet][rpc signrawtransactionwithwallet]: {{summary_signRawTransactionWithWallet}}
* [UnloadWallet][rpc unloadwallet]: {{summary_unloadWallet}}
* [WalletCreatefundedPsbt][rpc walletcreatefundedpsbt]: {{summary_walletCreatefundedPsbt}}
* [WalletLock][rpc walletlock]: {{summary_walletLock}}
* [WalletPassphrase][rpc walletpassphrase]: {{summary_walletPassphrase}}
* [WalletPassphraseChange][rpc walletpassphrasechange]: {{summary_walletPassphraseChange}}
* [WalletProcessPsbt][rpc walletprocesspsbt]: {{summary_walletProcessPsbt}}

{% endautocrossref %}

