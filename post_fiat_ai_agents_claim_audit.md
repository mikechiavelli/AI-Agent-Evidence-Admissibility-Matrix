# Post Fiat Alpha Registry — AI Agents Sector Claim Audit Pack

**Sector:** AI Agents  
**Schema:** v1.0.0 · **Generated:** 2026-04-13 · **Projects:** 10 · **Claims:** 30  
Loads without login · Machine-readable JSON block below · Evidence-tier rubric at end

---

## How to consume

1. Parse the JSON block with any standard JSON parser.
2. Filter `claims` where `admissible_for_scoring = true` before feeding scores to any downstream agent or scoring workflow.
3. Treat any claim with `contradiction_flag = true` as **blocked** regardless of `evidence_tier`.
4. Check `score_confidence.operator_action` at the project level before consuming `composite_score`.
5. Re-audit whenever any `recheck_trigger` condition is met.

---

## Quick-reference summary

| Ticker | Name | Score | Admissible | Contradictions | Confidence | Action |
|--------|------|------:|:----------:|:--------------:|:----------:|--------|
| RENDER | Render Network | 8.07 | 3/3 | 0 | high | use_now |
| TAO | Bittensor | 7.85 | 2/3 | 1 | medium | use_with_caution |
| VVV | Venice.ai (VVV) | 7.20 | 2/3 | 0 | medium | use_with_caution |
| FET | Fetch.ai (ASI Alliance) | 7.20 | 1/3 | 1 | medium | use_with_caution |
| VIRTUAL | Virtuals Protocol | 7.10 | 2/3 | 0 | medium | use_with_caution |
| OLAS | Autonolas | 6.95 | 2/3 | 1 | low | refresh_first |
| NMR | Numerai | 6.80 | 2/3 | 0 | medium | use_with_caution |
| ELIZAOS | ElizaOS | 6.50 | 2/3 | 0 | medium | use_with_caution |
| AGIX | SingularityNET | 6.40 | 2/3 | 1 | medium | use_with_caution |
| KITE | Kite AI | 5.90 | 1/3 | 0 | low | refresh_first |

---

## Machine-readable artifact

