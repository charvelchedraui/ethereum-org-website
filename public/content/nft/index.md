---
title: Non-fungible tokens (NFT)
metaTitle: What are NFTs? | How they work and their limits
description: "What are NFTs? Learn how non-fungible tokens record ownership on Ethereum, what a token does and does not give you, and the risks to watch for."
lang: en
template: use-cases
sidebarDepth: 2
image: /images/infrastructure_transparent.png
alt: An Eth logo being displayed via hologram.
summaryPoints:
  - "A token standard for issuing and tracking individual items on Ethereum."
  - "The ownership record is onchain. The file the token points to is usually stored elsewhere."
  - "Powered by smart contracts that follow shared standards such as ERC-721 and ERC-1155."
---

## What are NFTs? {#what-are-nfts}

A **non-fungible token (NFT)** is a token with its own identity on Ethereum. A smart contract records an identifier and the address that currently holds it. That differs from ether, where every unit spends the same and you do not care which one is in your wallet. You do care which NFT you hold, because one token does not stand in for another.

People point tokens at art, tickets, collectibles, names, and real-world assets. The holding is public on Ethereum's blockchain. A license, not the token, decides what you may do with the work.

<VideoWatch slug="learn-nfts-and-defi" />

## What does NFT stand for? {#what-does-nft-stand-for}

NFT stands for **non-fungible token**.

Fungible means one unit spends like any other, as a dollar bill does. Non-fungible means this token is not a stand-in for that one. Two tokens can share an artwork, and an edition of identical tickets is still a set of NFTs. The standard does not cap supply. The mint rules do, and you have to read them.

## How do NFTs work? {#how-nfts-work}

A smart contract mints the tokens, records which address holds each ID, and stores a link to metadata. ERC-721 gives each ID one holder. ERC-1155 can issue many copies of one ID, which is how a run of identical tickets usually works. The same standards run on layer 2 networks that settle to Ethereum. Only the holder, or a contract they approved, can transfer the token. The file itself is usually another link inside the metadata.

