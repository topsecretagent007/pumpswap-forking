# 🚀 PumpSwap Fork

PumpSwap Fork is a powerful SDK built to enable seamless interaction with the Pump.fun swap page, using Jito.
Written in TypeScript, it offers essential functions like buying/selling tokens, fetching token prices, and accessing liquidity pool data — all tailored for developers working within the PumpSwap ecosystem.

## 📬 Contact

Need help or want a custom bot developed?
Reach out on: [Telegram](https://t.me/topsecretagent_007)  |  [Twitter](https://x.com/lendon1114)

## 📚 Features

- **🔄 Buy/Sell Tokens:** Perform token swaps using specific parameters with bundle.

- **💰 Fetch Token Prices:** Retrieve the current price of tokens with a single function.

- **🏊‍♂️ Access PumpSwap Pools:** Fetch pool details for specific tokens.

- **⚙️ Customizable Environment:** Easily configure private keys and RPC keys.

## 🛠️ Usage

### ✅ Buy/Sell Tokens on PumpSwap
```typescript
import {wallet_1} from "./constants";
import {PumpSwapSDK} from './pumpswap';
async function main() {
    const mint = "your-pumpfun-token-address";
    const sol_amt = 0.99; // buy 1 SOL worth of token using WSOL
    const sell_percentage = 0.5; // sell 50% of the token
    const pumpswap_sdk = new PumpSwapSDK();
    await pumpswap_sdk.buy(new PublicKey(mint), wallet_1.publicKey, sol_amt); // 0.99 sol
    await pumpswap_sdk.sell_percentage(new PublicKey(mint), wallet_1.publicKey, sell_percentage);
    await pumpswap_sdk.sell_exactAmount(new PublicKey(mint), wallet_1.publicKey, 1000); // 1000 token
}
```

### 📈 Fetch Token Price
```typescript
import {getPrice} from './pool';
async function main() {
    const mint = new PublicKey("your-pumpfun-token-address");   
    console.log(await getPrice(mint));
}
```

### 💧 Fetch PumpSwap Pool Info
```typescript
import {getPumpSwapPool} from './pool';
async function main() {
    const mint = new PublicKey("your-pumpfun-token-address");   
    console.log(await getPumpSwapPool(mint));
}
```

Let me know if you'd like me to add:

- Environment setup instructions

- A full example with .env configuration

- CLI usage (if supported)

- Badges (e.g., version, license)

Happy shipping 🚢




