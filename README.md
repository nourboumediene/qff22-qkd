# Quantum Key Distribution Challenge

<p float="middle" style="pointer-events:none;">
  <img align="middle" src="logos/qff22_logo.png" width="26%"/>
  <picture>
  <img align="middle" width="54%"/>
  </picture>
  <img align="middle" src="logos/cqtech_logo.png" width="18%"/>
  
</p>

This challenge is proposed by [Constantine Quantum Technologies](https://cqtech.org/) for the [Qiskit Fall Fest 2022 at Algiers](https://qiskit-fall-fest-algiers.wtmalgiers.org/) organized by [Women Techmakers Algiers](https://www.linkedin.com/company/wtm-algiers/) & [GDG Algiers](https://www.gdgalgiers.com/)

## Introduction
In the BB84 protocol, Alice sends Bob a series of single photons/states through a quantum channel. If Eve measures these photons before they reach Bob, then her measurement can be detected, and Alice and Bob will know that an eavesdropper is spying on them.
However, in practice, Alice will most likely send multiple photons with the same state; it is indeed not an easy task to create only single photons 100% of the time. Therefor, Eve will intercept one of the photons and let the others pass to Bob. She will store the quantum state of her photon in a quantum memory and wait for the bases reveal. After Alice and Bob reveal their bases, Eve can then measure her stored states and get valuable information on the shared key.

To counteract this issue, the BBM92 protocol uses a source of entangled photons which are received by both Alice and Bob, instead of relying on Alice to send a quantum message to Bob. The rest of the protocol remains the same as with BB84. This renders the technique used by Eve in the BB84 case (photon number splitting attack, or PNS attack) completely ineffective.

## Tasks
In this challenge, try to:
1. Simulate a PNS attack in the case of BB84 with Qiskit. In this case, and for the sake of simplicity, Alice will always send 2 photons/states to Bob, making Eve's attack 100% effective.
2. Implement the BBM92 protocol.
3. Demonstrate the effectiveness of BBM92 against the PNS attack scheme which was described in the case of BB84. We will consider the case where two pairs of photons are emitted each time, instead of one.

**Notes**:
- You can use the BB84 codes from the workshop.
- To simulate Alice and Bob measuring their entangled photons (in BBM92), you must perform both measurements before running the qiskit job to ensure the correctness of the results, i.e., you cannot measure Alice's qubit and run the job and then measure Bob's qubit afterwards.
