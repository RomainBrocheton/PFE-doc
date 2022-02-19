# Exigences fonctionnelles
## Connexion
Les utilisateurs doivent pouvoir se connecter pour utiliser certaines fonctionnalités de l'application. Pour se connecter, un utilisateur doit cliquer sur le bouton de connexion. Il renseigne ensuite son adresse e-mail et son mot de passe. Une fois connecté, il est redirigé sur l'écran de visualisation manuelle.

Lors de la connexion, un token JWT sera généré et permettra de sécuriser les échanges avec l'API.

| **Endpoint**  | **Méthode** | **Succès**                    | **Erreur**                       |
|---------------|-------------|-------------------------------|----------------------------------|
| `/login`      | POST        | `{success:true, token: TOKEN}`| `{success:false, error: ERROR }` |

Le statut de la connexion est sauvegardé par le frontend dans le stockage local du navigateur. Cette variable contiendra le token JWT renvoyé en cas de succès.

## Inscription
Les utilisateurs doivent pouvoir s'inscrire. Pour s'inscrire, un utilisateur doit cliquer sur le bouton d'inscription et remplir le formulaire avec son adresse e-mail et son mot de passe. Il pourra ensuite se connecter.

| **Endpoint**  | **Méthode** | **Succès**      | **Erreur**                       |
|---------------|-------------|-----------------|----------------------------------|
| `/register`   | POST        | `{success:true}`| `{success:false, error: ERROR }` |

## Déconnexion
Les utilisateurs doivent pouvoir se déconnecter de l'application. Lorsque l'utilisateur cliquera sur le bouton de déconnexion, le stockage local contenant le token JWT sera supprimée et l'application reviendra sur la page de visualisation manuelle.

## Visualisation manuelle
Les utilisateurs doivent pouvoir visualiser les résultats de manière manuelle sur la carte. Pour se faire, ils doivent renseigner la latitude et la longitude centrale, un fichier Color et un fichier Grid.

## Visualisation automatique
## Insertion manuelle
## Insertion automatique