# Open Source Polkadot Stack [WIP!] <!-- omit in toc -->

The goal of this page is to provide an overview of the open-source Polkadot/Kusama Tech Stack.

This is a living document and we are relying on our community to contribute to it and help maintain it. [**Please feel free to make edits and additions via pull requests**](#construction_worker-contributing). We apologize if we missed your project!

---

- [:clipboard: About](#clipboard-about)
- [:battery: Funding](#battery-funding)
- [:bookmark_tabs: Layers of Polkadot Stack](#bookmark_tabs-layers-of-polkadot-stack)
  - [:iphone: User Interface](#iphone-user-interface)
  - [:wrench: Tools, APIs and Languages](#wrench-tools-apis-and-languages)
  - [:memo: ink Smart Contracts](#memo-ink-smart-contracts)
  - [:link: Chains and Pallets](#link-chains-and-pallets)
  - [:black_circle: Host](#black_circle-host)
  - [:electric_plug: Network Maintenance Tools](#electric_plug-network-maintenance-tools)
  - [:black_nib: Signatures](#black_nib-signatures)
  - [:heavy_check_mark: Consensus](#heavy_check_mark-consensus)
  - [:satellite: Networking](#satellite-networking)
- [:construction_worker: Contributing](#construction_worker-contributing)

## :clipboard: About

The Polkadot Tech Stack is a subset of the Web 3.0 Tech Stack, which consists of the **open-source** technologies contributing to and relying on [Polkadot](https://polkadot.network/), [Kusama](https://kusama.network/) and [Substrate](https://substrate.dev/). It is meant to be used for decentralized application (Dapp) development within numerous verticals including DeFi, Gaming, Provenance and many others not pictured below.

<!-- markdownlint-disable MD040 -->
```
|------|--------|------------|
| DeFi | Gaming | Provenance |
|______|________|____________|
            Dapps
|--------------------------/-|
| Explorers, Wallets      /  |
|------------------------/---|
| Tools, Apis, Languages/    |
|----------------------/-----|
| 2nd layer protocols /      |
|--------------------/-------|
| Chains            /  other |
|------------------/---    --|
| *Polkadot*      |   tech   |
|------------------\---------|
| P2P, Crypto, Wasm \        |
|--------------------\-------|
```

## :battery: Funding

The Web3 Foundation's [Grants Program](https://github.com/w3f/Grants-Program) is focused on funding development work to build out all layers of the Polkadot Tech Stack. 

To get a better understanding of the projects we consider most relevant, you can explore a detailed breakdown of the various layers of the stack below. We divide each of the layers into the various *components* which we feel are most important. We then highlight some of the *existing projects* that address these components as well as some *potentially interesting projects* that we would like to fund.

We typically like to fund more than one project for each component. So, if you see a component with 1 or 0 existing projects, it's likely that we would consider an application in this area. In order to consider funding a proposal that addresses a component with many existing projects, we would need to be persuaded that yours brings unique value to the ecosystem. Such value could come in many forms including but not limited to differentiated functionality, better user experience, the attraction of new users to the ecosystem or a high likelihood that the technology would be maintained for a long period of time.

By describing our areas of priority in detail, we do not wish to preclude grant applications that address different areas that we may not have thought of. We would like to fund all projects that bring value to the ecosystem. If you are considering applying for a project and are not sure if it falls within our areas of interest, please get in touch with us to discuss it.

## :bookmark_tabs: Layers of Polkadot Stack

In the below sections you can find a list of different layers of the Polkadot Stack.

### :iphone: User Interface 

| Components | Existing projects | Potentially interesting projects
|-|-|-
| Desktop/Web Wallets | [Talisman Web Application](https://github.com/TalismanSociety/talisman-web), [AirGap](https://github.com/airgap-it/airgap-wallet), [Sakura](https://github.com/w3finance/sakura) | User-friendly Wallet based on the [Recovery Pallet](https://github.com/paritytech/substrate/tree/master/frame/recovery), Web wallets focused on user-onboarding (e.g. using [localStorage](https://github.com/near/near-wallet))
| Browser Extensions | [Polkadot{.js}](https://github.com/polkadot-js/extension), [Polkadot-Js-Plus-Extension](https://github.com/Nick-1979/polkadot-Js-Plus-extension), [SubWallet-Extension](https://github.com/Koniverse/SubWallet-Extension), [Doter](https://github.com/ChainBridgeNetworkTeam/Doter), [Enzyme](https://getenzyme.dev/), [Speckle OS](https://github.com/GetSpeckle) | Sign-in with your polkadot, kusama, etc. account.  
| Mobile Wallets|  [Lunie](https://github.com/luniehq/lunie), [Polkawallet](https://github.com/polkawallet-io/polkawallet-flutter), [Parity Signer](https://github.com/paritytech/parity-signer), [imToken](https://github.com/consenlabs/token-core), [Fearless Wallet Android](https://github.com/soramitsu/fearless-Android), [Fearless Wallet iOS](https://github.com/soramitsu/fearless-iOS), [Stylo](https://github.com/stylo-app/stylo), [Nova Wallet](https://github.com/nova-wallet), [Fractapp](https://github.com/fractapp/fractapp/)  
| Burner Wallets/Faucet| [KodaDot](https://kodadot.js.org/), [Astar Faucet Bot](https://github.com/AstarNetwork/astar-faucet-bot) | Faucet (a sybil-resistant way to receive free tokens)
| CLI Wallet | [Subwallet](https://github.com/yxf/subwallet), [Proxy-hot-wallet](https://github.com/canontech/proxy-hot-wallet)
| Multisignature Wallets| [Subscan Multisig UI - React](https://github.com/itering/subscan-multisig-react), [Subscan Multisig UI](https://github.com/itering/subscan-multisig-ui), [Dorafactory-Multisig](https://github.com/DoraFactory/dorafactory-multisig) |
| Hardware Wallets | [Ledger Polkadot](https://github.com/ZondaX/ledger-polkadot), [Ledger Kusama](https://github.com/Zondax/ledger-kusama), [NGRAVE](https://ngrave.io/) | Trezor
| Block Explorers | [Polkascan](https://github.com/polkascan), [Polkastats](https://github.com/Colm3na), [Subscan](https://github.com/itering/subscan), [Statescan](https://github.com/opensquare-network/statescan), [Edgscan](https://github.com/edgeware-builders/edgscan) | Ink Smart Contract Explorer, Mempool focused explorer (including parachain transaction)
| Validator Dashboards | [Polkacube](https://github.com/hashquark-io), [YieldScan](https://github.com/buidl-labs/YieldScan), [Hubble](https://github.com/figment-networks/hubble/tree/master/app/controllers/polkadot)
| Node Explorers | [Polkadot Node Explorer](https://github.com/protos-research/polkadot-node-explorer)
| NFT Explorer | [NFT Explorer for Kusama & Polkadot](https://github.com/kodadot/nft-gallery)
| Governance Dashboards | [Polkassembly](https://github.com/premiurly/polkassembly), [dotreasury](https://github.com/opensquare-network/dotreasury), [Bright Treasury](https://github.com/bright/bright-tresury), [OpenSquare offchain voting](https://github.com/opensquare-network/collaboration) | UI for the kusama and/or polkadot treasury (see [bounty module](https://github.com/paritytech/substrate/pull/5715)), UI for Parachain Lease Offering (PLO)  |
| Staking Rewards | [Staking Rewards Collector](https://github.com/w3f/staking-rewards-collector), [Staking Rewards Viewer](https://github.com/jackson-harris-iii/staking-rewards-viewer), [Polkadot Staking Site](https://github.com/cryptolab-network/polkadot-staking-site) |
| Bridge UI | [Parity Bridges UI](https://github.com/paritytech/parity-bridges-ui), [Donut Interface (Steem <> Dot)](https://github.com/nutbox-dao/donut-interface) | |
| Parachain/Crowdloan | [Parachains.Network](https://github.com/jhonalino/parachains.network), [PolkAuction](https://github.com/CrommVardek/polk-auction-ui) | |
| Identicon | [PolkadotWebIdenticon](https://github.com/RidOne-technologies/polkadot-web-identicon), [Polkadot Angular IdentIcon](https://github.com/RidOne-technologies/polkadot-angular-identicon), [Bird Identicon](https://github.com/Noc2/Bird-Identicon)  |
| Other | [KappaSigmaMu Fratority](https://github.com/KappaSigmaMu/ksm-app), [Quadratic Funding Webapp](https://github.com/OAK-Foundation/quadratic-funding-webapp), [Polkawatch](https://gitlab.com/polkawatch), [Bytepay](https://github.com/bytepayment/bytepay), [charging-management-platform](https://github.com/Delmonicos/charging-management-platform) | Portfolio Viewer like Zapper or Zerion

### :wrench: Tools, APIs and Languages

| Components | Existing projects | Potentially interesting projects
|-|-|-
| Parachain | [Parachain utilities](https://github.com/AcalaNetwork/parachain-utilities), [Gantree](https://github.com/flex-dapps)| Tools to create parachains from frameworks used in other ecosystems |
| Client Libraries | [Go](https://github.com/centrifuge/go-substrate-rpc-client), [.Net](https://github.com/usetech-llc/polkadot_api_dotnet), [.NET Standard 2.0](https://github.com/ajuna-network/Ajuna.NetApi), [C++](https://github.com/usetech-llc/polkadot_api_cpp), [C](https://github.com/finoabanking/substrate-c-tool), [Haskell](https://github.com/airalab/hs-web3), [Javascript](https://github.com/polkadot-js/api), [Substrate API Sidecar - TypeScript](https://github.com/paritytech/substrate-api-sidecar), [Ruby](https://github.com/itering/scale.rb), [Python](https://github.com/polkascan/substrate-interface-api), [Java](https://github.com/polkadot-java), [Java (+ Android)](https://github.com/emeraldpay/polkaj), [Substrate Client Java](https://github.com/strategyobject/substrate-client-java), [Rust SCS](https://github.com/scs/substrate-api-client), [Rust Parity](https://github.com/paritytech/substrate-subxt), [PHP (gmajor-encrypt)](https://github.com/gmajor-encrypt/php-substrate-api), [PHP (neha0921)](https://github.com/neha0921/substrate-interface-package), [RPC-Ethereum](https://github.com/paritytech/frontier), [Swift](https://github.com/tesseract-one/Substrate.swift) | |
|Substrate Contract clients | [PatractGo](https://github.com/patractlabs/go-patract)  | |
| SCALE Codec | [Rust](https://github.com/paritytech/parity-scale-codec), [Python](https://github.com/polkascan/py-scale-codec), [Golang Chainsafe](https://github.com/ChainSafe/gossamer/tree/development/lib/scale), [Golang Itering](https://github.com/itering/scale.go), [C](https://github.com/MatthewDarnell/cScale), [C++](https://github.com/soramitsu/scale-codec-cpp), [JavaScript](https://github.com/polkadot-js/api), [AssemblyScript](https://github.com/LimeChain/as-scale-codec), [Haskell](https://github.com/airalab/hs-web3/tree/master/src/Codec), [Java](https://github.com/emeraldpay/polkaj), [Ruby](https://github.com/itering/scale.rb), [Dart](https://github.com/nbltrust/dart-scale-codec), [Swift](https://github.com/tesseract-one/swift-scale-codec), [PHP](https://github.com/gmajor-encrypt/php-scale-codec),  [JavaScript by Soramitsu](https://github.com/soramitsu/scale-codec-js-library) |
| Easy Runtime Development | [VS Code Plugin](https://github.com/everstake/vscode-plugin-substrate), [Atom Code Plugin](https://github.com/everstake/atom-plugin-substrate), [Substrate Playground](https://github.com/paritytech/substrate-playground), [Substrate Marketplace VS Code Plugin](https://github.com/paritytech/vscode-substrate), [AssemblyScript Runtime Generation](https://github.com/LimeChain/as-substrate-runtime), [Substrate Package Manager](https://github.com/clearloop/sup), [Subsembly: Framework for developing AssemblyScript Substrate Runtimes](https://github.com/LimeChain/subsembly), [dependency diener](https://github.com/bkchr/diener) | |
| Easy Smart Contract Development | [ink-playground](https://github.com/staketechnologies/ink-playground/tree/master), [Ink! Remix Plugin](https://github.com/blockchain-it-hr/ink-remix-plugin)
| Runtime Security | [K specifications](https://github.com/kframework/wasm-semantics), [PolPatrol - Polkadot Runtime Checker](https://github.com/ChainSecurity/polpatrol) | Automated Runtime checking tools, economic audit simulator such as [gauntlet.network](https://gauntlet.network/)
| Smart Contract Languages | [Ask!](https://github.com/patractlabs/ask), [Subscript](https://github.com/slickup/subscript), [Solang](https://github.com/hyperledger-labs/solang), [Ink!](https://github.com/paritytech/ink), [Pact](https://github.com/kadena-io/), [Move VM Substrate](https://github.com/pontem-network/sp-move), [Move smart contract by Neatcoin](https://github.com/neatcoin/neatcoin)  | Functional Programming Languages, other languages with developed toolchains |
| Smart Contract Security |
| Testing | [Halva](https://github.com/orgs/halva-suite), [Ink Waterfall](https://github.com/paritytech/ink-waterfall), [Redspot](https://github.com/patractlabs/redspot), [MixBytes Tank](https://github.com/mixbytes/tank), [sub-flood](https://github.com/NikVolf/sub-flood), [Substrate debug-kit](https://github.com/paritytech/substrate-debug-kit), [Dotscale - SCALE Codec Comparator](https://github.com/arijitAD/dotscale), [Asset CLI tool](https://github.com/JesseAbram/asset_cli_tool), [sub_crash](https://github.com/JesseAbram/unfinished_testing_tool), [subwasm](https://github.com/chevdor/subwasm), [subsee](https://github.com/ascjones/subsee), [polkadot-lab](https://github.com/w3f/polkadot-lab), [Zombienet](https://github.com/paritytech/zombienet), [RPC-perf](https://github.com/dwellir-public/rpc-perf/)
| Testnet | [Polkadot Launch](https://github.com/paritytech/polkadot-launch), [polkadot-starship](https://github.com/koute/polkadot-starship), [Fork off Substrate](https://github.com/maxsam4/fork-off-substrate), [Parachain Launch](https://github.com/open-web3-stack/parachain-launch) |
| Benchmarking | [Substrate Graph Benchmarks](https://github.com/shawntabrizi/substrate-graph-benchmarks) |
| Blockchain Indexing Engine | [Substrate Archive](https://github.com/paritytech/substrate-archive), [PSQL Indexer](https://github.com/usetech-llc/polkadot_psql_indexer), [Polkadothub Indexer](https://github.com/figment-networks/polkadothub-indexer), [Substrate Graph](https://github.com/playzero/substrate-graph), [Hydra](https://github.com/subsquid/hydra), [Subquery](https://github.com/OnFinality-io/subql), [Polkadot Profit Transformer](https://github.com/p2p-org/polkadot-profit-transformer) |
| Blockchain/Event Monitoring | [Web3 Guardian](https://github.com/open-web3-stack/guardian), [Aurras Event Manager](https://github.com/HugoByte/aurras-event-manager), [@commonwealth/chain-events](https://github.com/hicommonwealth/chain-events) |
| Gaming | [Mobile Game Framework for Substrate](https://github.com/creator-rs/creator/) | [Amethyst](https://amethyst.rs/) + [Substrate](https://substrate.dev/)
| No-code Platforms | [EzCode's Polkadot.js plugin on Bubble.io](https://bubble.io/plugin/polkadotjs-1639402639641x977692461648052200), [Blackprint Visual Programming Polkadot.js module](https://github.com/Blackprint/nodes-polkadot.js) | |
| XCM | [XCM-tools](https://github.com/PureStake/xcm-tools) | |
| Other | [open-web3 JS library](https://github.com/open-web3-stack/open-web3.js), [VM-Bridge](https://github.com/CycanTech/GVM-Bridge), [srtool](https://github.com/paritytech/srtool), [Substrate Tip Bot](https://github.com/paritytech/substrate-tip-bot), [ORI (Onchain Risk Intelligence)](https://github.com/syntifi/ori), [PolkaTools](https://github.com/albertov19/PolkaTools), [polkadot-scripts](https://github.com/paritytech/polkadot-scripts), [Static analyzer for Substrate FRAME's pallets](https://github.com/simon-perriard/saft)

### :memo: ink Smart Contracts 

| Components | Existing projects | Potentially interesting projects
|-|-|-
| DeFi | [Vera](https://github.com/veradefi/defi), [Nsure Insurance](https://github.com/nsure-tech/dot-contract), [Everlasting Cash](https://github.com/CycanTech/ELC), [Coinversation](https://github.com/Coinversation/coinpro), [zenlink-dex-contract](https://github.com/zenlinkpro/zenlink-dex-contract), [AlgoCash](https://github.com/ReserveLabs/AlgoCash) | New seigniorage-style stable coins
| Gaming | [NewOmega](https://github.com/WiktorStarczewski/newomega.polkadot/blob/master/newomega_delegator/newomega/newomega.rs) | |
| DAO | [subDAO](https://github.com/SubDAO-Network/subDAO-contracts), [RainbowDAO](https://github.com/RainbowcityFoundation/RainbowDAO-Protocol-Ink-milestone_1) | |
| Spam Protection | [Prosopo](https://github.com/prosopo-io/integration) | |
| Other | [Candle Auctions](https://github.com/agryaznov/candle-auction-ink), [polkasign-contract](https://github.com/SubDAO-Network/polkasign-contract) | |


### :link: Chains and Pallets 

| Components | Existing projects | Potentially interesting projects
|-|-|-
| Scalable Transactions | [Perun channels](https://github.com/perun-network/perun-polkadot-pallet), [CLI demo of Perun](https://github.com/perun-network/perun-polkadot-demo), [Astar](https://github.com/AstarNetwork/Astar), [Celer](https://github.com/celer-network), [Gunclear](https://github.com/GunClear)| roll-ups, DAG-based consensus mechanisms, side chains |
| Bridges |  [interBTC](https://github.com/interlay/interbtc), [Ethereum by Centrifuge](https://github.com/centrifuge/), [EOS by Bifrost](https://github.com/bifrost-finance), [POA <> Substrate](https://github.com/paritytech/parity-bridge), [Substrate <> Ethereum DAI Bridge](https://github.com/akropolisio/POC-polkadai-bridge), [Substrate <> Substrate Bridge](https://github.com/paritytech/substrate-bridge-relay), [BTC by ChainX](https://github.com/chainx-org/ChainX), [Cosmos-Substrate bridge](https://github.com/ChorusOne/wormhole-bridge), [Substrate IBC Pallet](https://github.com/octopus-network/substrate-ibc), [Polkadot Ethereum Bridge](https://github.com/Snowfork/polkadot-ethereum), [Darwinia](https://github.com/darwinia-network/darwinia), [Stellar/DeFi Bridge by Pendulum](https://github.com/pendulum-chain/pendulum-prototype), [Filecoindot](https://github.com/ChainSafe/filecoindot) | ZCash |
| Privacy | [Webb Anon](https://github.com/webb-tools/anon), [ZeroChain](https://github.com/LayerXcom/zero-chain), [pLibra (Phala Network)](https://github.com/phala-network), [Automata Network](https://github.com/automata-network/automata), [zCloak Network](https://github.com/zCloak-Network), [Zero Network](https://github.com/zero-network) |  [Multi-Asset Shielded Pool (MASP)](https://github.com/anoma/masp), [Zkay](https://arxiv.org/pdf/2009.01020.pdf), [Zexe](https://eprint.iacr.org/2018/962.pdf)
| ZKP | [ZeroPool](https://github.com/zeropoolnetwork), [Megaclite](https://github.com/patractlabs/megaclite), [zkMega](https://github.com/patractlabs/zkmega), [PLONK for Substrate](https://github.com/AstarNetwork/plonk) |
| Off-Chain | [substraTEE](https://github.com/scs/substraTEE)
| DeFi | [Compound Gateway](https://github.com/compound-finance/gateway), [Parallel Finance](https://github.com/parallel-finance/parallel), [PINT](https://github.com/ChainSafe/PINT), [Katal Chain](https://github.com/katalchain), [Laminar Chain](https://github.com/laminar-protocol/laminar-chain), [Acala](https://github.com/AcalaNetwork), [Centrifuge](https://github.com/centrifuge/), [Stafi](https://github.com/stafiprotocol/stafi-node), [Bandot](https://github.com/bandotorg/Bandot), [Definex](https://github.com/y2labs-0sh), [OAX Foundation](https://github.com/OAXFoundation/parrot), [Cybex](https://github.com/alexxuyang/substrate-dex), [Zenlink](https://github.com/zenlinkpro/pallet-zenlink), [Swaps Pallet](https://github.com/lsaether/pallet-swaps), [Polkadex](https://github.com/Polkadex-Substrate/Polkadex/tree/master), [SubDEX](https://github.com/subdarkdex), [HydraDX](https://github.com/galacticcouncil/hack.HydraDX-node), [Substrate Stablecoin](https://github.com/apopiak/stablecoin), [Standard protocol](https://github.com/digitalnativeinc/standard-substrate), [Polkaswap](https://github.com/sora-xor/sora2-network), [Curve AMM](https://github.com/equilibrium-eosdt/equilibrium-curve-amm), [Konomi Network](https://github.com/konomi-network/cumulus/), [Composable Finance](https://github.com/ComposableFi/composable), [Stable Asset](https://github.com/nutsfinance/stable-asset), [Libra Payment](https://github.com/atscaletech/libra), [Mangata](https://github.com/mangata-finance/mangata-node) | DEX with privacy and confidentiality features such as those found in a [dark pool](https://en.wikipedia.org/wiki/Dark_pool)
| Smart contract chains | [moonbeam](https://github.com/PureStake/moonbeam), [Edgeware](https://github.com/hicommonwealth), [EVM Module](https://substrate.dev/docs/en/next/conceptual/runtime/contracts/evm_module), [ParaState](https://github.com/ParaState/substrate-ssvm-node), [gear](https://github.com/gear-tech/gear), [CENNZnet](https://github.com/cennznet/cennznet), [SkyeKiwi](https://github.com/skyekiwi/skyekiwi-network) | smart contract chains with novel security approaches, smart contract chains based on existing toolchains|
| Oracle | [Laminar](https://github.com/laminar-protocol/open-runtime-module-library/tree/master/oracle), [Parallel Finance](https://github.com/parallel-finance/parallel/blob/feature-oracle/pallets/ocw-oracle/src/lib.rs), [Katal Chain](https://github.com/katalchain/blockchain/tree/master/modules/oracle), [Chainlink-polkadot](https://github.com/smartcontractkit/chainlink-polkadot), [Ares Protocol](https://github.com/aresprotocols/ares), [Kylin Network](https://github.com/Kylin-Network/kylin-node), [interbtc-clients oracle](https://github.com/interlay/interbtc-clients/tree/master/oracle), [Anonima](https://github.com/webb-tools/anonima), [Apollo](https://github.com/ComposableFi/composable/tree/main/frame/oracle)
| Identity/DID | [Caelum Labs](https://gitlab.com/caelum-tech/lorena), [Litentry](https://github.com/litentry/litentry-runtime), [pallet-did](https://github.com/substrate-developer-hub/pallet-did), [dot-id](https://github.com/prasad-kumkar/dot-id)
| IoT | [Nodle](https://github.com/NodleCode/), [MXC/DataHighway](https://github.com/DataHighway-DHX/node), [peaq-network-node](https://github.com/peaqnetwork/peaq-network-node)
| Verifiable Claims | [KILT](https://github.com/KILTprotocol), [Dock](https://github.com/docknetwork), [Fennel Protocol](https://github.com/fennelLabs/Fennel-Protocol)
| Supply chain| | | 
| Health care| [AriaHealth](https://github.com/AriaHealth/MetaNetwork) | | 
| Social Networking | [Social Network](https://github.com/social-network), [SubSocial](https://github.com/dappforce/dappforce-subsocial), [ZeroDAO](https://github.com/ZeroDAO/ZeroDAO-node), [Myriad Node](https://github.com/myriadsocial/myriad-node), [Wika Network](https://github.com/randombishop/wika_etl) | Private instant messenger that uses on-chain identity
| Governance/DAO| [Sunshine DAO](https://github.com/sunshine-protocol/sunshine-bounty), [Governance OS](https://github.com/NucleiStudio/governance-os), [Idavoll Network](https://github.com/idavollnetwork/idavoll), [Substrate Moloch](https://github.com/DoraFactory/Substrate-Moloch-V2) |   [Consul](https://github.com/consul/consul) - Open Government and E-Participation Web Software
| Prediction Markets and Futarchy| [Zeitgeist](https://github.com/zeitgeistpm/zeitgeist), [X Predict Market](https://github.com/XPredictMarket) |
| Messaging | [HOPR](https://github.com/validitylabs/HOPR-PL-Substrate), [Mailchain](https://github.com/mailchain), [Nolik](https://github.com/chainify/pallet-nolik/)
| File Storage, Cloud | [DatDot](https://github.com/playproject-io/datdot), [Crust Network](https://github.com/crustio), [offchain::ipfs](https://rs-ipfs.github.io/offchain-ipfs-manual/), [Canyon Network](https://github.com/canyon-network/canyon), [CESS](https://github.com/Cumulus2021/cess), [CESS Proving Subsystem](https://github.com/CESSProject/cess-proving-system), [Iris](https://github.com/iridium-labs/iris), [fmd-cess](https://github.com/CESSProject/fmd-cess), [IPFS Frame V3](https://github.com/DanHenton/pocket-substrate/tree/ipfs-ocw)
| Name Service| [Substrate Names](https://github.com/xaya/substrate-names), [ENS on Substrate](https://github.com/hskang9/substrate-name-service), [PNS-Pallets](https://github.com/pnsproject/pns-pallets)
| Gaming | [Bit.country](https://github.com/bit-country/Bit-Country-Blockchain), [SubGame](https://github.com/SubGame-Network/subgame-network), [subzero](https://github.com/playzero/subzero), [Web3Games](https://github.com/web3gamesofficial/web3games-blockchain), [Ajuna Network](https://github.com/ajuna-network/), [Gafi Network](https://github.com/cryptoviet/gafi) | 
| Computation/AI | [DeepBrain Chain](https://github.com/DeepBrainChain/DeepBrainChain-MainChain), [AI Infrastructure on Blockchain](https://github.com/anudit/cerebrum) |
| Enable specific use-cases | [Robonomics](https://github.com/airalab/substrate-node-robonomics), [UniversalDOT](https://github.com/UniversalDot), [Evercity Sustainable Finance Protocol](https://github.com/EvercityEcosystem/evercity-chain), [Fennel Protocol](https://github.com/fennelLabs/Fennel-Protocol)
| NFT | [ternoa](https://github.com/capsule-corp-ternoa/chain), [FRAME Pallet: NFTs for Substrate](https://github.com/danforbes/pallet-nft), [NFT Parachain by usetech](https://github.com/w3f-community/nft_parachain), [DNFT](https://github.com/DNFT-Team/dnft-substrate-node/tree/master/pallets), [RMRK-Substrate](https://github.com/rmrk-team/rmrk-substrate)
| Randomness | [DKG and Randomness Beacon](https://github.com/Cardinal-Cryptography/substrate/tree/randomness-beacon)
| Licensing | [Anagolay Network](https://github.com/anagolay/anagolay-chain)  | 
| Banking Integration | [FIAT on-off-ramp](https://github.com/element36-io/ebics-java-service)
| Crowdfunding | [Imbue Network](https://github.com/ImbueNetwork/imbue), [Quadratic Funding pallet by Dora](https://github.com/zhangjiannan/QFgrant), [Quadratic Funding pallet by OAK](https://github.com/OAK-Foundation/quadratic-funding-pallet/tree/master)  |  [Minimum Anti-Collusion Infrastructure (MACI)](https://ethresear.ch/t/minimal-anti-collusion-infrastructure/5413) 
| Other | [Substrate Open Runtime Module Library](https://github.com/open-web3-stack/open-runtime-module-library), [Substrate Account Filter](https://github.com/gautamdhameja/substrate-account-filter), [Subtensor](https://github.com/opentensor/subtensor), [BitGreen](https://github.com/bitgreen/bitg-node), [AdMeta](https://github.com/AdMetaNetwork/admeta), [Chocolate Node](https://github.com/chocolatenetwork/chocolate-node), [Virto Network](https://github.com/virto-network/virto-node), [Substrate Validator Set](https://github.com/gautamdhameja/substrate-validator-set), [DEIP](https://github.com/DEIPworld/deip-substrate), [DeBio](https://github.com/debionetwork/debio-node), [MathChain](https://github.com/mathwallet/MathChain), [encointer](https://github.com/encointer/encointer-node), [Grassland](https://github.com/grasslandnetwork/substrate_node) | Decentralized review/reputation system

### :black_circle: Host

| Components | Existing projects | Potentially interesting projects
|-|-|-
| Rust | [Substrate](https://github.com/paritytech/substrate), [Cumulus](https://github.com/paritytech/cumulus)
| C++ | [Kagome](https://github.com/soramitsu/kagome)
| Go | [Gossamer](https://github.com/ChainSafe/gossamer)
| AssemblyScript |
| Light Client | [Substrate Connect](https://github.com/paritytech/substrate-connect) |

### :electric_plug: Network Maintenance Tools

| Components | Existing projects | Potentially interesting projects
|-|-|-
| Secure validator setup | [Polkadot Validation Node Ansible Setup](https://github.com/polkachu/polkadot-validator), [Trutzone-based HSM](https://github.com/ZondaX), [W3F Polkadot Validator Setup](https://github.com/w3f/polkadot-validator-setup)  
| High availability setup | [Archipel](https://github.com/luguslabs/archipel), [Polkadot Failover Mechanism](https://github.com/protofire/polkadot-failover-mechanism), [Open Node Framework](https://github.com/Tenet-X/open-node)
| Load Balanced Endpoints | [terragrunt-polkadot](https://github.com/insight-w3f/terragrunt-polkadot)
| Deployment Tools| [Polkadot Package Manager](https://github.com/Blockdaemon/bpm-sdk), [PolkaHub](https://github.com/akropolisio/polkahub-monorepo), [Avado](https://github.com/AvadoDServer/AVADO-DNP-Polkadot-custom), [Polkadot Deployer](https://github.com/w3f/polkadot-deployer)
| Validator monitoring | [P.A.N.I.C.](https://github.com/SimplyVC/panic_polkadot), [Polkalert](https://github.com/galacticcouncil/polkalert), [B-Harvest](https://github.com/nodebreaker0-0/substrate/tree/prometheus_v0.3), [nmonpolkadot](https://github.com/stakezone/nmonpolkadot), [Polkadot-K8s-Monitor](https://github.com/ironoa/polkadot-k8s-monitor), [Polkadot-Watcher](https://github.com/w3f/polkadot-watcher), [1KV Telegram Bot](https://github.com/helikon-labs/polkadot-kusama-1kv-telegram-bot)
| Validator payout management | [Substrate validator auto payout](https://github.com/Colm3na/substrate-auto-payout), [Polkadot Payouts](https://github.com/w3f/polkadot-payouts), [staking-payouts CLI](https://github.com/emostov/staking-payouts), [Payctl](https://github.com/stakelink/substrate-payctl), [crunch](https://github.com/turboflakes/crunch) |

### :black_nib: Signatures

| Components | Existing projects | Potentially interesting projects
|-|-|-
| SR25519 | [rust](https://github.com/w3f/schnorrkel) (contains partial bindings for C, JavaScript, and Python), [.Net bindings](https://github.com/gautamdhameja/sr25519-dotnet), [C](https://github.com/usetech-llc/sr25519) *(old)*, [C](https://github.com/TerenceGe/sr25519-donna) *(new)*, [C/C++](https://github.com/soramitsu/soramitsu-sr25519-crust), [C#](https://github.com/usetech-llc/sr25519_dotnet), [Go](https://github.com/ChainSafe/go-schnorrkel), [java](https://github.com/debuggor/schnorrkel-java), [PHP](https://github.com/gmajor-encrypt/sr25519-bindings)
| Distributed key generation (DKG) | [keygen.rs](https://github.com/isislovecruft/frost-dalek)
| Validator HSMs| |
| Validator HSM-like solutions|

### :heavy_check_mark: Consensus

| Components | Existing projects | Potentially interesting projects
|-|-|-
| PoC | [Spartan](https://github.com/subspace/substrate) |
| PoW | [PoW consensus for Substrate](https://github.com/paritytech/substrate/tree/master/client/consensus/pow), [RandomX](https://github.com/kulupu/kulupu/tree/master/pow), [Sha3 PoW](https://github.com/substrate-developer-hub/recipes/tree/master/consensus/sha3pow) |
| Block production | [BABE](https://github.com/paritytech/substrate/tree/master/client/consensus/babe), [Aura](https://github.com/paritytech/substrate/tree/master/client/consensus/aura) |
| Finality | [GRANDPA](https://github.com/paritytech/substrate/tree/master/frame/grandpa) |
| Other | [Nimbus: Upgradeable consensus framework](https://github.com/PureStake/nimbus) | 


### :satellite: Networking

| Components          | Existing projects                                                                                               | Potentially interesting projects |
|---------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------|
| DHT crawler         | [Go](https://github.com/atredispartners/dht-crawler-polkadot), [Kotlin](https://github.com/emeraldpay/polkabot) |                                  |
| RPC Tor-like access | [WhiteNoise](https://github.com/Evanesco-Labs/WhiteNoise.rs)                                                    |                                  |

## :construction_worker: Contributing

Pull requests, issues, or other contributions from the community are encouraged!  You can not only add specific projects, but also potentially interesting fields/areas which are currently missing in the tech stack.

:heavy_exclamation_mark: All technologies listed above need to be open-source. Ideally, the links lead directly to the code.

_Note: You will need a GitHub account to suggest changes or open issues. If you do not have one, you may [sign up for free](https://github.com/join)._
