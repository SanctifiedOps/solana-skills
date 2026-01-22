# Solana Cheatsheets

Quick reference commands and snippets. Copy-paste and ship.

---

## SPL Token CLI

### Create Token (Legacy)
```bash
# Create new token with 6 decimals
spl-token create-token --decimals 6

# Create with specific keypair
spl-token create-token --decimals 6 --mint-authority <KEYPAIR_PATH>
```

### Create Token Account
```bash
# Create associated token account for yourself
spl-token create-account <MINT_ADDRESS>

# Create for another wallet
spl-token create-account <MINT_ADDRESS> --owner <WALLET_ADDRESS>
```

### Mint Tokens
```bash
# Mint to your ATA
spl-token mint <MINT_ADDRESS> <AMOUNT>

# Mint to specific account
spl-token mint <MINT_ADDRESS> <AMOUNT> <TOKEN_ACCOUNT>
```

### Check Balances
```bash
# All token balances
spl-token accounts

# Specific token
spl-token balance <MINT_ADDRESS>

# Account info
spl-token account-info <TOKEN_ACCOUNT>
```

### Authority Management
```bash
# View current authorities
spl-token display <MINT_ADDRESS>

# Revoke mint authority (permanent!)
spl-token authorize <MINT_ADDRESS> mint --disable

# Revoke freeze authority
spl-token authorize <MINT_ADDRESS> freeze --disable

# Transfer mint authority
spl-token authorize <MINT_ADDRESS> mint <NEW_AUTHORITY>
```

### Transfer
```bash
# Transfer tokens
spl-token transfer <MINT_ADDRESS> <AMOUNT> <RECIPIENT_WALLET>

# Transfer all
spl-token transfer <MINT_ADDRESS> ALL <RECIPIENT_WALLET>
```

---

## Anchor CLI

### Project Setup
```bash
# Create new project
anchor init <PROJECT_NAME>

# Build
anchor build

# Test
anchor test

# Test on specific cluster
anchor test --provider.cluster devnet
```

### Deployment
```bash
# Deploy to devnet
anchor deploy --provider.cluster devnet

# Deploy to mainnet
anchor deploy --provider.cluster mainnet

# Upgrade existing program
anchor upgrade target/deploy/<PROGRAM>.so --program-id <PROGRAM_ID>
```

### Keys and IDs
```bash
# Get program ID from keypair
solana-keygen pubkey target/deploy/<PROGRAM>-keypair.json

# Generate new keypair
solana-keygen new -o <OUTPUT_PATH>
```

### IDL
```bash
# Generate IDL
anchor idl init <PROGRAM_ID> --filepath target/idl/<PROGRAM>.json

# Upgrade IDL
anchor idl upgrade <PROGRAM_ID> --filepath target/idl/<PROGRAM>.json

# Fetch IDL
anchor idl fetch <PROGRAM_ID>
```

---

## Solana CLI

### Cluster Configuration
```bash
# Check current cluster
solana config get

# Set to devnet
solana config set --url devnet

# Set to mainnet
solana config set --url mainnet-beta

# Use custom RPC
solana config set --url https://your-rpc-endpoint.com
```

### Account Operations
```bash
# Check balance
solana balance

# Check specific address
solana balance <ADDRESS>

# Airdrop (devnet only)
solana airdrop 2

# Transfer SOL
solana transfer <RECIPIENT> <AMOUNT>
```

### Account Info
```bash
# Get account details
solana account <ADDRESS>

# Get account data as JSON
solana account <ADDRESS> --output json

# Check rent exemption
solana rent <DATA_SIZE_BYTES>
```

### Transaction Info
```bash
# Get transaction details
solana confirm -v <SIGNATURE>

# Watch for confirmation
solana confirm <SIGNATURE> --commitment finalized
```

---

## RPC Endpoints

### Public (Free, Rate Limited)
```
Mainnet: https://api.mainnet-beta.solana.com
Devnet:  https://api.devnet.solana.com
Testnet: https://api.testnet.solana.com
```

### Providers (Require API Key)
```
Helius:     https://mainnet.helius-rpc.com/?api-key=<KEY>
QuickNode:  https://your-endpoint.quiknode.pro/<KEY>
Alchemy:    https://solana-mainnet.g.alchemy.com/v2/<KEY>
Triton:     https://your-pool.triton.one/?access-token=<KEY>
```

