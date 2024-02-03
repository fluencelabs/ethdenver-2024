# Fluence ETHDenver 2024 Buidlathon Tracks And Bounties

Welcome to the Year of the SporkWhale which undoubtedly will culminate in another epic Hackathon pushing the boundaries of decentralization to new heights. To this end, Fluence is sponsoring five buidl tracks paying out a combined total of USDC 25,000! Eat the Cloud with Fluence and join us for the '24 Buidlathon and the [Fluence DE:PIN Summit](), 02/27/2024 in mile-high Denver.

## About Fluence

[Fluence](https://fluence.network/) is a decentralized serverless compute and infrastructure (DePin) platform. With Fluence, developers create Fluence Compute Functions and deploy them to Tier 4 data centers providing provable, decentralized CPU and RAM resources. Fluence's on-chain marketplace, built on [IPC](https://www.ipc.space/), facilitates the trustless matching of developers' capacity demand and providers' capacity supply for one, or many, Fluence Compute Functions at a time. That is, developers not only work with decentralized compute at the application or protocol level but also at the infrastructure level.


## Buidl With Fluence

Fluence Functions is a decentralized, stateless compute service leveraging the Wasm-Wasi runtime without developers having to provision or manage servers. Fluence Functions not only follow the serverless paradigm but introduce decentralization at the compute as well as the server level. That is, Fluence Functions execute on decentralized physical infrastructure (DePin) enabling the decentralization of applications and protocols from the bottom up.

### Create, Deploy And Execute A Fluence Compute Function -- 5 x USDC 1,000

Create a Fluence Compute Function of your choice, deploy it to the Fluence testnet and orchestrate it with Fluence Workflow. Examine the function locally with the REPL provided by Fluence CLI and orchestrate the distributed function with an Aqua script. Use Fluence CLI to execute the Aqua script and capture the response.

Be one of the first five (5) submitters of a functional and complete solution to be eligible for a bounty. Follow the submissions guides provided below **and** add a screenshot of the REPL output for your function and document the captured function response.

### Improve Your dAPP with fRPC -- 5 x USDC 1,000

While RPC as a Service is a convenient and cost efficient option to bring EVM JSON-RPC to your dAPP, it introduces some side-effects: single-point of failure, data integrity and privacy concerns come to mind.

Fluence has prepared a substrate to easily and cheaply enable decentralized RPC for your dApp from existing building blocks using [fRPC](https://github.com/fluencelabs/fRPC-Substrate). By adding multiple RPC endpoints of your choosing, self-hosting a tiny http gateway with your dApp, deploying the provided compute function to the number of peers of your choosing and configuring the Aqua script to select the desired distributed availability or consensus algorithm, e.g. failover or quorum, you can enable you dApp with a performant decentralized RPC solution without having to touch the code of your dApp.

You provide request logs for at least two different json-rpc method requests from your dApp illustrating the elimination of a single point of failure, much improved privacy and data integrity. Be one of the first five (5) submitted, functional solutions to integrate fRPC with your dAPP to cash in on a USDC 1,000 bounty. See submission guidelines below for more information and requirements.

### Integrate Your Fluence Functions With Ceramic -- 1 x USDC 2,500, 1 X USDC 1,500, 1 X USDC 1,000

Like all serverless compute solutions, Fluence Functions is inherently stateless, which means durable storage needs to be integrated into the solution stack. This track rewards hackers to integrate [Ceramic](https://ceramic.network/) as the decentralized data layer for your Fluence Functions.

Your Fluence Functions need to have a read and write capability to Ceramic Streams or Compose DB and choreograph your Fluence Compute Functions with Aqua scripts to demonstrate the read and write operation. Bonus points for deploying your function to more than one provider in the Fluence testnet and to code your Aqua script to take advantage of this deployment. For example, write from the function on one peer and read from the function from the other peer.

 Follow the submissions guides provided below.

### Spread Your Wings With Fluence Functions, ZK or MPC  -- 1 x USDC 3,500, 1 x USDC 1,500

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

Follow the submissions guides provided below.

#### Bring MPC Threshold Signature Schemes To Fluence Functions

[MPC TSS](https://wiki.mpcalliance.org/threshold%20keygen%20and%20storage.html) is a cryptographic primitive for [distributed key generation](https://en.wikipedia.org/wiki/Distributed_key_generation) and message signing. Not surprisingly, MPC TSS has attracted a lot of interest from the blockchain and Web3 community at large. 

In this build track, you are asked to implement or port an exiting MPC TSS library of your choosing to the Fluence Marine Wasm runtime and to illustrate distributed key generation, key refresh and message signing with Aqua workflows over your Fluence Functions wrapping your (ported) MPC TSS Wasm library. Your implementation should be two party or better and 
the implemented or ported MPC TSS library needs to be corrected for these [exploits](https://www.verichains.io/tsshock/).

Follow the submissions guides provided below.

### Utilize EIP 4844 For Short-Term State Management -- 1 x USDC 2,500, 1 x USDC 1,500, 1 x USDC 1,000

[EIP 4844](https://www.eip4844.com/), aka proto-dank-sharding, provides a new data type, Blob, on Ethereum. Blobs are persisted on beacon nodes and are pruned after approximately two weeks. Hence, EIP 4844 may provide Fluence Functions developers with a convenient, verifiable and cheap "intermediate" data durability layer suitable for retaining small state, such as stream pagination or subnet data synchronization. Moreover, Ethereum core devs have made EIP 4844 available on [Goerli](https://www.theblock.co/post/273050/ethereum-dencun-goerli-proto-danksharding) just in time!

Teams should implement a read-write EIP 4844 Blob solution for their Fluence Functions and demonstrate both operations in Aqua scripts. Moreover, an important aspect of this task is to manage the "discovery" of the Blob by your Fluence Functions.

Generously document the on-chain aspects of Blob creation and any resulting API(s). Follow the submissions guides provided below.

## Submission Guidelines

In addition to the [ETHDenver Rules & Regulations](), teams need to fork [this](https://github.com/fluencelabs/ethdenver-2024) repo and add their submission. Keep this repo **private** until the end of the Buidlathon. 

When the number of valid, eligible and equally accomplished submissions exceeds the number of prizes, as determined by the Judge(s), the timestamp of the last change of the submitted repo will serve as the tie-breaker.

An eligible submission requires teams to 

* generously document their solution with one or more readme files and, when applicable, code documentation
* commit the complete project scaffold to your forked repo including the .fluence directory
* submit a two (2) to five (5) minute (linked) Youtube, or similar, hosted video shilling your masterpiece
* submit as a Github or GitLab repo with MIT or Apache 2.0 license

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
