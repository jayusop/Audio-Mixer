<p align="center">
  <a href="README.md">한국어</a> · <a href="README.en.md">English</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.ja.md">日本語</a> · <b>Français</b>
</p>

<p align="center">
  <img src="docs/icon.png" width="128" alt="Audio Mixer">
</p>

<h1 align="center">Audio Mixer</h1>

<p align="center">
  Mixeur audio pour la barre des menus de macOS · Volume par app · Égaliseur · AutoEQ<br>
  <a href="https://github.com/jayusop/Audio-Mixer/releases/latest"><b>⬇ Télécharger la dernière version</b></a> ·
  <a href="https://jayusop.github.io/Audio-Mixer/?lang=fr">Site web</a>
</p>

<p align="center">
  <img alt="macOS 14.2+" src="https://img.shields.io/badge/macOS-14.2%2B-8f7dff">
  <img alt="Apple Silicon / Intel" src="https://img.shields.io/badge/Apple%20Silicon%20%2F%20Intel-supported-ff6fb6">
  <img alt="Release" src="https://img.shields.io/github/v/release/jayusop/Audio-Mixer?color=5fe1f2">
</p>

---

Une app macOS qui vit dans la barre des menus et offre un **volume par app**, le **volume des périphériques d'entrée/sortie**, un **égaliseur graphique/paramétrique** et des **profils de correction de casque AutoEQ**. Aucun pilote audio virtuel requis.

> Configuration requise : macOS 14.2 ou version ultérieure (Apple Silicon / Intel)<br>
> 🌐 La langue de l'app suit la langue système de macOS (coréen, anglais, chinois, japonais). Les autres langues s'affichent en anglais.

## Installation

1. Téléchargez `AudioMixer.zip` depuis [Releases](https://github.com/jayusop/Audio-Mixer/releases/latest), décompressez-le et placez `AudioMixer.app` dans le dossier **Applications**.
2. À la première ouverture, macOS indique ne pas pouvoir vérifier le développeur (cette app distribuée à titre personnel n'est pas notariée par Apple). Cliquez sur **Terminé**, puis sur **Ouvrir quand même** en bas de **Réglages Système › Confidentialité et sécurité**. Ou, dans le Terminal :
   ```bash
   xattr -dr com.apple.quarantine /Applications/AudioMixer.app
   ```
3. Une icône de curseurs apparaît dans la barre des menus. La première fois qu'elle traite du son, l'app demande l'autorisation **« Enregistrement de l'audio du système »** → **Autoriser**. (Si vous l'avez manquée, activez-la dans Réglages Système › Confidentialité et sécurité › Enregistrement de l'écran et de l'audio du système.)

> Si l'autorisation est redemandée après une mise à jour, supprimez l'ancienne entrée Audio Mixer de la liste puis autorisez-la de nouveau.

## Fonctionnalités

| Domaine | Fonctionnalités |
|---|---|
| Mixeur | Choix des périphériques de sortie/d'entrée, volume matériel et coupure du son, volume logiciel pour les périphériques sans volume matériel (ex. HDMI) |
| Volume par app | Détection automatique des apps en lecture, 0–100 % (200 % en option), coupure du son, vumètres, réglages mémorisés par app, exclusion du traitement |
| Égaliseur | EQ graphique 10 bandes (±12 dB), jusqu'à 32 filtres paramétriques (PK/LSC/HSC/LP/HP/NO), courbe de réponse en fréquence, édition par glisser-déposer |
| AutoEQ | Recherche et application en ligne dans la base AutoEQ (~8 800 casques/écouteurs), import/export de ParametricEQ.txt |
| Préréglages | 17 intégrés + préréglages personnels (enregistrer/remplacer/supprimer), **bascule automatique selon le périphérique de sortie** |
| Protection du son | Préampli automatique (atténue de l'amplification maximale), limiteur de crête, protection contre l'écrêtage, balance G/D |
| Divers | Ouverture à la connexion, interrupteur général du traitement, interface en coréen · anglais · chinois · japonais |

## En toute sérénité

- **Aucun enregistrement** : le son est seulement traité en temps réel — jamais enregistré ni envoyé.
- **Quittez, le son reste intact** : si Audio Mixer se ferme (même de façon inattendue), le son de toutes les apps revient instantanément à la normale.
- **Reprise automatique** : se reconnecte tout seul après un changement de sortie ou une mise en veille.
- **Aucune interférence** : les apps qui envoient le son directement vers un autre périphérique (ex. une STAN avec interface audio) ne sont pas touchées.

## Remarques / Limites

- Si vous refusez l'autorisation, le volume par app et l'EQ ne fonctionnent pas (le son est lu normalement) ; seul le volume des périphériques est réglable.
- Juste après le début de la lecture d'une app, un très court instant de son non traité peut être audible.

## Crédits et contact

- Données des profils EQ: [AutoEq](https://github.com/jaakkopasanen/AutoEq) (jaakkopasanen)
- Signaler un bug: [Issues](https://github.com/jayusop/Audio-Mixer/issues) · e-mail jayusop@gmail.com
