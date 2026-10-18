# MATLAB_Data_Analytics

# 📊 Data Analytics with MATLAB

> Transforming raw spectral data into insights using MATLAB - Data cleaning, analysis, and visualization.

### 🎓 Certification
**MATLAB Onramp (complete)** - MathWorks | 
>Skills: Data import, vectorization, plotting, logical indexing

---

### 🧠 Core Data Analytics Skills Demonstrated

| Skill | How I Applied It |
| :--- | :--- |
| **Data Import & Handling** | `load starData` - Loading and managing large datasets |
| **Signal Processing** | Finding minima with `[sha,idx] = min(spectra)` and spectral analysis |
| **Data Transformation** | `lambda0 = 656.28` Doppler shift calculation: `z = lambda/lambda0 - 1; speed = z*299792.458` |
| **Logical Indexing** | Filtering data with `speed(v)<0` to separate blueshift/redshift |
| **Data Visualization** | Advanced `plot()` with lineWidth, hold on/off, multi-spectra comparison |
| **Loop Automation** | `for v = 1:7` processing 7 stellar spectra automatically |

---

### 🔬 Featured Project: Stellar Spectra Analysis

This project analyzes star movement using Doppler effect from spectral data.

**Objective:** Calculate star speed from light spectra and visualize absorption lines.

```matlab
% Task 1 - Find minimum and calculate speed
[sha,idx] = min(spectra);
lambdaDa = lambda(idx);
z = lambdaDa/656.28 - 1;
speed = z*299792.458

% Tasks 2-4 - Plot and classify moving stars
for v = 1:7
 s = spectra(:,v);
 if speed(v)<0
     plot(lambda,s,"--")
 else
     plot(v)(v)
     plot(lambda,s,linewidth=3)
 end
 hold on
end
hold off
```

**Result:** Plot showing Doppler shift - dip at ~656nm indicates star velocity.

### 📸 MATLAB in Action

<div align="left">
  <img width="800" alt="image (2)" src="https://github.com/user-attachments/assets/e8eee67c-4059-490b-b915-c069969714cb" />
  <br>
  <em>Fig 1: Live Editor - Spectral analysis and multi-plot visualization in MATLAB Onramp (88% complete)</em>
</div>

---

### 📈 Visualization Output

<p align="left">
<img width="800" alt="image" src="https://github.com/user-attachments/assets/27fee7a5-38ce-476b-aff8-9587a8439a89" />
</p>

*Left: Stellar spectra showing absorption line shift | Right: Workspace variables and speed calculations*

---

### 🛠️ Tech Stack

`MATLAB` `Live Editor` `Data Visualization` `Vectorization` `Signal Processing` `Data Cleaning`

### 🚀 How to Run
```bash
% In MATLAB
load starData
% Run starplots.mlx
```

### 📫 Connect
Interested in data analytics collaborations? Let's connect!

---
**Built with MATLAB R2024a - Focused on turning data into decisions.**