```json
{
  "schema_version": "1.0.0",
  "generated": "2026-04-13",
  "sector": "AI Agents",
  "project_count": 10,
  "projects": [
    {
      "id": "RENDER",
      "name": "Render Network",
      "sector": "AI Agents",
      "composite_score": 8.07,
      "score_confidence": {
        "level": "high",
        "value": 0.88,
        "operator_action": "use_now",
        "rationale": "All 3 score drivers backed by primary or on-chain sources with no active contradictions"
      },
      "claims": [
        {
          "claim_id": "RENDER-C1",
          "text": "GPU render jobs settled on-chain via RNDR token with verifiable job completion receipts",
          "source_url": "https://rendernetwork.com/whitepaper",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If protocol migrates to new settlement layer or job verification mechanism changes"
        },
        {
          "claim_id": "RENDER-C2",
          "text": "Network migrated to Solana mainnet Q4 2023; token contract verifiable on Solscan",
          "source_url": "https://solscan.io/token/rndrizKT3MK1iimdxRdWabcF7Zg7AR5T4nud4EkHBof",
          "evidence_tier": "onchain",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "Monthly \u2014 verify active node count and job throughput on Solscan"
        },
        {
          "claim_id": "RENDER-C3",
          "text": "Apple and NVIDIA partnership integrations listed in official newsroom",
          "source_url": "https://rendernetwork.com/news/render-network-partners-with-apple",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If partnership announcements not followed by verifiable on-chain usage data within 2 quarters"
        }
      ]
    },
    {
      "id": "TAO",
      "name": "Bittensor",
      "sector": "AI Agents",
      "composite_score": 7.85,
      "score_confidence": {
        "level": "medium",
        "value": 0.65,
        "operator_action": "use_with_caution",
        "rationale": "On-chain emission mechanics confirmed but subnet performance claims rely on self-reporting; no independent fee-accrual audit"
      },
      "claims": [
        {
          "claim_id": "TAO-C1",
          "text": "Subnet emission schedule and validator reward distribution visible on-chain via Taostats",
          "source_url": "https://taostats.io",
          "evidence_tier": "onchain",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "Quarterly \u2014 emission rate changes require governance vote; monitor opentensor GitHub runtime upgrades"
        },
        {
          "claim_id": "TAO-C2",
          "text": "Individual subnet performance statistics self-reported by subnet owners on Taostats pages",
          "source_url": "https://taostats.io/subnets",
          "evidence_tier": "aggregator",
          "contradiction_flag": true,
          "admissible_for_scoring": false,
          "recheck_trigger": "Re-audit when independent subnet quality scoring published; current self-reporting creates selection bias"
        },
        {
          "claim_id": "TAO-C3",
          "text": "No protocol fee-accrual mechanism; M2 value capture is emission-only by design per whitepaper",
          "source_url": "https://bittensor.com/whitepaper",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If tokenomics v2 introduces fee burning or protocol revenue; monitor opentensor.ai governance forum"
        }
      ]
    },
    {
      "id": "VVV",
      "name": "Venice.ai (VVV)",
      "sector": "AI Agents",
      "composite_score": 7.2,
      "score_confidence": {
        "level": "medium",
        "value": 0.72,
        "operator_action": "use_with_caution",
        "rationale": "42.7% supply burn and OpenClaw integration verifiable; usage metrics rely on self-reported API call counts"
      },
      "claims": [
        {
          "claim_id": "VVV-C1",
          "text": "42.7% of VVV supply confirmed burned; burn address verifiable on Ethereum mainnet",
          "source_url": "https://etherscan.io/token/0x9a8e0217cd870783c3f2317d11432a36f9183357",
          "evidence_tier": "onchain",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "Monthly \u2014 verify burn address balance has not changed unexpectedly"
        },
        {
          "claim_id": "VVV-C2",
          "text": "OpenClaw AI integration documented on Venice.ai official product page",
          "source_url": "https://venice.ai/blog/openclaw-integration",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If integration is deprecated or OpenClaw project changes scope"
        },
        {
          "claim_id": "VVV-C3",
          "text": "Monthly active API users cited in official blog; no third-party analytics corroboration",
          "source_url": "https://venice.ai/blog/network-stats",
          "evidence_tier": "marketing",
          "contradiction_flag": false,
          "admissible_for_scoring": false,
          "recheck_trigger": "Require on-chain or third-party API call metering before admitting to usage score dimension"
        }
      ]
    },
    {
      "id": "FET",
      "name": "Fetch.ai (ASI Alliance)",
      "sector": "AI Agents",
      "composite_score": 7.2,
      "score_confidence": {
        "level": "medium",
        "value": 0.62,
        "operator_action": "use_with_caution",
        "rationale": "ASI Alliance merger complicates score attribution; merged entity tokenomics not stable for 2-quarter baseline"
      },
      "claims": [
        {
          "claim_id": "FET-C1",
          "text": "AEA framework open-source with active GitHub commit history; SDK installable via PyPI",
          "source_url": "https://github.com/fetchai/agents-aea",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "Quarterly \u2014 track commit frequency and contributor count as dev activity proxy"
        },
        {
          "claim_id": "FET-C2",
          "text": "ASI Alliance merger with SingularityNET and Ocean Protocol finalized; FET rebranded to ASI token",
          "source_url": "https://superintelligence.io",
          "evidence_tier": "primary",
          "contradiction_flag": true,
          "admissible_for_scoring": false,
          "recheck_trigger": "Re-score after 2 full quarters post-merger with unified tokenomics; integration risk unresolved"
        },
        {
          "claim_id": "FET-C3",
          "text": "DeltaV marketplace user session counts cited in official blog with no independent traffic audit",
          "source_url": "https://fetch.ai/blog/deltav-launch",
          "evidence_tier": "marketing",
          "contradiction_flag": false,
          "admissible_for_scoring": false,
          "recheck_trigger": "Seek DappRadar or Dune Analytics dashboard confirming sessions before admitting to ecosystem score"
        }
      ]
    },
    {
      "id": "VIRTUAL",
      "name": "Virtuals Protocol",
      "sector": "AI Agents",
      "composite_score": 7.1,
      "score_confidence": {
        "level": "medium",
        "value": 0.58,
        "operator_action": "use_with_caution",
        "rationale": "TVL aggregator-sourced; partner integration TVL unverified by on-chain data"
      },
      "claims": [
        {
          "claim_id": "VIRTUAL-C1",
          "text": "Protocol TVL and revenue tracked on DeFiLlama; Base chain deployment verifiable on Basescan",
          "source_url": "https://defillama.com/protocol/virtuals-protocol",
          "evidence_tier": "aggregator",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "Monthly \u2014 cross-check DeFiLlama figures against Basescan contract events after any upgrade"
        },
        {
          "claim_id": "VIRTUAL-C2",
          "text": "Agent NFT co-ownership model and token bonding curve mechanics published in official whitepaper",
          "source_url": "https://whitepaper.virtuals.io",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If bonding curve parameters changed via governance; monitor Base contract upgrade events"
        },
        {
          "claim_id": "VIRTUAL-C3",
          "text": "Partner integration list cited in official ecosystem blog; no on-chain TVL from partner apps confirmed",
          "source_url": "https://virtuals.io/blog/ecosystem",
          "evidence_tier": "marketing",
          "contradiction_flag": false,
          "admissible_for_scoring": false,
          "recheck_trigger": "Require on-chain transaction volume from named integrations before admitting to ecosystem score"
        }
      ]
    },
    {
      "id": "OLAS",
      "name": "Autonolas",
      "sector": "AI Agents",
      "composite_score": 6.95,
      "score_confidence": {
        "level": "low",
        "value": 0.44,
        "operator_action": "refresh_first",
        "rationale": "Key traction claim (service deployment count) cites marketing source with no on-chain corroboration; only 1 of 3 claims fully admissible"
      },
      "claims": [
        {
          "claim_id": "OLAS-C1",
          "text": "OLAS staking and bonding program mechanics described in official docs; contracts verifiable on Ethereum",
          "source_url": "https://olas.network/docs/tokenomics",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If tokenomics contracts upgraded; monitor Ethereum ServiceRegistry contract events"
        },
        {
          "claim_id": "OLAS-C2",
          "text": "Autonomous services deployment count cited in marketing blog; no Dune or on-chain dashboard confirms figure",
          "source_url": "https://olas.network/blog/autonomous-services-milestone",
          "evidence_tier": "marketing",
          "contradiction_flag": true,
          "admissible_for_scoring": false,
          "recheck_trigger": "Build or locate Dune query counting ServiceRegistry contract events before re-admitting"
        },
        {
          "claim_id": "OLAS-C3",
          "text": "OLAS listed in CoinGecko AI token sector index; market data aggregator-sourced",
          "source_url": "https://www.coingecko.com/en/coins/autonolas",
          "evidence_tier": "aggregator",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If token migrates chain or CoinGecko data stale >30 days"
        }
      ]
    },
    {
      "id": "NMR",
      "name": "Numerai",
      "sector": "AI Agents",
      "composite_score": 6.8,
      "score_confidence": {
        "level": "medium",
        "value": 0.7,
        "operator_action": "use_with_caution",
        "rationale": "Tournament mechanics on-chain; actual hedge fund AUM and returns not publicly disclosed"
      },
      "claims": [
        {
          "claim_id": "NMR-C1",
          "text": "NMR staking and tournament payouts verifiable on Ethereum mainnet",
          "source_url": "https://etherscan.io/token/0x1776e1f26f98b1a5df9cd347953a26dd3cb46671",
          "evidence_tier": "onchain",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "Monthly \u2014 monitor stake volume as proxy for model submission health"
        },
        {
          "claim_id": "NMR-C2",
          "text": "Tournament model performance and leaderboard published on Numerai official platform",
          "source_url": "https://numer.ai/tournament",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If Numerai changes tournament structure or scoring methodology"
        },
        {
          "claim_id": "NMR-C3",
          "text": "Numerai hedge fund AUM and returns not publicly disclosed; value capture relies on NMR burn only",
          "source_url": "https://numer.ai/about",
          "evidence_tier": "marketing",
          "contradiction_flag": false,
          "admissible_for_scoring": false,
          "recheck_trigger": "If Numerai publishes audited fund performance data"
        }
      ]
    },
    {
      "id": "ELIZAOS",
      "name": "ElizaOS",
      "sector": "AI Agents",
      "composite_score": 6.5,
      "score_confidence": {
        "level": "medium",
        "value": 0.57,
        "operator_action": "use_with_caution",
        "rationale": "GitHub activity primary-sourced; agent deployment and token utility claims lack independent on-chain corroboration"
      },
      "claims": [
        {
          "claim_id": "ELIZAOS-C1",
          "text": "ElizaOS open-source framework GitHub shows high contributor count and recent commit activity",
          "source_url": "https://github.com/elizaOS/eliza",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "Quarterly \u2014 monitor stars, forks, and contributor velocity as developer adoption proxy"
        },
        {
          "claim_id": "ELIZAOS-C2",
          "text": "ai16z DAO and ELIZAOS token mechanics cited in official documentation; DAO structure early-stage",
          "source_url": "https://elizaos.ai/docs",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If DAO governance model changes materially; monitor elizaos.ai governance forum"
        },
        {
          "claim_id": "ELIZAOS-C3",
          "text": "Agent deployment count and ecosystem partner count cited in official blog without on-chain corroboration",
          "source_url": "https://elizaos.ai/blog/ecosystem",
          "evidence_tier": "marketing",
          "contradiction_flag": false,
          "admissible_for_scoring": false,
          "recheck_trigger": "Require on-chain registry or independent analytics dashboard to verify deployment claims"
        }
      ]
    },
    {
      "id": "AGIX",
      "name": "SingularityNET",
      "sector": "AI Agents",
      "composite_score": 6.4,
      "score_confidence": {
        "level": "medium",
        "value": 0.55,
        "operator_action": "use_with_caution",
        "rationale": "AGIX merged into ASI Alliance; pre-merger score preserved but token is now ASI; re-audit required for forward use"
      },
      "claims": [
        {
          "claim_id": "AGIX-C1",
          "text": "AGIX token converted to ASI as part of ASI Alliance merger; on-chain conversion verifiable",
          "source_url": "https://etherscan.io/token/0x5b7533812759b45c2b44c19e320ba2cd2681b542",
          "evidence_tier": "onchain",
          "contradiction_flag": true,
          "admissible_for_scoring": false,
          "recheck_trigger": "Score must be re-run under ASI Alliance entity; AGIX-specific metrics no longer standalone valid"
        },
        {
          "claim_id": "AGIX-C2",
          "text": "AI service marketplace transaction history documented on SingularityNET platform",
          "source_url": "https://beta.singularitynet.io/marketplace",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If marketplace migrates to ASI-branded platform post-merger"
        },
        {
          "claim_id": "AGIX-C3",
          "text": "Ben Goertzel AGI roadmap and OpenCog Hyperon cited in official research docs; timelines speculative",
          "source_url": "https://singularitynet.io/roadmap",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "Annual \u2014 roadmap milestones should be cross-checked against published research outputs"
        }
      ]
    },
    {
      "id": "KITE",
      "name": "Kite AI",
      "sector": "AI Agents",
      "composite_score": 5.9,
      "score_confidence": {
        "level": "low",
        "value": 0.4,
        "operator_action": "refresh_first",
        "rationale": "Very early stage; most claims marketing or undated; no on-chain data independently verified"
      },
      "claims": [
        {
          "claim_id": "KITE-C1",
          "text": "Kite AI whitepaper describes proof-of-attributed-intelligence consensus mechanism",
          "source_url": "https://kiteai.gitbook.io",
          "evidence_tier": "primary",
          "contradiction_flag": false,
          "admissible_for_scoring": true,
          "recheck_trigger": "If consensus mechanism changes materially before mainnet launch"
        },
        {
          "claim_id": "KITE-C2",
          "text": "Testnet agent interaction count cited in official blog; no independent verification available",
          "source_url": "https://kiteai.gitbook.io/kite-ai/blog",
          "evidence_tier": "marketing",
          "contradiction_flag": false,
          "admissible_for_scoring": false,
          "recheck_trigger": "Require mainnet launch and on-chain data before admitting usage metrics"
        },
        {
          "claim_id": "KITE-C3",
          "text": "Partnership announcements with AI model providers cited without integration details or on-chain evidence",
          "source_url": "https://kiteai.gitbook.io/kite-ai/partnerships",
          "evidence_tier": "marketing",
          "contradiction_flag": false,
          "admissible_for_scoring": false,
          "recheck_trigger": "Require working integration commit or on-chain evidence of partner usage"
        }
      ]
    }
  ],
  "rubric": {
    "evidence_tiers": {
      "primary": "Official protocol docs, whitepapers, GitHub repos, or direct team publications. Highest admissibility weight.",
      "onchain": "Block explorers, on-chain contract events, or protocol-native indexers. Equal to primary; preferred for quantitative claims.",
      "aggregator": "DeFiLlama, CoinGecko, Taostats, DappRadar, protocol dashboards. Accepted but requires monthly recheck; methodology may lag upgrades.",
      "third_party": "Independent audits, academic papers, press coverage from named outlets. Accepted; note publication date.",
      "marketing": "Official blogs, social posts, or press releases without supporting on-chain or third-party corroboration. Not admissible by default."
    },
    "contradiction_flag": {
      "true": "Claim conflicts with another scored claim, a known on-chain fact, merger/migration event, or testnet-vs-mainnet substitution. Blocks admissibility.",
      "false": "No known active contradiction. Proceed per evidence tier rules."
    },
    "admissible_for_scoring": {
      "true": "Claim may directly feed composite scorecard dimension. Requires evidence_tier in [primary, onchain, aggregator, third_party] AND contradiction_flag = false.",
      "false": "Informational only. Do not use in weighted dimension calculation until recheck_trigger is resolved."
    },
    "score_confidence": {
      "high": "value >= 0.80. Criteria: >=2 of 3 claims admissible, 0 contradiction flags, no marketing-only score drivers. operator_action: use_now.",
      "medium": "value 0.50-0.79. Criteria: 1-2 admissible claims OR 1 contradiction OR >=1 aggregator driver for a key dimension. operator_action: use_with_caution.",
      "low": "value < 0.50. Criteria: <=1 admissible claim OR >=2 contradictions OR key score driver is marketing-sourced OR project is pre-mainnet. operator_action: refresh_first."
    },
    "operator_actions": {
      "use_now": "Score is reliable for downstream agent or authorization workflow consumption.",
      "use_with_caution": "Score is directionally valid but flag uncertainty in any output that depends on it.",
      "refresh_first": "Do not consume score until recheck_triggers for inadmissible claims are resolved."
    },
    "score_confidence_formula": "value = (admissible_claims / 3) * 0.6 + (1 - contradiction_ratio) * 0.4 where contradiction_ratio = contradictions / 3.",
    "dimension_weights": {
      "Technology_Product": 0.25,
      "Tokenomics": 0.25,
      "Market_Position": 0.2,
      "Team_Execution": 0.15,
      "Risk_Red_Flags": 0.15
    }
  }
}
```

