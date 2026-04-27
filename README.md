# Roll4Sol: Decentralized Peer-to-Peer Dice 🎲

Roll4Sol is a high-performance, decentralized gaming protocol built on the **Solana** blockchain. Unlike traditional online casinos, Roll4Sol uses an on-chain, trustless vault system where players duel directly against each other. No house, no hidden logic—just pure code.



## 🚀 Key Features

* **Self-Custody & Autonomy:** Players retain full control of their funds. If a game hasn't started, the creator can reclaim their SOL instantly via the smart contract.
* **Provably Fair:** Outcomes are determined by a transparent on-chain hashing protocol, ensuring results are auditable and tamper-proof.
* **Instant Settlement:** Winners receive payouts automatically through the smart contract the moment the roll is revealed.
* **Early Bird Promotion:** Genesis players enjoy a reduced **5% sustainability fee**, supporting the platform's RPC and hosting infrastructure.

---

## 🛠 Technical Stack

* **Smart Contract:** Developed with the **Anchor Framework** (Rust).
* **Frontend:** React, TypeScript, and Tailwind CSS.
* **State Management:** Real-time synchronization via **Solana Wallet Adapter**.
* **Backend Cache:** **RedisJSON** for high-speed game indexing and metadata fetching.
* **Infrastructure:** Private **Helius/Alchemy RPC** nodes for 403-resistant, high-uptime connectivity.

---

## 📦 Getting Started

### Prerequisites
* Node.js (v18+)
* Solana CLI & Anchor (for contract development)
* A Solana Wallet (Phantom, Solflare, etc.)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/roll4sol.git
   cd roll4sol
   ```

2. **Install dependencies:**
   ```bash
   # Install Web dependencies
   npm install

   # Install Backend dependencies
   cd server && npm install
   ```

3. **Environment Setup:**
   Create a `.env` file in the root and server directories:
   ```env
   SOLANA_RPC_URL=https://mainnet.helius-rpc.com/?api-key=YOUR_KEY
   REDIS_URL=redis://localhost:6379
   ```

4. **Run the App:**
   ```bash
   npm run dev
   ```

---

## 🏗 Program Logic

The game flows through a secure state machine within the Solana program:

1.  **Initialize:** Creator locks SOL into a Program Derived Address (PDA) vault.
2.  **Join:** Opponent matches the bet and joins the session.
3.  **Play/Reveal:** Cryptographic seeds from both transactions are hashed on-chain to generate the roll.
4.  **Settle:** The vault releases the total bank (minus the sustainability fee) to the winner's address.

---

## 🛡 Security

* **Auditability:** Every transaction and game result is viewable on Solscan.
* **Anti-Bot:** Integration with Blowfish and Phantom security protocols to ensure a safe user environment.
* **Verified Contract:** The program is deployed on Solana Mainnet-Beta and is fully verifiable.

## 🤝 Community & Support

* **X (Twitter):** [@Roll4Sol](https://x.com/dice_r4s)
* **Discord:** [Join the Community](https://discord.gg/c4qtWDGZYS)
* **Domain:** [game.roll4sol.com](https://game.roll4sol.com)

---

*Disclaimer: Cryptocurrency gaming involves risk. Ensure you are compliant with your local regulations before participating.*
