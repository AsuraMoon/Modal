# ConfirmationModal Component Readme

`ConfirmationModal` est un composant React qui affiche un message de réussite lorsqu'une personne est enregistrée avec succès. Il masque automatiquement le message après 3 secondes, mais permet également une fermeture immédiate en cliquant sur le bouton "X".

## Utilisation

### Imports des dependecies 

`npm i sass` pour le style pré-defini

### Importation du composant

```javascript
import ConfirmationModal from './ConfirmationModal';
```

### Props

Le composant accepte deux props :

- `isVisible` (obligatoire, booléen) : Un booléen indiquant si le message doit être visible ou non.
- `onHide` (obligatoire, fonction) : Une fonction à appeler lorsque le message est fermé, automatiquement ou manuellement.

### Exemple

```javascript
function MyComponent() {
  const [isMessageVisible, setIsMessageVisible] = useState(false);

  const handleRegistrationSuccess = () => {
    setIsMessageVisible(true);
  };

  return (
    <>
      {/* Formulaire d'inscription ou autre contenu */}
      <ConfirmationModal isVisible={isMessageVisible} onHide={() => setIsMessageVisible(false)} />
    </>
  );
}
```

### Style

Le composant inclut un style de base, mais peut être personnalisé en utilisant les classes CSS fournies :

- `confirmation-overlay` : Le conteneur de superposition.
- `overlay-visible` : L'état visible de la superposition.
- `confirmation-message` : Le conteneur pour le message.
- `visible` : L'état visible du message.
- `hidden` : L'état caché du message.

### Validation des props

Le composant utilise PropTypes pour valider ses props :

- `isVisible` : Doit être un booléen.
- `onHide` : Doit être une fonction.

### Note

Ce composant est conçu pour être utilisé dans un environnement React et nécessite l'utilisation de hooks et de PropTypes. Assurez-vous que votre projet inclut ces fonctionnalités avant d'utiliser ce composant.

### Keywords

Modal React JS 