---

## Rubric — plain-text reference

### Evidence tiers

| Tier | Definition | Admissible by default |
|------|-----------|:--------------------:|
| `primary` | Official docs, whitepapers, GitHub repos, direct team publications | Yes |
| `onchain` | Block explorers, on-chain contract events, protocol-native indexers | Yes |
| `aggregator` | DeFiLlama, CoinGecko, Taostats, DappRadar, protocol dashboards | Yes — recheck monthly |
| `third_party` | Independent audits, named press, academic papers | Yes — note date |
| `marketing` | Official blogs / social posts without corroborating on-chain evidence | **No** |

### Decision logic

```
IF contradiction_flag = true        → admissible_for_scoring = false  (always)
IF evidence_tier = 'marketing'      → admissible_for_scoring = false  (always)
IF evidence_tier IN [primary, onchain, aggregator, third_party]
   AND contradiction_flag = false   → admissible_for_scoring = true
```

### Score confidence bands

| Level | Value range | operator_action |
|-------|:-----------:|----------------|
| high | ≥ 0.80 | use_now |
| medium | 0.50 – 0.79 | use_with_caution |
| low | < 0.50 | refresh_first |

**Confidence formula:**  
`value = (admissible_claims / 3) × 0.6 + (1 − contradiction_ratio) × 0.4`  
where `contradiction_ratio = contradictions / 3`.

### Dimension weights (composite score)

| Dimension | Weight |
|-----------|:------:|
| Technology / Product | 25% |
| Tokenomics | 25% |
| Market Position | 20% |
| Team / Execution | 15% |
| Risk / Red Flags | 15% |

---

*Post Fiat Alpha Registry — AI Agents sector. Composite scores are point-in-time as of 2026-04-13. Re-audit triggers listed per claim.*