# Robox.fi

Robox.fi is the first escrow-less NFT leveraged trading platform on Solana. The platform consolidates NFT listings from various marketplaces, providing easy browsing and enabling traders to trade NFTs at a fraction of their price.

[Robox.fi](http://Robox.fi) seeks to revolutionize the NFT market by creating a user-friendly and secure trading platform that provides equal opportunities to investors and traders to access high-value NFTs.

The platform is designed to democratize the NFT market by:

- Making it more accessible and liquid, allowing for easier buying and selling of NFTs.
- Allowing users to trade NFTs with leverage while taking into account their unique needs and risk tolerance, addressing the low liquidity and risk aversion challenges faced by NFT traders.

Ultimately, [Robox.fi](http://robox.fi/) aims to become the go-to platform for NFT trading, offering advanced leverages and trading mechanics while maintaining a focus on simplicity and usability.

## Key Features
* Buy NFTs from Hadeswap with leverage
* Customizable down payment and duration
* NFTs are frozen in the user's wallet until repayment
* Ability to sell NFTs instantly via Hadeswap AMM
* Liquidation options include margin call or expiration
* Internal liquidity pool available
* Loan repayment

## Architecture Overview
The Robox.fi app consists of three main components: client, server, and contract.

![image](https://github.com/robox-fi/.github-private/blob/main/robox_architecture.jpg)

## Repositories
[Backend APIs](https://github.com/robox-fi/users_positions_API) - Internal APIs that are used for CRUD of Users and Positions data.

Tech Stack: NodeJS, ExpressJS, Anchor, MongoDB, Repl.it

[Solana Program](https://github.com/robox-fi/bnpl-contract) - The core component that allows to buy/sell/liquidate/list NFTs on-chain using cross program invocations (CPIs).

Tech Stack: Rust, Anchor

[Frontend](https://github.com/robox-fi/robox-fi-web) - The main frontend app that connects all the components together. It allows users to browse collections, buy NFTs with leverage, sell/list them and track stats. 

Tech Stack: Typescript, Anchor, Vercel

[Liquidation backend](https://github.com/robox-fi/liquidation-tracker) - This component is running on the backend in real-time and tracks Floor Price and Duration for each active leveraged position. If the FP drops to liquidation price or duration experices - NFT is automatically sold on Hadeswap AMM (Later on we will have other liquidation options in order to mitigate risks of cascade liquidations)

Tech Stack: NodeJS, Mongodb
## Links

Site: https://robox-fi-web.vercel.app/

Twitter: https://twitter.com/robox_fi


