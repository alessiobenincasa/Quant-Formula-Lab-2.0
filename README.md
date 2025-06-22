# Quant Formula Lab 2.0 🚀  
**From Itô to Production** – un laboratoire open-source qui démontre, sur un seul
repo, la maîtrise simultanée  
1️⃣ des maths ﬁnancières avancées,  
2️⃣ de l’ingénierie logiciel « production-grade »,  
3️⃣ et du storytelling data pour recruteurs hedge fund.

---

## Pourquoi ce projet ?
> *“Show, don’t tell.”*  
Les desks quant cherchent des profils capables de **coder un modèle**, **l’orchestrer
en prod** et **expliquer le risque**. Ce side-project est ma « vitre » : chaque
commit relie une formule théorique à un artefact exécutable.

---

## Fonctionnalités clés
| Bloc | Contenu | Objectif de signal |
|------|---------|--------------------|
| **Core-Math** (`/pricing`, `/risk`) | Black-Scholes, Heston (SDE), Monte-Carlo antithetic, optimisation mean-CVaR & Kelly (`cvxpy`) | Rigueur mathématique |
| **Backtest & Paper-Trading** | Algo EMA 10/50 + filtre CVaR, tourné sous **QuantConnect LEAN** (Docker) avec data Zerodha | Capacité à livrer un moteur live |
| **Risk Streaming** (`/services/var-engine`) | Micro-service **Go** + Redis Streams → VaR & CVaR rolling 1 min, exposé via Prometheus | Culture micro-services & low-latency |
| **CI/CD secure** | GitHub Actions, tests > 90 %, images Docker signées Sigstore, SBOM Trivy | Discipline Dev-Sec-Ops |
| **UX & Storytelling** | Notebooks Binder + GIF démo, README → DOI Zenodo | Pédagogie & diffusion |

---

## Lancer le lab en 3 commandes

```bash
git clone https://github.com/yourUser/quant-formula-lab.git
cd quant-formula-lab
make quickstart          # build Docker, run tests et notebook démo