After the transfer is [finalized](/glossary/#finality), reverting it means destroying more than one third of all staked ether. Finality does not cap the supply or assign the copyright.

### Where is the file stored? {#where-is-the-file-stored}

The media usually sits on the **InterPlanetary File System (IPFS)** or a web server. If the host goes away, the token remains and the file does not.

A 2022 study of OpenSea assets found 88.71% of asset URLs and 80.69% of metadata URLs on ordinary web domains. From June–December 2021, 3.91% of the IPFS images and 9.04% of the IPFS metadata in that set stopped resolving. An IPFS link makes a swapped file detectable. It does not store the bytes for you, and some contracts let the owner change the link later.

## What are NFTs used for? {#nft-use-cases}

People use NFTs for attendance, course certificates, game items, digital art, real-world assets, names such as ENS names, gated content, tickets, and collateral in decentralized finance.

A creator deploys a contract, sets the supply, and attaches a link to the work. Holding a token shows it came from that contract. It does not show the contract is the creator people expect. Copies that reuse a collection's art are common, so match the address to one the creator published.

Tickets can move between wallets without a box office, and the contract can cap the supply. The contract address shows which contract issued the ticket. It does not, by itself, show that the organizer deployed it, and the venue decides whether to accept the token at the door.

ethereum.org has used NFTs to recognize contributors, translators, and call attendees. They are listed on the [collectibles](/collectibles/) page. **Proof of Attendance Protocol (POAP)**, the protocol behind many of them, stopped new issuers on 16-Mar-2026 and on 3-Aug-2026 said the company was winding down. Nearly 7.6 million POAPs remain onchain. The company's website and file hosting may not.

![An ethereum.org POAP, a collectible minted for contributors](./poap.png)

The site's **ethereum.eth** name is a token, registered with the **Ethereum Name Service (ENS)**, unlike the `.org` name. [Check the ENS record](https://app.ens.domains/name/ethereum.eth).

<Alert variant="update">
<AlertEmoji text=":eyes:"/>
<AlertContent className="justify-between flex-row items-center">
  <div>See apps in the collectibles category.</div>
  <ButtonLink href="/apps/categories/collectibles">
    Explore collectibles
  </ButtonLink>
</AlertContent>
</Alert>

## What does owning an NFT give you? {#what-owning-an-nft-gives-you}

You own a record: the contract lists your address, you can transfer the token, and any Ethereum app can see that without an account at one company.

You do not automatically own the copyright. A 12-Mar-2024 report to Congress, from the U.S. Copyright Office and the U.S. Patent and Trademark Office, says transferring an NFT transfers the token, not the copyright. A separate agreement licenses or assigns those rights. The contract can point at those terms. Whether code alone meets the signed-writing rule is unsettled.

An app can check what you hold. A song, a game item, or entry to an event still depends on the license, and on that app choosing to honor it. An NFT is not a music file that plays in every app.

## How do NFTs compare with a platform account? {#nft-comparison}

| An NFT | A typical platform account |
| --- | --- |
| **You hold the token.** Only you can transfer it. The file usually lives offchain. | **The platform holds the account** and can close it. |
| **Other apps can read what you hold.** | Each company runs a closed system. |
| **You can list a token wherever the standard is supported.** A few marketplaces handle most of the volume, each with its own rules, fees, and regional limits. | Creators depend on one platform's terms and country rules. |
| **A creator can publish a royalty rate.** Since 2023, major marketplaces have treated it as optional. | The platform sets the revenue split and can change it. |

## Where do NFTs stand today? {#where-nfts-stand-today}

DappRadar put 2021 volume above $23 billion. Reuters, citing DappRadar, reported about $25 billion of sales that year. For 2025, DappRadar reported $867 million in the second quarter, down 45% from the previous quarter. Other write-ups of that release say about $823 million. The third quarter was $1.58 billion across 18.1 million sales. Dollar volume fell much harder than the number of sales. Totals cover many chains and include wash trades. This page quotes no 2026 figure, because DappRadar had not published a quarterly report for that year.

## What are the limits? {#nft-limits}

### Royalties are not automatic {#royalties}

ERC-2981 lets a creator publish a rate, for example 5% of a resale, and the address that should receive it. Marketplaces can read that value. The transfer itself does not collect the fee, and the recipient is not automatically the contract owner.

On 17-Aug-2023 OpenSea made fees on new collections optional from 31-Aug-2023, and ended enforcement for filtered collections on 29-Feb-2024. Other large marketplaces had already dropped required fees or cut them. A contract can block transfers that skip a paying venue. Those tokens trade only where that block is supported.

### The copyright stays with the creator {#copyright}

Anyone can mint a token that points at art they do not own. The chain records who deployed the contract. It does not check the copyright. Copying or selling the work still needs a license.

### The file can disappear {#file-permanence}

A dead host can leave a blank image on a token you still own. An editable link can change the picture after the sale. Content addressing shows the swap. It does not keep the file online.

### Energy use after The Merge {#energy-use}

Before The Merge, Ethereum used proof-of-work, and a mint drew on the same energy as any other transaction. Moving to proof-of-stake cut annualized electricity use by more than 99.988%, the Crypto Carbon Ratings Institute estimates. One NFT transaction on today's network is negligible beside that older cost. Figures and the source are on the [energy consumption](/energy-consumption/) page.

## How do you get an NFT? {#how-to-get-an-nft}

1. Create a [wallet](/wallets/) and keep the keys. The contract records the token on that address.
2. Get a little [ETH](/get-eth/) for the fee, plus the price if you are buying.
3. Take a transfer, mint from a contract, or buy where the token standard is supported.

ethereum.org does not recommend a marketplace. Match the contract to an address the creator published, and read every approval. One approval can let another contract move everything in the wallet.

## What are the risks? {#nft-security}

A finalized ownership record is extremely difficult to rewrite. The market around the token is not.

- **Phishing and approvals.** Losses usually come from a fake site, an unread signature, or a leaked key.
- **Fake contracts.** A copy can use the same art and a different address. The token is real. The collection is not the one you wanted.
- **Abandoned projects.** The seller can disappear after the mint, keep a function that mints an unlimited supply, or change the metadata later.
- **Wash trading.** A seller can trade with another address they control and call it demand. One study, through late 2021, flagged about 2% of sales in the largest Ethereum collections and called that a lower bound. A 2024 study of three large marketplaces flagged about 30–40% of trades, and from about a quarter to nearly all of the dollar volume, depending on the marketplace.
- **No guaranteed buyer.** The token is worth what the next buyer will pay. The protocol does not provide one.

<ButtonLink href="/security/">
  More on security
</ButtonLink>

## Further reading {#further-reading}

- [Non-fungible tokens and intellectual property](https://www.copyright.gov/policy/nft-study/Joint-USPTO-USCO-Report-on-NFTs-and-Intellectual-Property.pdf) – _U.S. Copyright Office and U.S. Patent and Trademark Office, 12-Mar-2024_
- [EIP-2981: NFT royalty standard](https://eips.ethereum.org/EIPS/eip-2981) – _Ethereum Improvement Proposals_
- [ERC-721 token standard](/developers/docs/standards/tokens/erc-721/)
- [ERC-1155 token standard](/developers/docs/standards/tokens/erc-1155/)
- [Understanding security issues in the NFT ecosystem](https://arxiv.org/abs/2111.08893) – _Das, Bose, Ruaro, Kruegel, and Vigna, ACM CCS 2022_
- [NFT wash trading: quantifying suspicious behaviour in NFT markets](https://arxiv.org/abs/2202.03866) – _von Wachter, Jensen, Regner, and Ross, 2022_
- [NFT wash trading: direct vs. indirect estimation](https://arxiv.org/abs/2311.18717) – _Hemenway Falk, Tsoukalas, and Zhang, 2024_
- [NFT sales hit $25 billion in 2021](https://www.reuters.com/markets/europe/nft-sales-hit-25-billion-2021-growth-shows-signs-slowing-2022-01-10/) – _Reuters, 10-Jan-2022_
- [2021 Dapp Industry Report](https://dappradar.com/blog/2021-dapp-industry-report) – _DappRadar_
- [State of the Dapp Industry, Q2 2025](https://dappradar.com/blog/state-of-the-dapp-industry-q2-2025) – _DappRadar_
- [State of the Dapp Industry, Q3 2025](https://dappradar.com/blog/state-of-the-dapp-industry-q3-2025) – _DappRadar_
- [OpenSea to end resale royalties policy](https://www.theartnewspaper.com/2023/08/23/opensea-nft-marketplace-ending-resale-royalties-policy) – _The Art Newspaper, 23-Aug-2023_
- [Proof of Attendance Protocol is shutting down](https://www.theblock.co/news/ecosystems/2026-08-03-proof-of-attendance-protocol-is-shutting-down-after-5-years-410482) – _The Block, 3-Aug-2026_
- [POAP winds down after five years](https://unchainedcrypto.com/poap-winds-down-after-five-years-and-nearly-7-6-million-onchain-badges/) – _Unchained, 3-Aug-2026_
- [Ethereum energy consumption](/energy-consumption/)
- [Attack and defense in proof-of-stake](/developers/docs/consensus-mechanisms/pos/attack-and-defense/)
- [A beginner's guide to NFTs](https://paragraph.com/@lindaxie/a-beginner-s-guide-to-nfts) – _Linda Xie, 4-Jan-2021_
- [Etherscan NFT tracker](https://etherscan.io/nft-top-contracts)
- [Blockscout token tracker](https://eth.blockscout.com/tokens?type=ERC-721,ERC-1155)
- [NFTScan](https://nftscan.com/)

<Divider />

<QuizWidget quizKey="nfts" />
