⭐ AfiaPass — The Logistics Trust Engine

AfiaPass is a decentralized middleware infrastructure designed to solve the Nigerian logistics crisis—specifically the "Checkpoint Problem" and multiple taxation. Built on the Stellar blockchain, it enables any application to issue unforgeable, on-chain digital transit permits that programmatically split levies between government and union wallets in real-time.

By leveraging Soroban smart contracts, AfiaPass transforms every delivery into a verifiable, auditable transaction, reducing friction for riders and ensuring transparency for revenue agencies. 🔑 Quick Summary 🌐 What AfiaPass Solves

Logistics in Nigeria (like your Drive-Thru Afia project) currently suffers from systemic bottlenecks that code can finally address:

✅ Illegal/Multiple Taxation: Automates a "Single Point of Payment" that splits funds to all relevant tiers (LGA, State, Union) via smart contract.

✅ Checkpoint Harassment: Provides riders with a verifiable digital "Pass" that can be validated by road officials instantly.

✅ Revenue Leakage: Ensures taxes reach the correct government wallets instead of "informal" collectors.

✅ Offline Dead-Zones: Uses signed JWTs to allow verification even where there is zero internet connectivity.

🚀 Core Architecture

AfiaPass uses a Hexagonal Architecture to bridge Web2 logistics apps with Web3 trust.

    The Core (Domain)

Contains the "Laws of the Road"—business logic defining when a permit is valid, how long it lasts, and which LGAs are covered. 2. The Ports (Interfaces)

Defines how the SDK talks to the outside world.

BlockchainProvider: Interface for interacting with Stellar.

PermitIssuer: Interface for the permit generation engine.

    The Adapters (Infrastructure)

    Stellar/Soroban Adapter: Uses Java 21 Virtual Threads to broadcast transactions to Stellar nodes with automatic failover.

    Offline Signer: Generates SEP-10 compliant signatures for QR codes.

🏗️ Project Structure

Within TheTwoHorsemen organization, the project is split into three main repositories: 🧭 How AfiaPass Works

Payment Request: An app (e.g., Drive-Thru Afia) calls afiaPass.issuePermit().

Smart Split: The Soroban contract receives NGNC (Naira Stablecoin) and instantly routes:

    5% to Local Govt Wallet

    5% to Transport Union Wallet

    90% to the Logistics Operator

Digital Receipt: The SDK returns a Signed QR Code to the rider's phone.

Instant Verification: An official scans the QR code; their app verifies the signature against the AfiaPass Public Key without needing internet.

🛠️ Tech Stack ⚡ Getting Started (For Java Developers) Prerequisites

JDK 21

Maven

Stellar Testnet Account

Installation

Add the repository to your pom.xml: 🌍 Use Cases

Food Delivery: Protect your DailyDrop riders from arbitrary "levies" on the road.

Haulage: Allow interstate trucks to pay a "Harmonized Transit Fee" once.

State Revenue: Provide a transparent digital channel for Local Governments to collect transport taxes.

