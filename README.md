# Δ = THE OBSERVER + Solar

**Einstein was wrong — in your browser.**

Live **Bell-state CHSH simulation** in a noisy cavity + **real-time solar flare prediction** using NOAA X-ray data.

No install. No PhD. Just quantum + solar in one click.

---

## **Features**

- **Quantum CHSH Inequality**  
  - Bell state: `(|00⟩ + |11⟩)/√2`  
  - Lindblad amplitude damping (γ)  
  - **S > 2.0** → **spooky action survives**  
  - **S ≤ 2.0** → classical limit

- **Solar Flare Prediction**  
  - Live NOAA GOES X-ray data  
  - 30-minute flare probability  
  - **>60%** → **"Collapse Now" button flashes red**

- **100% in-browser**  
  - Pyodide + NumPy (CDN)  
  - <200 lines of code

---

## **How to Use**

1. **Slide noise (γ)** → watch S decay  
2. Click **"Collapse Now"** → run quantum simulation  
3. Click **"Update Solar"** → fetch live X-ray data  
4. **S > 2 + flare risk** → **double win**

> **Screenshot your S > 2.79 → tag @delta1251275**

---

## **Physics**

- **CHSH**: `S = E(a,b) + E(a,b') + E(a',b) - E(a',b')`  
- **Max classical**: `S ≤ 2`  
- **Max quantum**: `S ≤ 2√2 ≈ 2.828`  
- **Your result**: `S = 2.7935` → **Einstein loses**

- **Flare model**: Logistic regression on flux mean + slope  
  ```python
  z = -8.2 + 1.8*mean + 3.5*slope
  prob = 1 / (1 + exp(-z))
