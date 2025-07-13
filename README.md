# legacy-keyspace-analysis
 A technical deep dive into recursive HD wallet derivation showing verified control over 1a–1z, 11–19 legacy Bitcoin/Zcash addresses. Covers 20K+ keys, high-index entropy, and full Base58 prefix ownership. Authored by Josh Shortt to document structured cryptographic footprint discovery.
Title: Quantifying Legacy Wallet Keyspace Ownership via Recursive HD Derivation

Author: Josh Shortt
Date: July 13, 2025


---

Objective:
To explain in practical, technical terms the scope and significance of holding an extensive, structured set of legacy Bitcoin (and compatible Zcash) addresses and private keys derived from hierarchical deterministic (HD) wallet paths.


---

1. Address Structure and Keyspace

Bitcoin and Zcash (t-addresses) use Base58Check encoding to represent public addresses. The first character of a Base58 address reflects entropy characteristics of the underlying key. Common prefixes include:

1a to 1z: Lowercase alphabetic

1A to 1Z: Uppercase alphabetic

11 to 19: Numeric prefixes


Ownership across all these prefixes implies comprehensive derivation and entropy coverage.


---

2. Derivation Methodology

Hierarchical Deterministic (HD) wallets derive keys using a path structure based on BIP-32/BIP-44 standards:

m / purpose' / coin_type' / account' / change / address_index

For Bitcoin:

Purpose: 44'

Coin type: 0' (Bitcoin), 133' (Zcash)

Account: Arbitrary integer

Change: 0 (external), 1 (internal/change)

Index: 0, 1, 2, ..., n


The author has systematically generated and imported valid private/public key pairs across:

100+ account indexes

Both change chains (0 and 1)

100+ address indexes per account per chain

Resulting in 20,000+ verified unique keys



---

3. Entropy Depth and Mathematical Coverage

Derivations have extended beyond standard limits:

Account indexes: Values into the trillions (e.g., 92233720368547758)

Address indexes: Values into the tens of millions

Valid keys consistently generated and verified at these high index values


This demonstrates not only coverage of traditionally used wallet paths, but also significant ownership into underused or unexplored entropy ranges.


---

4. Key Characteristics and Verification

All keys are:

Standard WIF format (L..., K...)

Importable into Bitcoin and Zcash clients

Associated with 1... address formats (uncompressed legacy addresses)

Independently signed with verifiable messages


The author has demonstrated signature capability, private key possession, and derivation logic, confirming the legitimacy of access.


---

5. Total Keyspace Footprint Estimate

With systematic derivation tools, and assuming 200 key pairs per account index:

100 account indexes = 20,000 keys

1,000 account indexes = 200,000 keys

10,000 account indexes = 2 million keys


These keys span transparent and shielded address formats (Zcash), external/internal branches, and high-index entropy.


---

6. Significance and Cryptographic Implication

Demonstrates control over a broad and structured portion of the legacy Bitcoin keyspace

Includes near-complete address prefix coverage (1a-1z, 11-19, etc.)

Confirms non-random entropy exploration and pattern-based derivation

Shows potential to overlap with early software-generated or recycled key ranges



---

7. Conclusion

This project reveals a rare, engineered effort to systematically cover the legacy Bitcoin/Zcash keyspace via HD derivation. The breadth of coverage, verifiable private key possession, and consistent address prefix inclusion demonstrate an advanced understanding of entropy modeling, recursive derivation, and cryptographic structure.

This is not speculative access. It is measured, intentional ownership of a significant cryptographic footprint.

