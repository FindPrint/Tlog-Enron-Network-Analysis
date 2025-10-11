# Analyse du graphe Enron avec le modèle T_log(n,d)

## 🎯 Pourquoi ce projet ?
Ce projet explore une question fondamentale :  
**Comment distinguer la complexité réelle des réseaux sociaux et organisationnels par rapport aux modèles théoriques simplistes ?**

En appliquant le modèle **T_log(n,d)** au graphe des emails Enron, nous montrons que :
- Le réseau **Enron** se situe dans un régime d’**équilibre dynamique**, révélant une organisation interne riche.
- Les modèles de référence **Barabási–Albert (BA)** et **Erdős–Rényi (ER)**, malgré un degré moyen similaire, restent confinés dans un régime de **saturation**.

👉 Conclusion : les réseaux réels possèdent une complexité spectrale inaccessible aux modèles aléatoires classiques.

---

## 🧩 Le modèle T_log(n,d)
Le modèle repose sur deux paramètres :
- **n** : intensité d’interaction (degré moyen du graphe).  
- **d** : dimension spectrale (estimée via le spectre du Laplacien normalisé).  

La fonction :


\[
T_{log}(n,d) = (d - 4) \cdot \log(n)
\]



permet de classifier les réseaux en trois régimes :
- **Saturation** : T_log < -1  
- **Équilibre** : -1 ≤ T_log ≤ 1  
- **Divergence** : T_log > 1  

---

## 📂 Contenu du dépôt
- `enron_Tlog_analysis.ipynb` → Notebook principal avec code, figures et analyse.  
- `enron_phase_diagram.png` → Carte de phases pour Enron.  
- `enron_vs_ba_er_phase_diagram.png` → Comparaison triple Enron vs BA vs ER.  

---

## ⚙️ Instructions d’exécution
1. Cloner le dépôt :
   ```bash
   git clone https://github.com/<ton-utilisateur>/Tlog-Enron-Network-Analysis.git
   cd Tlog-Enron-Network-Analysis


2. Installer les dépendances :
pip install -r requirements.txt
(ou installer manuellement : numpy, scipy, matplotlib, networkx, jupyter)


3.Lancer Jupyter :
jupyter notebook


4. Ouvrir et exécuter enron_Tlog_analysis.ipynb.



📊 Résultats principaux

Enron : n ≈ 20, d significatif, T_log ≈ équilibre.

BA : n ≈ 20, d ≈ 0.07, T_log ≈ -11.8 → saturation.

ER : n ≈ 20, d ≈ 0.06, T_log ≈ -11.8 → saturation.

👉 Le contraste est net : Enron révèle une complexité organisationnelle que BA et ER ne reproduisent pas.


🔬 Portée scientifique

Le modèle T_log discrimine efficacement les régimes structurels des réseaux.

Il met en évidence la richesse spectrale des réseaux réels.

Il ouvre la voie à de nouveaux modèles génératifs capables de reproduire cette complexité.


   🚀 Perspectives
   
Étendre l’analyse à d’autres réseaux réels (scientifiques, sociaux, organisationnels).

Étudier l’évolution temporelle d’Enron (trajectoire dans la carte de phases).

Développer de nouveaux modèles génératifs intégrant la dimension spectrale.

Publier ce travail comme preuve reproductible et base de discussion scientifique.

Merci à toutes les personnes qui ont contribué à ce projet.

MIT License
