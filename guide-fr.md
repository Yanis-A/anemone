# Anemone : installation et réglages

Anemone se place entre ton micro et ton chat vocal. Il nettoie ta voix et la met en avant, ajoute la musique, les pads de sons et des effets, puis envoie le tout à Discord ou au chat vocal d'un jeu, comme un micro ordinaire. Son interface est en français quand Windows l'est.

<p align="center">
  <img src="images/cockpit-fr.png" alt="La fenêtre d'Anemone en français : Voix et Rack FX à gauche, la Soundboard au centre, Musique, Mix et Sortie à droite" width="100%">
</p>

## 1. Installer

1. Il te faut **Windows 10 ou 11, en 64 bits**.
2. Installe **VB-Cable**, gratuit, depuis [vb-audio.com/Cable](https://vb-audio.com/Cable/). C'est un câble audio virtuel : Anemone envoie le son dedans, et Discord l'écoute comme un micro. Il n'est pas fourni avec Anemone. Redémarre si son installateur te le demande.
3. Télécharge [`Anemone-windows-x64.zip`](https://github.com/Yanis-A/anemone/releases/latest/download/Anemone-windows-x64.zip), décompresse-le où tu veux et lance `Anemone.exe`. Il n'y a pas d'installateur.

> **« Windows a protégé votre ordinateur » ?** Anemone n'est pas signé, alors SmartScreen peut prévenir au premier lancement. Clique sur **Informations complémentaires**, puis **Exécuter quand même**.

## 2. Régler Anemone

Ouvre le panneau des appareils (l'icône des curseurs, en haut) et vérifie :

- **Micro** : ton micro ;
- **Casque** : ton casque ou tes enceintes ;
- **Sortie d'appel** : `CABLE Input (VB-Audio Virtual Cable)`.

## 3. Régler Discord

Ouvre les **Paramètres utilisateur** (la roue dentée, en bas à gauche), puis **Voix et vidéo** :

- **Périphérique d'entrée** : `CABLE Output (VB-Audio Virtual Cable)` ;
- **Périphérique de sortie** : ton casque, comme d'habitude ;
- **Profil d'entrée audio** : **Studio** (audio pur, sans aucun traitement).

Le profil Studio compte beaucoup : Anemone retire déjà le bruit et règle le niveau. Le traitement de Discord par-dessus abîmerait ta voix, la musique et les pads.

Clique sur **Vérifions** pour t'entendre comme les autres t'entendent.

Dans un jeu qui a son propre chat vocal, choisis `CABLE Output` comme micro, et coupe sa suppression de bruit s'il en a une.

## Bon à savoir

- **Te couper** : le bouton **ON AIR** en haut d'Anemone (On/Off) coupe tout ce qui part vers l'appel. Il a un raccourci global, qui marche aussi en jeu.
- **T'entendre dans le casque** : active *Entendre ma voix* dans le panneau Sortie.
- **Plus de son sur ton PC après l'installation de VB-Cable ?** Windows prend parfois le câble comme appareil par défaut. Appuie sur Win+R, tape `mmsys.cpl`, puis remets tes enceintes ou ton casque (onglet *Lecture*) et ton micro (onglet *Enregistrement*) comme périphériques par défaut. Ne mets jamais `CABLE Input` comme sortie par défaut : tout le son du PC partirait dans l'appel.
- Fermer la fenêtre laisse Anemone tourner dans la zone de notification, à côté de l'horloge. Les réglages sont gardés dans `%APPDATA%\Anemone\settings.json`.
