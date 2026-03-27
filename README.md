# inertia-wheels-sbus

**Inertia Wheels S.Bus Cable — Legacy / Discontinued**

---

## 📄 Reference Document

👉 **Open the full cable specification:**  
[IW-C-SB-V2.pdf](./IW-C-SB-V2.pdf)

---

## Overview

This document describes the legacy S.Bus cable used to connect Inertia Wheels receivers to standard S.Bus-compatible systems.

It may also function with Alpha Wheels via Alpha Link wireless.

This information is provided for customers maintaining or integrating with existing (legacy) systems.

---

## Support Status

⚠️ **This interface is no longer supported or recommended for new systems.**

This documentation is provided for reference only. NODO does not provide support, validation, or guarantees for S.Bus-based integrations.

---

## Important Considerations

- The cable design is **unshielded**, making it susceptible to:
  - Motor noise
  - Wireless interference
  - Ground noise coupling

- Some systems (e.g., Ronin 2) use auxiliary S.Bus channels for functions such as:
  - Recenter
  - Run/Stop

- These auxiliary channels are particularly **sensitive to signal degradation** and may behave unpredictably in noisy environments.

- The S.Bus protocol itself:
  - Has **no built-in checksum**
  - Provides **no inherent error detection or correction**

---

## Implications

Due to the above:

- Signal integrity issues may result in:
  - Intermittent control behavior
  - Incorrect channel values
  - Unintended triggering of auxiliary functions

- Reliability will vary significantly depending on:
  - Cable routing
  - Electrical environment
  - System grounding

---

## Recommendation

For all new systems and critical applications, use **modern, noise-resilient communication methods** supported by the TORQ ecosystem.

---

## Disclaimer

This documentation is provided as-is for legacy compatibility purposes.  
NODO assumes no responsibility for performance, reliability, or safety when using S.Bus-based integrations.
