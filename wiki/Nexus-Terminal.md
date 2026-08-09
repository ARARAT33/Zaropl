# ⚡ Nexus Terminal — Complete Technical Reference

> **Warning**: This documentation describes a tool that is intentionally complex and obfuscated.

---

## Architecture: 7-Layer Onion Pattern

```
Layer 7: SelfModCore       (recursive introspection, mutation)
  └─ Layer 6: DimensionalCompressor (Gram-Schmidt projection)
       └─ Layer 5: EntropyPool       (cryptographic randomness)
            └─ Layer 4: SignalModulator   (DSP engine)
                 └─ Layer 3: PatternRecognizer (Markov chains)
                      └─ Layer 2: EventFractalizer  (recursive branching)
                           └─ Layer 1: ShadowDOM          (virtual state tree)
                                └─ Layer 0: SymbolicConstants  (encrypted keys)
```

---

## Layer Details

### Layer 0: Symbolic Constants
- κ (kappa): Empty registry | Σ (Sigma): XOR stream cipher | Δ (Delta): Key "nexus:quantum:forge:2026" | Φ (Phi): Encrypted core serial

### Layer 1: ShadowDOM
Virtual tree with 24 nodes. 12 entangled pairs (n0⟷n6, n1⟷n7, ...). Observer pattern for mutation tracking.

### Layer 2: Event Fractalizer
1 source event → 30 sub-events (depth 4). 2^1+2^2+2^3+2^4 = 30 total. Each carries fractalLevel, fractalIndex, totalFractals, fractalSeed.

### Layer 3: Pattern Recognizer
3rd-order Markov chain. 8-state transition matrix (α,β,γ,δ,ε,ζ,η,θ). Hidden states via hashed keys. `predict()` uses weighted random selection.

### Layer 4: Signal Modulator
7 oscillators (sine/square/sawtooth/triangle/noise). 7 filters (lowpass/highpass/bandpass). Cross-modulation: signal←shadow, compress←entropy. ADSR envelope.

### Layer 5: Entropy Pool
512 bytes. 8-round mixing: `pool[i] = pool[i]⊕pool[i+37]⊕pool[i+73]⊕(pool[i]<<3)⊕(pool[i+37]>>5)`. Shannon entropy monitoring.

### Layer 6: Dimensional Compressor
8D Gram-Schmidt basis. Lossy compression by keeping top-N coefficients. Supports project/reconstruct/compress operations.

### Layer 7: SelfModCore
Layer management, mutation tracking, evolution cycles. Each cycle: noise perturbation + mutation re-application. Supports introspection and JSON serialization.

---

## Commands

### Visible (13)
| Command | Function |
|---------|----------|
| `help` | Show command list |
| `scan` | Full diagnostic (evolves core, reads all layers) |
| `tree` | Display ShadowDOM nodes with value bars |
| `signal` | Live oscillator outputs |
| `entropy` | Shannon entropy, pool sample, RNG |
| `patterns` | Hidden pattern states |
| `compress` | 8D→4D compression demo |
| `evolve` | 3-cycle evolution with oscillator mutation |
| `events` | Fractalize 3→30 sub-events |
| `chain` | Markov chain entries |
| `inject [data]` | Feed custom data to entropy pool |
| `clear` | Clear terminal |
| `admin` | Open hidden admin panel |

### Hidden (5)
| Command | Effect |
|---------|--------|
| `quantum` | 7 rapid cycles with live display |
| `deepscan` | 25 cycles, full introspection output |
| `nexus` | Show encrypted serial + key |
| `self` | Introspection report |
| `hack` | Animated decryption sequence |

---

## Admin Panel
Accessed by typing `admin`. Controls: Evolve (+5), Inject Entropy, Reset Core. Metrics: nodes, chains, oscillators, entropy, compression ratio, generations, mutations.

## Background Process
Every 3s: tick modulator, update metrics, 15% chance auto-evolve, refresh heatmap.

## Encryption
Rolling XOR cipher: `Σ(s,k) = s[i] XOR k[i%len(k)]`. Static key Δ="nexus:quantum:forge:2026".