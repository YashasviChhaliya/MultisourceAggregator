# MultisourceAggregator
Build consensus mechanisms from multiple oracles

**Multi-Source Oracle Aggregator**

**Project Description**
The Multi-Source Oracle Aggregator is a Clarity smart contract that implements consensus mechanisms to aggregate data from multiple oracle sources. The contract ensures reliable, tamper-resistant price feeds by requiring multiple authorized oracles to submit price data before reaching consensus. It uses statistical methods to filter out outliers and provide high-confidence price information for decentralized applications.

**Project Vision**
Our vision is to create a robust, decentralized oracle infrastructure that eliminates single points of failure in price feed systems. By aggregating data from multiple trusted sources and implementing sophisticated consensus mechanisms, we aim to provide the most reliable and accurate price data for the Stacks ecosystem. This infrastructure will enable more secure DeFi applications, prediction markets, and other price-dependent smart contracts.

**Key Features**

*Multi-Oracle Consensus*: Requires minimum threshold of oracle responses before price consensus
*Outlier Detection*: Built-in mechanisms to filter out anomalous price submissions
*Confidence Scoring*: Each consensus price includes a confidence rating
*Round-based Updates*: Time-based rounds ensure fresh, regular price updates
*Authorization System*: Only verified oracles can submit price data

**Core Functions**
1. *submit-price
clarity
(define-public (submit-price (asset (string-ascii 10)) (price uint)))
Allows authorized oracles to submit price data for specific assets. Automatically triggers consensus calculation when minimum threshold is reached.

2. *get-consensus-price*
clarity
(define-public (get-consensus-price (asset (string-ascii 10))))
Retrieves the latest consensus price for a given asset, including timestamp and confidence score.

**Future Scope**
*Phase 1 (Current)*
Basic multi-oracle consensus mechanism
Price submission and aggregation
Simple outlier detection

*Phase 2 (Next 6 months)*
Advanced statistical methods (weighted median, TWAP)
Dynamic oracle reputation system
Configurable deviation thresholds per asset
Historical price data storage

*Phase 3 (12+ months)*
Cross-chain oracle integration
Automated oracle discovery and onboarding
Machine learning-based anomaly detection
Integration with major DeFi protocols
Real-time price feeds via streaming

**Long-term Vision**
Become the standard oracle infrastructure for Stacks ecosystem
Support for diverse data types beyond prices (weather, sports, events)
Governance token for decentralized oracle management
Integration with Bitcoin L2 solutions

**Contract Address Details**

*Contract Address*: STVPRZRAXWY6875RFRS4ZSXBSY05EGKAYFFMR4S5.Multi_Source_Aggregator


**Usage Examples**
clarity
;; Submit a price as an authorized oracle
(contract-call? .oracle-aggregator submit-price "BTC" u45000)

;; Get consensus price for Bitcoin
(contract-call? .oracle-aggregator get-consensus-price "BTC")

**Security Considerations**
Only authorized oracles can submit price data
Minimum consensus threshold prevents manipulation
Price deviation limits protect against extreme outliers
Round-based system prevents stale data usage
Built with ❤️ for the Stacks ecosystem

**Transection**:
<img width="1916" height="868" alt="image" src="https://github.com/user-attachments/assets/c8d59bea-1aca-4a10-bb2e-b46fb381e10a" />
