# REPO PC v2 — Remote Support à interrupteur unique

Cette version conserve les fonctions d’optimisation de REPO et remplace les boutons d’installation manuels par un seul interrupteur **Remote Support**.

## Activer
- L’utilisateur active lui-même l’interrupteur.
- Windows affiche l’UAC ; l’utilisateur doit accepter avec son propre compte administrateur.
- REPO extrait l’agent MeshCentral officiel intégré au package et lance son mode documenté `-fullinstall`.
- L’agent s’installe comme service Windows et se reconnecte au serveur en arrière-plan.
- REPO détecte le service `Mesh Agent` et reflète son état dans l’interrupteur et le texte de statut.

## Désactiver
- L’utilisateur désactive l’interrupteur.
- Windows affiche à nouveau l’UAC.
- REPO exécute le mode documenté `-fulluninstall` du Mesh Agent, attend la disparition du service, puis retire la copie temporaire de l’installateur.

## Consentement et visibilité
- L’agent est clairement identifié dans la page Remote Support et dans les services Windows comme **Mesh Agent**.
- Le client peut le désactiver depuis REPO PC ; l’opération nécessite une autorisation Windows.
- L’installation de l’agent n’accorde pas à elle seule l’autorisation d’une session distante. Configure les demandes de consentement dans MeshCentral (par exemple Notify / Privacy Bar) pour que chaque session de prise en main soit portée à l’attention de l’utilisateur.
- Le statut « service running » confirme que le service est actif localement ; il ne garantit pas à lui seul que le PC est actuellement en ligne sur le serveur. Vérifie son état dans MeshCentral.

## Notes
- Le binaire de l’agent n’est pas inclus dans cette préversion publique.
- Le projet doit être recompilé et testé sur Windows ; ce conteneur ne dispose pas du SDK .NET/WPF.
- Pour les clients hors de ton réseau local, l’adresse serveur doit être accessible depuis Internet et utiliser un certificat HTTPS valide.
