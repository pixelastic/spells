# dnd5-spells

All D&D 5e spells from the Player Handbook (PHB) packaged as a node module.

```js
import spells from 'dnd5-spells';
console.info(spells.eldritchBlast);
// {
//   castingTime: '1 action',
//   classes: [ 'Warlock' ],
//   components: [ 'V', 'S' ],
//   description: 'A beam of crackling energy streaks toward a creature within range. Make a ranged spell attack against the target. On a hit, the target takes 1d10 force damage.\n' +
//     'The spell creates more than one beam when you reach higher levels: two beams at 5th level, three beams at 11th level, and four beams at 17th level. You can direct the beams at the same target or at different ones. Make a separate attack roll for each beam.',
//   duration: 'Instantaneous',
//   fr: {
//     castingTime: '1 action',
//     classes: [ 'Sorcier' ],
//     duration: 'Instantané',
//     name: 'Explosion occulte',
//     page: '239',
//     range: '36m',
//     shortDescription: "Si l'attaque avec un sort touche, inflige 1d10 dégâts de force (nbre de rayons/niv)."
//   },
//   isConcentration: false,
//   isRitual: false,
//   level: 0,
//   name: 'Eldritch Blast',
//   page: '237',
//   range: '120 ft',
//   school: 'Evocation'
// }
```

## Installation

```shell
yarn add dnd5-spells
```

Or

```shell
npm install dnd5-spells
```

## Usage

The module exports an object where each key is a specific spell. Keys are camel
cased versions of the spell (for example, the "Acid Splash" spell is available
through `.acidSplash`).

Each spell also contains a `.fr` key, containing localized data in french, for
when it differs from the original data. For example, french range uses the
metric system, and page number match the french PHB. Spell name, classes,
casting time and durations are also localized.

Note that french localized version contain a short description of the spell and
not the complete description. Also, the base english spell does not yet contain
short descriptions. I'd love to sync those, but feel free to open a PR if you
have the missing data.
