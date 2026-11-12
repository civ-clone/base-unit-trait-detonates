# base-unit-trait-detonates

The `Detonates` unit trait: a unit type with it detonates instead of fighting.

A unit type with this trait is a nuclear weapon: it detonates on its target rather than attacking it.

For example: Civ1: Nuclear. Civ2: Nuclear Msl.

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(Detonates)`:

```ts
import Detonates from '@civ-clone/base-unit-trait-detonates/Detonates';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, Detonates));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