### Jito (Bundles)
```
Block Engine: https://mainnet.block-engine.jito.wtf
NY:           https://ny.mainnet.block-engine.jito.wtf
Amsterdam:    https://amsterdam.mainnet.block-engine.jito.wtf
Frankfurt:    https://frankfurt.mainnet.block-engine.jito.wtf
Tokyo:        https://tokyo.mainnet.block-engine.jito.wtf
```

---

## Jupiter API

### Get Quote
```bash
curl "https://quote-api.jup.ag/v6/quote?\
inputMint=So11111111111111111111111111111111111111112&\
outputMint=EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v&\
amount=1000000000&\
slippageBps=50"
```

### Get Swap Transaction
```bash
curl -X POST "https://quote-api.jup.ag/v6/swap" \
  -H "Content-Type: application/json" \
  -d '{
    "quoteResponse": <QUOTE_FROM_ABOVE>,
    "userPublicKey": "<YOUR_WALLET>",
    "wrapAndUnwrapSol": true
  }'
```

### Get Token Price
```bash
curl "https://price.jup.ag/v6/price?ids=SOL,USDC,BONK"
```

---

## Helius DAS API

### Get Assets by Owner
```bash
curl https://mainnet.helius-rpc.com/?api-key=<KEY> \
  -X POST \
  -H "Content-Type: application/json" \
  -d '{
    "jsonrpc": "2.0",
    "id": "1",
    "method": "getAssetsByOwner",
    "params": {
      "ownerAddress": "<WALLET>",
      "page": 1,
      "limit": 100
    }
  }'
```

### Get Asset
```bash
curl https://mainnet.helius-rpc.com/?api-key=<KEY> \
  -X POST \
  -H "Content-Type: application/json" \
  -d '{
    "jsonrpc": "2.0",
    "id": "1",
    "method": "getAsset",
    "params": {
      "id": "<ASSET_ID>"
    }
  }'
```

### Get Asset Proof (for cNFT transfers)
```bash
curl https://mainnet.helius-rpc.com/?api-key=<KEY> \
  -X POST \
  -H "Content-Type: application/json" \
  -d '{
    "jsonrpc": "2.0",
    "id": "1",
    "method": "getAssetProof",
    "params": {
      "id": "<ASSET_ID>"
    }
  }'
```

---

## Common Program IDs

```typescript
// System
const SYSTEM_PROGRAM = '11111111111111111111111111111111';
const TOKEN_PROGRAM = 'TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA';
const TOKEN_2022_PROGRAM = 'TokenzQdBNbLqP5VEhdkAS6EPFLC1PHnBqCXEpPxuEb';
const ASSOCIATED_TOKEN_PROGRAM = 'ATokenGPvbdGVxr1b2hvZbsiqW5xWH25efTNsLJA8knL';
const RENT = 'SysvarRent111111111111111111111111111111111';

// Metaplex
const METADATA_PROGRAM = 'metaqbxxUerdq28cj1RbAWkYQm3ybzjb6a8bt518x1s';
const BUBBLEGUM = 'BGUMAp9Gq7iTEuizy4pqaxsTyUCBK68MDfK752saRPUY';

// DeFi
const JUPITER_V6 = 'JUP6LkbZbjS1jKKwapdHNy74zcZ3tLUZoi5QNyVTaV4';
const RAYDIUM_AMM = '675kPX9MHTjS2zt1qfr1NYHuzeLXfQM9H24wFSUt1Mp8';
const ORCA_WHIRLPOOL = 'whirLbMiicVdio4qvUfM5KAg6Ct8VwpYzGff3uctyCc';

// Infrastructure
const COMPUTE_BUDGET = 'ComputeBudget111111111111111111111111111111';
const MEMO = 'MemoSq4gqABAXKb96qnH8TysNcWxMyWCqXgDLGmfcHr';
```

---

## TypeScript Snippets

### Connect to RPC
```typescript
import { Connection, clusterApiUrl } from '@solana/web3.js';

const connection = new Connection(
  clusterApiUrl('mainnet-beta'), // or custom RPC
  'confirmed'
);
```

