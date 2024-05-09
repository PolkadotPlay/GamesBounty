# CLAWBIRD CHAOS

- **Team Name:** Clawbird Pty Ltd
- **Funding Details:**
  - **DOT**: For the **DOT** compensation, please provide a Polkadot address. (ex. multisig, with core contributors)

> **TODO**: Update this section with funding details

## Game Project Overview :page_facing_up:

# Game Project Application Form

## 1. Pitch the Game

### Please describe the game in a short pitch.

"CLAWBIRD CHAOS" merges choose your own adventure stories with the biographies of real-world identities, pseudo identities, or your own identity, with their associated on-chain Web3 identities, DAO entities, or pseudo identities, and various Polkadot ecosystem capabilities to unveil captivating Web3 narratives and learning pathways that are player-driven and dynamically generated from the latest Polkadot SDK and optionally from a player's custom extensions or coretime choice, and where achievements are unlocked to recognise improvements in their cultural appreciation, encouraging them to proportionally stretch their face-to-face or video-based Web3 social connectedness, allow them to feed and train their own generative AI with upgrades of more unique knowledge through match-making, and to trade that knowledge with in a legal, privacy-preserving, and ethical way.

### Please describe the game's core loop? (minimalistic)

``` mermaid
---
title: CLAWBIRD CHAOS Gameplay Loop
---
flowchart LR
id1[Identify] --> id2[Interact] --> id3[Learn]  --> id5[Connect] --> id6[Mint] --> id7[Upgrade] --> id8[Buy/Sell] --> id9[Repeat]
```

### Are there any existing games that you would consider similar to your project?
*If so, please list them and describe how your game compares or differs.*

NO, not yet that we are aware of.

> **TODO**: Update this section with any existing games that are similar.

### Do you have a Game Design Document (GDD) for your project?
- **If yes,** *could you please share the link of the document with us?*
- **If no,** *could you provide an excerpt or summary that highlights key aspects of your game's design, mechanics, and vision?*

NO, we do not have one yet to share but we may produce one that may be shared with one or two curators if they sign an NDA.

> **TODO**: Update this section with GDD

## 2. Game Dev Experience

### Have you built games prior to this bounty request?
- **If yes,** *please list game name(s) & links:*

Yes, as listed below:

