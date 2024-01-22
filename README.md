# Fluence ETHDenver 2024 Buidlathon Tracks And Bounties

Welcome to the Year of the SporkWhale which undoubtedly will culminate in another epic Hackathon pushing the boundaries of decentralization to new heights. To this end, Fluence is sponsoring 
five buidl tracks paying out a combined total of USDC 25,000!

## About Fluence

[Fluence](https://fluence.network/) is a decentralized serverless compute and DePin protocol. Buidling on Fluence, developers create Fluence Functions from Wasm and deploy their Fluence Functions to Tier 4 data centers providing provable, decentralized hardware resources. Fluence's on-chain marketplace built on [IPC](https://www.ipc.space/) facilitates the trustless matching of developers' capacity demand and providers' capacity supply one, or many, Fluence Functions at a time. That is, developers not only can work with decentralized compute but be assured that that compute is deployed on DePin instead of centrally controlled data centers. 

Eat the Cloud with Fluence, join us in the Buidlathon and the [Fluence DE:PIN Summit](), 02/27/2024 in mile-high Denver.


## Buidl With Fluence

### Improve Your dAPP with fRPC -- 5 x USDC 1,000

While RPC as a Service is a convenient and cost efficient option to bring EVM JSON-RPC to your dAPP, it introduces some crappy side-effects: single-point of failure, data integrity and privacy concerns come to mind.

Fluence has prepared a substrate to easily and cheaply enable decentralized RPC from existing building blocks using Fluence Functions call [fRPC](https://github.com/fluencelabs/fRPC-Substrate). By adding multiple RPC endpoints of your choosing and self-hosting a tiny http gateway with your dApp, you simple need to add the gateways url to your dAPP and to enjoy decentralized RPC: no single point of failure, much improved data integrity and significantly improved privacy.

Be one of the first five (5) submitted solutions to integrate fRPC with your dAPP to cash in on a USDC 1,000 bounty. See submission guidelines below for more information.

### Create And Deploy A Fluence Function -- 5 x USDC 1,000

Fluence Functions is a decentralized, stateless compute services built on Wasm without developers having to provision or manage servers. Fluence Functions not only follow the serverless paradigm like AWS Lambda or Azure Functions but introduce decentralization a the compute as well as server level via DePin. In fact, Fluence capacity providers commit provable capacity from Tier 4 data centers.

Create and deploy a Fluence Function of you choice to the Fluence testnet. Examine the function locally with Fluence's Marine REPL and run the function with Fluence's Aqua distributed workflow engine. Follow the submissions guides provided below and add a screenshot of the REPL output for your function.

### Integrate Your Fluence Functions With Decentralized Storage -- 1 x USDC 2,500, 1 X USDC 1,500, 1 X USDC 1,000

Like all serverless compute solutions, Fluence Functions is inherently stateless, which means durable storage needs to be integrated into the solution stack. Instead of centralized storage solutions, this track rewards hackers to integrate [Ceramic](https://ceramic.network/) as your a decentralized data layer to your decentralized compute with Fluence Functions.

At the very minimum, your Fluence Functions should have a read and write capability to the chosen storage solution and use different Aqua workflow scripts to demonstrate the read and write operation. 

### Spread Your Wings With Fluence, ZK or MPC  -- 1 x USDC 3,500, 1 x USDC 1,500

Tackle either the MPC or ZKP track for fame and fortune!

#### Buidl A ZK Circuit Backend for your dApp with Halo2 And Fluence Functions

ZKPs are increasingly an integral aspect of Web3 solutions and allow provers to convince verifiers that their claim is true without revealing the inputs to the claim. ZKPs come in all shapes and sizes: interactive vs non-interactive, range proofs, etc.

A popular ZKP protocol is [halo2](https://github.com/zcash/halo2), which is a recursive snark protocol without trusted setup. Moreover, halo2 not only is Rust-native implementation but also provides [Wasm bindings](https://crates.io/crates/halo2-wasm).

This track tasks you to port the halo2 tooling to Fluence's [Marine Wasm runtime]() to enable backends for proof generation and proof verification. Since a general purpose solution is out of the questions, you are encouraged to constrain the circuit to some reasonable problem, such as proving [Hamming distances](https://en.wikipedia.org/wiki/Hamming_distance). Hamming distances are quite useful in error correction as well as a measurement of (dis-) similarity for biometrics, which can and is used in dApps and other Web3 (identity) protocols. To further keep you on the path of success, you are encouraged to extensively draw from and build on, giving credit where credit is due, the two part tutorial *Building a ZK web app with Halo2 and Wasm* listed below.

##### References

* [Halo2 Book](https://zcash.github.io/halo2/user/simple-example.html)
* [halo2-wasm](https://crates.io/crates/halo2-wasm)
* [halo primer](https://medium.com/@ola_zkzkvm/halo-principle-explained-fa5a2e2767cd)
* Building a ZK web app with Halo2 and Wasm [part 1](https://medium.com/@yujiangtham/lets-dissect-a-zksnark-part-1-a82fc092f58a) and [part 2](https://medium.com/@yujiangtham/building-a-zero-knowledge-web-app-with-halo-2-and-wasm-part-2-379477444dc3)


### Utilize EIP 4844 For Short-Term State Management -- 1 x USDC 3,500, 1 x USDC 1,500

[EIP 4844](https://www.eip4844.com/), aka proto-dank-sharding, provides a new data type, Blob, on Ethereum. Blobs are persisted beacon nodes and are pruned after approximately two weeks. Hence, EIP 4844 may provide Fluence Functions developers with a convenient, verifiable and cheap "intermediate" data durability layer to Fluence Functions suitable for retaining small state, such as stream pagination, or subnet data synchronization. Moreover, Ethereum core devs have made EIP 4844 available on [Goerli](https://www.theblock.co/post/273050/ethereum-dencun-goerli-proto-danksharding).

Teams should implement at least a read-write EIP 4844 Blob solution for their Fluence Functions and demonstrate both operations in separate Aqua workflows. However, the most important aspect of this task is to manage the "discovery" of the Blob by your Fluence Functions without, duh, storing a Blob reference on another storage solution. That is, your solution should be able to "index" your Blob(s) against, say, your account address and your Functions.


## Submission Guidelines

In addition to the [ETHDenver Rules & Regulations](), eligible teams need to fork this repo and add their solution. Keep this repo **private** until the end of the Buidlathon. When the number of valid, eligible and equally accomplished submissions exceeds the number of prizes, as determined by the Judges, the timestamp of the last change of the submitted repo will serve as the tie-breaker.

An eligible submission requires teams to 

* generously document their solution with one or more readme files and, when applicable, code documentation
* provide a dockerized demo of your solution
* submit a two (2) to five (5) minute (linked) Youtube, or similar, hosted video shilling you masterpiece
* Submit via a Github or GitLab repo with MIT or Apache 2.0 license

Please note that teams not only are eligible but encouraged to submit solutions for more than one track!

## Workshop

An IRL workshop is scheduled for February 25, 2024, TBD at TDB. For updates, please subscribe to the [Fluence discord](https://fluence.chat/) channel.



## Resources

* [Fluence Home](https://fluence.network/)
* [Fluence Docs](https://fluence.dev)
* [Fluence Github](https://github.com/fluencelabs)
* [Discord](https://fluence.chat/)
* [Telegram](https://t.me/fluence_project)
* [X](https://twitter.com/fluence_project)
* [Youtube](https://www.youtube.com/channel/UC3b5eFyKRFlEMwSJ1BTjpbw)