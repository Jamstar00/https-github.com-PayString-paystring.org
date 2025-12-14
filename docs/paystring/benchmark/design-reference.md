---
title: Benchmark - Design
---

# Benchmark - Design

The purpose of this document is to share the design adopted by PayString for characterizing its performance using close-to-real test scenarios.

**Nodes Design**

*   A: Client(s) → Server(s)
*   B: Client(s) → LoadBalancer(s) → Server(s)

Both are acceptable; but ***B is recommended***.

**Scenarios Design**

The ***default*** design mimics typical PayString lookup and resolution operations, and the weight parameters enhance the flexibility of adding/removing scenarios with minimal implementation effort.

| Scenarios | Weight |
| ---| --- |
| PayString lookup - successful | 40 |
| PayString lookup - not found | 10 |
| PayString resolution - single address | 30 |
| PayString resolution - multiple addresses | 15 |
| PayString creation | 3 |
| PayString update | 2 |
| [***Optional***] HTTPS verification tests | 5 |
| [***Optional***] Cross-network resolution | 5 |
| [***Optional***] High-load concurrent requests | 10 |

**Data Design**

*   Generate test PayStrings across multiple networks (XRP Ledger, Bitcoin, Ethereum, etc.)
*   Create realistic payment address mappings for each PayString
*   Each test user is allocated multiple PayStrings with different address types
*   Test data includes valid and invalid PayString formats to test error handling
*   A group of distinct test users is pre-selected to serve as load generators
*   ***For lookup scenarios, we use either distinct PayString addresses to maximize the lookup parallelism or a limited set to test caching behavior***

**Data Volume**

*   A: Generate 100k PayStrings and set up the test scenarios with 1M+ requests
*   B: Generate 1M+ PayStrings and set up the test scenarios with 10M-25M requests

Both are acceptable, but ***B is recommended as it includes more requests and PayString mappings, which provides insights into how database growth impacts performance over time***.

**Evaluation Criteria**

*   No server failures should occur during execution
*   The request throughput should be consistent with the client sending rate
*   Response time p50 should be less than 50ms, p90 less than 100ms, p99 less than 500ms
*   The error rate (4xx and 5xx responses) must be less than 0.1%
*   All successful lookups must return valid PayString protocol responses
*   HTTPS certificate validation must succeed for all requests

**Protocol Reference**

*   PayString Protocol: [https://paystring.org](https://paystring.org) - Official PayString website and protocol overview
*   PayString RFC: [https://github.com/paystring/rfcs](https://github.com/paystring/rfcs) - Protocol specifications and RFCs
*   Implementation Guide: [https://docs.paystring.org](https://docs.paystring.org) - Technical implementation documentation