- **FlappyTips 2**
  * [Functional Demo](https://youtu.be/UhEuqTKF6aA)
  * [Open-source code](https://github.com/ltfschoen/flappytips)
  * Date: Feb-Mar 2023
  * **Objective**: Fly the DOT character between more gaps (of obstacles blocks) than all other opponents to win the game of that starting block on the Zeitgeist chain.
  * **Economics**: Players may choose to play without using any funds. However, incentives exist that require tokens, where users may create a Substrate-based account and deposit sufficient tokens (DOT tokens) to cover the transaction costs required to share their game results. If the user plays the game and shares their results, they may be eligible for a tip from the treasury.
  * **Features:**
    <details>
      <summary>Click here to show</summary>

      * Restricted gameplay endpoint of only Zeitgeist to use their block time for ease of integration with the Zeitgeist prediction markets. Future releases may restore choice of chain
      * Support for multiplayer using Websockets (FlappyTips 2) instead of just single player games (FlappyTips 1). If no other opponents connect in time. Once the user selects a Polkadot.js Extension account to play with and clicks "Play" it schedules a game at a future block. Other players may join if they also click "Play" a sufficient amount of blocks before the game starts, otherwise they are scheduled to play at a future block, where other players can join too.
      * Support to show ghost icon of other players during gameplay
      * Support to track the start block and end block of the game after all players have hit an obstacle
      * Gameplay success factor where players may only Win in multiplayer. Single player games or draws are shown as losing
      * IP address recording only incase necessary to block malicious users in production.
      * Created an ink! Smart Contract to generate source of randomness using Moonbeam network randomness precompiles and Chainlink VRFs [here](https://github.com/ltfschoen/XCMTemplate/tree/main/dapps/evm2/randomness) since randomness precompiles could not be gamed.
      * Created XCM ink! Smart contracts to generate source of randomness from a future block hash to overcome randomness precompiles that could be gamed [here](https://github.com/ltfschoen/XCMTemplate/tree/main/dapps/xcm/unnamed)
    </details>
  * **Research** 
    * Investigated using Astar network zkSNARK circuits for game proofs that are available in their [plonk pallet](https://github.com/AstarNetwork/plonk) that was [funded through W3F grants](https://github.com/w3f/Grants-Program/pull/454#issuecomment-993621915) that may be added to the CLAWBIRD CHAOS core.
  * **Technology**
    * Polkadot.js API, Polkadot Extension, ink!, Express API, P5 Gaming API, React, Node.js 19, Yarn 3, Websockets, Docker

- **FlappyTips 1**
  * [Open-source code](https://github.com/ltfschoen/flappytips/releases)
  * Date: Jun-Jul 2020
  * **Features:**

    <details>
      <summary>Click here to show</summary>

      * Choice of supported chains (i.e. Polkadot, Kusama, Edgeware).
      * Player character is a DOT icon (similar to Flappy Bird)
      * Players may click a Tweet button after the game to share their results on Twitter
      * Polkadot.js Extension is integrated when playing on Desktop, otherwise user needs to enter their private key to share their result (until FlappyTips supports account QR code scanning)
      * Responsive with support for mobile devices or desktop
      * Press Spacebar multiple times to fly the DOT on desktop
      * Touch the screen multiple times to fly the DOT on mobile devices
      * Blocks appear each time a new block is authored on your chosen chain. The chain must support treasury.reportAwesome
      * After each block appears, the speed that it moves increases each time.
      * After about 10 blocks the gap may becomes larger but it still becomes more difficult as the blocks move faster
      * If you click "Share your awesomeness?" button after each game and enter your "Mnemonic Seed" (Mobile) or select an account injected by Polkadot.js Extension (Desktop) that corresponds to the chain that you chose to connected to in the game, along with an optional identifer (i.e. your Twitter handle), it then will submit an extrinsic to the chain that will report your awesomeness for clearing some blocks as a Tip, and should appear in the "Tip" section of the Polkadot Treasury here https://polkadot.js.org/apps/#/treasury.
      * ink! Smart Contract for Leaderboard
      * Game deployed to Sia Skynet IPFS hash using Skynet SDK with redirection to a Handshake decentralised domain name using the Namebase API where Handshake DNS settings configured https://siasky.net/hns/flappy
      * Sia network endpoint with blocks info from Sia Stats and estimated next block and scoring for partial blocks
      * Script to interact with Handshake API to watch a domain name auction and place hidden bid during blocks just before reveal depending on congestion
      * Script to decode DNS info from Namebase API
      * Supports CORS and Express API to host on Heroku
    </details>

  * **Technology**
    * Polkadot.js API, Polkadot Extension, ink!, Express API, P5 Gaming API, React, Node.js 10, Yarn 1.

- **FriendRecall Game Portal**
  * [Functional Demo](https://youtu.be/-WC8WSwFvD4)
  * Date: Feb 2016
  * **Technology:**
    * 3D game environment developed for Apple iOS devices using Xcode with the Swift and Objective-C languages
    * SceneKit (3D game engine)
    * Facebook SDK Login
    * iAds (iOS Ads for app monetisation)
    * iCloud and Local User Defaults (persisting user game state across devices) 

- **Paddle Tree Game**
  * [Functional Demo](https://youtu.be/RjGY3d_2ewI)
  * Date: Sept 2014
  * **About**
    * Adapted from a Lynda.com Tutorial
    * Demonstration using iPhone Simulator
    * Find out how easy it was to develop at [this link](http://lukeschoen.blogspot.com/2014/06/ios-sprite-kit-game-launched.html) 

### Do any of the previously mentioned games have a Web3 component?
- **If yes,** *please describe the Web3 components, link reference & blockchain ecosystem:*

Yes, as listed below:

- **FlappyTips 2**
  * **Web3 components**
    * **Technology**
      * Polkadot.js API, Polkadot Extension, ink!
    * **Features**
      * Created an ink! Smart Contract to generate source of randomness using Moonbeam network randomness precompiles and Chainlink VRFs [here](https://github.com/ltfschoen/XCMTemplate/tree/main/dapps/evm2/randomness) since randomness precompiles could not be gamed.
      * Created XCM ink! Smart contracts to generate source of randomness from a future block hash to overcome randomness precompiles that could be gamed [here](https://github.com/ltfschoen/XCMTemplate/tree/main/dapps/xcm/unnamed)
  * **Link Reference**
    * [ink! Randomness Smart Contract](https://github.com/ltfschoen/XCMTemplate/tree/main/dapps/evm2/randomness)
    * [Zeitgeist integration scripts](https://github.com/ltfschoen/flappytips/tree/master/scripts)
  * **Blockchain ecosystems**
    * Zeitgeist, Moonbeam

- **FlappyTips 1**
  * **Web3 components**
    * **Technology**
      * Polkadot.js API, Polkadot Extension
    * **Features**
      * Integrates with the Polkadot.js Extension
      * Blocks appear each time a new block is authored on your chosen chain. The chain must support treasury.reportAwesome
      * If you click "Share your awesomeness?" button after each game and enter your "Mnemonic Seed" (Mobile) or select an account injected by Polkadot.js Extension (Desktop) that corresponds to the chain that you chose to connected to in the game, along with an optional identifer (i.e. your Twitter handle), it then will submit an extrinsic to the chain that will report your awesomeness for clearing some blocks as a Tip, and should appear in the "Tip" section of the Polkadot Treasury here https://polkadot.js.org/apps/#/treasury.
      * Game deployed to Sia Skynet IPFS hash using Skynet SDK with redirection to a Handshake decentralised domain name using the Namebase API where Handshake DNS settings configured https://siasky.net/hns/flappy
      * Sia network endpoint with blocks info from Sia Stats and estimated next block and scoring for partial blocks
      * Script to interact with Handshake API to watch a domain name auction and place hidden bid during blocks just before reveal depending on congestion
      * Script to Decode DNS info from Namebase API
  * **Link Reference**
    * [ink! Leaderboard Smart Contract](https://github.com/ltfschoen/flappytips/blob/master/ink/contracts/leaderboard/lib.rs)
  * **Blockchain ecosystems**
    * Polkadot, Kusama, Edgeware, Sia, Handshake, Namebase

### Do you have experience in working with game engines, such as Unity & Unreal?
- **If yes,** *please include some insights:*

Yes, I built an experimental Unity game that was not released. I wrote this [blogpost](https://lukeschoen.blogspot.com/2015/07/unity-5.html) summarising the key takeaways from course "Unity 5 3D Essential Training by Adam Crespi" when I first studied Unity 3D 5 and Unity C# Scripting  

## 3. Technical Expertise

### How much of your game logic do you intend to build on the blockchain?
- [ ] None, I just want a token.
- [ ] Only the Game Assets/NFTs should remain on-chain.
- [ ] Some mechanics will need to be on-chain.
- [X] This should be a fully on-chain game.
- [ ] Other: 

### Do you have any expertise in Blockchain Development?
- [ ] No, none at all.
- [ ] I know how the Blockchain works, but never developed anything in crypto.
- [X] I have EVM / SmartContract experience.
- [ ] I have only used SDK for my games on other platforms.
- [X] I know Rust & Substrate and can create basic runtime code.
- [X] Other: Experienced in Rust & Substrate having built and launched the [DataHighway parachain](https://github.com/DataHighway-DHX) on Kusama.

### Would you like a technical Team from Polkadot Play, to help you identify the technical requirements?
- **If yes,** please describe what you consider your major pain points.

YES, we are currently creating the GDG.

## 4. The Team

### Could you share insights about team members who are essential to your project's success? Highlight their specific skill sets and contributions to the game development. 

#### Team member #1

Luke Schoen is the lead game developer of the CLAWBIRD CHAOS game using Unity and the [Polkadot Unity SDK](https://github.com/PolkadotPlay/Polkadot.Unity.SDK/wiki) and [Substrate .NET API](https://github.com/SubstrateGaming/Substrate.NET.API). He has over 5 years of experience in the Polkadot and Ethereum ecosystems. He was a Top 5% Substrate and Polkadot Beta contributor on Stack Exchange in 2023. He studied Encode zkEVM Bootcamp Dec-Jan 2023 and the Encode ZK Bootcamp Oct-Nov 2023. He participated in Ethereum Protocol Fellowship (EPF) Cohort 4 from July-Nov 2023. He achieved a High Credit in online Rust exam qualifier associated with the Polkadot Blockchain Academy in 2023. He built and deployed DataHighway parachain on Kusama network in 2022. He was a front-end Developer of Polkadot.js in 2018-2019. He was a teaching Assistant at Coder Academy bootcamp in 2018. He also has experience with machine learning and AI.

#### Team member #2

Claudia Lucero shall provide administrative support to the game developers.

### Team Code Repos

* [Clawbird](https://github.com/clawbird)
* [Luke Schoen](https://github.com/ltfschoen)

### Team LinkedIn Profiles (if available)

* [Luke Schoen](https://www.linkedin.com/in/ltfschoen/)

## 5. Development

### Development Status :open_book:
If you've already started implementing your project or it is part of a larger repository, please provide a link and a description of the code here.
> **Example** ...

> **TODO**: Update this section

### What are the key milestones for your game's development, and what are the estimated completion dates for each?
- **Milestone 1:**
- **Milestone 2:**
- **Milestone 3:**

> **TODO**: Update this section

### Are you intending to raise more funds?
- **If yes,** please describe what you expect to be the full amount needed to finalize the product.

> **TODO**: Update this section

## 6. Detailed Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**. In the descriptions, it should be clear how your game project is related to Substrate, Kusama, Polkadot, or a (System-)Parachain. We *recommend* that teams structure their roadmap as 1 milestone ≈ 1 month.

> **TODO**: Update this section

### Overview

- **Total Estimated Duration:** 360 months
- **Full-Time Equivalent (FTE):** 0.1 FTE
- **Total Costs:** 32,500 DOT

> **TODO**: Update this section. Initial costs higher than maintenance costs.

### Milestone 1 - Phase 1 of 4 of Basic Functionality

- **Estimated duration:** 1 month
- **FTE:**  0.25
- **Costs:** 225 DOT

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. Examples of steps are shown in 1 - 8.

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Specify the IP owning entity; ensure proper copyright compliance for all reused materials, including appropriate licenses and attributions, or choose an open-source license (Apache 2.0, GPLv3, MIT, Unlicense). |
| **0b.** | Documentation | Provide comprehensive **inline documentation** of the code and a detailed **tutorial**. The tutorial should guide users on how to set up, play the game, and assess the milestone's deliverables, ensuring functionality and compliance with the milestone objectives. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Platform | Provide a detailed description of the game's platform compatibility and the infrastructure setup required to host and run the game, including supported operating systems, hardware requirements, and necessary backend services. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the games bounty). (Content, language, and medium should reflect your target audience described above.) |

| 1. | Backend module: CLAWBIRD CHAOS BE | We will create a Substrate module that will provide the following functionality: **TODO** |
| 2. | Frontend module: CLAWBIRD CHAOS FE | We will create a frontend (Unity) that will  provide essential parts including the following: **TODO** |
| 3. | Asset Layer: CLAWBIRD CHAOS AL | We will create an asset layer consisting of the concept and data models of our game assets models: **TODO** |
| 4. | Substrate chain: CLAWBIRD CHAOS SS | Modules of our custom chain will interact: **TODO** |
| 5. | Library: CLAWBIRD CHAOS LIB | We will deliver a JS library that will implement the functionality: **TODO** |
| 6. | Smart contracts: CLAWBIRD CHAOS SC | We will deliver a set of ink! smart contracts that will: **TODO**
| 7. | GDD: CLAWBIRD CHAOS GDD | We will create an comprehensive Game Design Document (GDD) including the core game loop and the game narrative |
| 8. | BSA: CLAWBIRD CHAOS BSA | We will create an Blockchain Solution Architecture (BSA) showing the proper interaction of the game with the Blockchain elements |

> **TODO**: Update this section

### Milestone 2 Example — Additional features

> **TODO**: Update this section

## 7. Future Plans

Please include here

- how you intend to finance the project's long-term maintenance and development,
- how you intend to use, enhance, and promote your project in the short term, and
- the team's long-term plans and intentions in relation to it.

- **Long-Term Maintenance and Development Funding:**
  * Web3 social connection fees

> **TODO**: Update this section with more information

- **Short-Term Usage, Enhancement, and Promotion:**
  * Grillchat via [https://grillapp.net/@chaos](https://grillapp.net/@chaos)
  * Twitter via [@ltfschoen](https://twitter.com/ltfschoen)
  * Twitter via [@ClawbirdDAO](https://twitter.com/ClawbirdDAO)

- **Long-term plans and intentions**
  * Autonomous self-sustainable on-chain game

## 8. Additional Information :heavy_plus_sign:

### While we've covered a range of topics, there might still be questions or areas of uncertainty on your side or ours. We encourage you to share any additional thoughts, questions, or concerns you may have, with us.

### How did you hear about the Grants Program?
- [ ] Polkadot Play Website
- [ ] Twitter
- [ ] Medium
- [ ] Personal recommendation
- [X] Other: Telegram (via Hope Clary in Polkadot Strategy > Ideas)
