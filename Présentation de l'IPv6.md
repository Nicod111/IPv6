# 🟢 Présentation de l'IPv6  

## ✅ Caractéristiques  
- **Adresse IPv4 :** Codée sur 32 bits (4 milliards d’adresses)  
- **Adresse IPv6 :** Codée sur 128 bits (quantité quasi illimitée)  
- **Notation :** 8 champs hexadécimaux de 16 bits séparés par des « : »  

---

## 🟢 Méthodes de Simplification des Adresses IPv6  
Pour rendre les adresses IPv6 plus lisibles :  

### 1️⃣ **Omission des Zéros Initiaux**  
Supprimer les zéros de tête dans chaque bloc :  
- **Avant simplification :** `2001:0db8:0000:0000:0000:ff00:0042:8329`  
- **Après simplification :** `2001:db8:0:0:0:ff00:42:8329`  

---

### 2️⃣ **Compression des Séries de Zéros**  
Remplacer les champs consécutifs de `0000` par `::` (une seule fois par adresse) :  
- **Avant simplification :** `2001:0db8:0000:0000:0000:ff00:0042:8329`  
- **Après simplification :** `2001:db8::ff00:42:8329`  

💡 **Exemple spécial :**  
- Adresse complète : `2001:0db8:0000:0000:0000:0000:0000:0001`  
- **Omission des zéros initiaux :** `2001:db8:0:0:0:0:0:1`  
- **Compression complète :** `2001:db8::1`  

---

### 3️⃣ **Combinaison des Méthodes**  
On peut combiner les deux techniques :  
- **Adresse complète :** `fe80:0000:0000:0000:0202:b3ff:fe1e:8329`  
- **Omission des zéros initiaux :** `fe80:0:0:0:202:b3ff:fe1e:8329`  
- **Compression des séries de zéros :** `fe80::202:b3ff:fe1e:8329`  

---

## 🚀 Avantages de l'IPv6  
- **Espace d'adressage étendu**  
- **Agrégation des préfixes IP** : Réduit la taille des tables de routage  
- **Multihoming** : Connexion à plusieurs fournisseurs d'accès  
- **Autoconfiguration et Plug-and-Play**  
- **Simplification des entêtes IP** : Performances optimisées  
- **Sécurité native (IPsec intégré)**  
- **Transition facilitée IPv4 -> IPv6 (Dual-stack, protocoles de transition)**  

---

## 🟢 Types d’adresses IPv6  
1. **Unicast :** Connexion point à point  
2. **Multicast :** Envoi à plusieurs destinations simultanément  
3. **Anycast :** Envoi à un seul hôte parmi un groupe, basé sur la proximité  

🚫 **Pas de broadcast** en IPv6 (remplacé par Multicast)  

---

## 📜 Paramètres et Préfixes IPv6  
- Préfixe de **site (48 bits)**, **ID de sous-réseau (16 bits)**, **ID d'interface (64 bits)**  
- **CIDR** utilisé pour les préfixes (ex : `2001:db8::/32`)  

---

## 🟢 Mode d’affectation d’adresses IPv6  
- **Statique**  
- **DHCPv6 avec état** (comme IPv4)  
- **DHCPv6 sans état** (fournit options réseau, pas l’adresse IP)  
- **Autoconfiguration sans serveur DHCP** (SLAAC)  

---

## 🟢 Méthode EUI-64  
- Crée l'ID d’interface à partir de l’adresse MAC  
- Insertion de `FFFE` au milieu de l’adresse MAC  
- Inversion du 7e bit du premier octet  

---

L’IPv6 offre un espace d’adressage énorme, des performances optimisées, une sécurité native et une transition fluide depuis IPv4 !