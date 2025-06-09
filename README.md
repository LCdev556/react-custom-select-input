# react-custom-select-input

Un composant `SelectInput` React réutilisable, converti depuis un plugin jQuery existant.  
Fait partie du projet d'évaluation OpenClassrooms : conversion de plugins jQuery en composants React.

## Dépendances

Ce composant React nécessite les dépendances suivantes pour fonctionner correctement :

- **React** (version 19.1.0 supérieure)
- **Prop-types** (version 15.8.1 ou supérieure)
- **Bootstrap** (version 5.3.6 ou supérieure)

Assurez-vous de les avoir installées dans votre projet avant d'utiliser ce composant

## ✨ Fonctionnalités

- Affiche un `<select>` avec :
  - un label personnalisé
  - une option placeholder
  - une liste d’options dynamiques
  - la gestion des erreurs de validation
- Clés de valeur et de label personnalisables via `valueKey` et `labelKey`

## 📦 Installation

### Depuis npm :

```bash
npm i @lcdev556/react-select-input
```

## 📚 Utilisation

```jsx
import SelectInput from 'react-custom-select-input';

const options = [
  { label: 'Option 1', value: 'opt1' },
  { label: 'Option 2', value: 'opt2' },
];

function App() {
  const [selected, setSelected] = useState('');

  return (
    <SelectInput
      id="mySelect"
      name="mySelect"
      value={selected}
      onChange={(e) => setSelected(e.target.value)}
      label="Choose an option"
      placeholder="Select..."
      options={options}
      error=""
    />
  );
}
```

## 📖 Props

| Prop         | Type              | Obligatoire | Description |
|--------------|-------------------|:------------|:--------------|
| `id`         | `string`          | ✅          | Identifiant unique pour le champ |
| `name`       | `string`          | ✅          | Nom du champ |
| `value`      | `string` ou `number` | ✅       | Valeur sélectionnée |
| `onChange`   | `function`        | ✅          | Fonction déclenchée au changement |
| `label`      | `string`          | ✅          | Texte du label |
| `placeholder`| `string`          | ✅          | Texte affiché dans l'option par défaut |
| `options`    | `array` d'`object`| ✅          | Liste des options `{ label, value }` |
| `valueKey`   | `string`          | optionnel   | Clé pour la valeur dans chaque option (par défaut `value`) |
| `labelKey`   | `string`          | optionnel   | Clé pour le label dans chaque option (par défaut `label`) |
| `error`      | `string`          | optionnel   | Message d'erreur |

## 📜 Licence

MIT

---

## 📎 Projet réalisé dans le cadre de la formation [OpenClassrooms Développeur d’Application JavaScript React](https://openclassrooms.com/fr/paths/717-developpeur-dapplication-javascript-react).
