# Tommygun875
Building an open-source digital raffle drum so creators can run transparent giveaways without the chaos of paper tickets.
# Digital Raffle Drum (open source)

A transparent, visual raffle drum for creators. Import entries, spin a digital drum, and pick a random winner you can show on-camera.

---

## 🧩 Why
Giveaways get messy once they hit thousands of entries.  
This project keeps the *look* of a physical raffle drum while making draws digital, fair, and verifiable.

---

## 🚀 Features
- Paste or import entries (CSV / Google Sheets)
- 3-D or list-shuffle animation for the draw
- Secure random selection. tickets are tied to physics.
- Audit log with seed + timestamp for verification
- Simple web UI (React + Node)

---

## 🛠️ Tech Stack
| Layer | Tools |
|-------|-------|
| Frontend | React / Next.js + Three.js |
| Backend | Node / Express + Supabase |
| RNG | `crypto.getRandomValues()` |
| Build | Vite or Next.js |

---

## 🔐 Randomness Verification
1. Generate a `serverSeed`, hash it, publish the hash.  
2. Combine `serverSeed + timestamp + entryCount` → hash again.  
3. `winnerIndex = hash % entryCount`.  
4. Reveal `serverSeed` after the draw so anyone can verify.

---

## 🧱 Roadmap
| Phase | Goal |
|-------|------|
| MVP | Paste entries → pick winner → log result |
| Phase 1 | 3-D drum animation |
| Phase 2 | Google Sheets import |
| Phase 3 | Public “watch the draw” page |
| Phase 4 | VRF (verifiable random function) integration |

---

## 💡 Contributing
See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 📄 License
[MIT](LICENSE)

---

## 👤 Maintainer
Thomas Griffin  
📧 thomasrgriffin17@gmail.com