### Load Keypair
```typescript
import { Keypair } from '@solana/web3.js';
import fs from 'fs';

// From file
const keypair = Keypair.fromSecretKey(
  Uint8Array.from(JSON.parse(fs.readFileSync('~/.config/solana/id.json', 'utf-8')))
);

// From base58
import bs58 from 'bs58';
const keypair = Keypair.fromSecretKey(bs58.decode('<BASE58_PRIVATE_KEY>'));
```

### Get Balance
```typescript
const balance = await connection.getBalance(publicKey);
console.log(`Balance: ${balance / 1e9} SOL`);
```

### Add Priority Fee
```typescript
import { ComputeBudgetProgram, Transaction } from '@solana/web3.js';

const tx = new Transaction();
tx.add(ComputeBudgetProgram.setComputeUnitLimit({ units: 200_000 }));
tx.add(ComputeBudgetProgram.setComputeUnitPrice({ microLamports: 10_000 }));
// Add your instructions after
```

### Send Transaction with Retry
```typescript
async function sendWithRetry(
  connection: Connection,
  transaction: Transaction,
  signers: Keypair[],
  maxRetries = 3
): Promise<string> {
  let signature: string;
  for (let i = 0; i < maxRetries; i++) {
    try {
      const { blockhash } = await connection.getLatestBlockhash();
      transaction.recentBlockhash = blockhash;
      transaction.sign(...signers);

      signature = await connection.sendRawTransaction(transaction.serialize(), {
        skipPreflight: false,
        maxRetries: 0,
      });

      await connection.confirmTransaction(signature, 'confirmed');
      return signature;
    } catch (e) {
      if (i === maxRetries - 1) throw e;
      await new Promise(r => setTimeout(r, 1000 * (i + 1)));
    }
  }
  throw new Error('Max retries exceeded');
}
```

---

## Useful Addresses

### Burn Addresses
```
1nc1nerator11111111111111111111111111111111
1111111111111111111111111111111111111111111
```

### Jito Tip Accounts
```
96gYZGLnJYVFmbjzopPSU6QiEV5fGqZNyN9nmNhvrZU5
HFqU5x63VTqvQss8hp11i4wVV8bD44PvwucfZ2bU7gRe
Cw8CFyM9FkoMi7K7Crf6HNQqf4uEMzpKw6QNghXLvLkY
ADaUMid9yfUytqMBgopwjb2DTLSokTSzL1zt6iGPaS49
DfXygSm4jCyNCybVYYK6DwvWqjKee8pbDmJGcLWNDXjh
ADuUkR4vqLUMWXxW9gh6D6L8pMSawimctcNZ5pGwDcEt
DttWaMuVvTiduZRnguLF7jNxTgiMBZ1hyAumKUiL2KRL
3AVi9Tg9Uo68tJfuvoKvqKNWKkC5wPdSSdeBnizKZ6jT
```

### Common Tokens
```
SOL:  So11111111111111111111111111111111111111112
USDC: EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v
USDT: Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB
BONK: DezXAZ8z7PnrnRJjz3wXBoRgixCa6xjnB7YaB1pPB263
WIF:  EKpQGSJtjMFqKZ9KQanSqYXRcF8fBopzLHYxdM65zcjm
JUP:  JUPyiwrYJFskUPiHa7hkeR8VUtAeFoSYbKedZNsDvCN
```

---

## Quick Debugging

### Check Transaction Status
```bash
solana confirm -v <SIGNATURE>
```

### Decode Transaction
```bash
# Use Solscan or Solana FM
https://solscan.io/tx/<SIGNATURE>
https://solana.fm/tx/<SIGNATURE>
```

### Check Account Owner
```bash
solana account <ADDRESS> | grep "Owner"
```

### Get Rent Exemption
```bash
# For N bytes of data
solana rent <BYTES>
```

### Estimate Priority Fee
```typescript
const recentFees = await connection.getRecentPrioritizationFees();
const median = recentFees
  .map(f => f.prioritizationFee)
  .sort((a, b) => a - b)[Math.floor(recentFees.length / 2)];
console.log(`Median priority fee: ${median} micro-lamports`);
```

---

Built for builders. Ship fast.
