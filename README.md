# oogaboogaland-fork

Custom Tesla-robot Ooga for [Ooga Booga Land](https://github.com/OogaBoogaX/oogaboogaland).

This repo holds one custom contributor character, **Optimus Ooga** (handle and GitHub login `ibrihamturay-coder`), in `src/characters/ibrihamturay-coder.js`. It's based on the `2140data` android. The plating is white and silver with black joints and a cyan core. A black visor band carries two steady blue eyes, and the character carries nunchaku. Cyan thrusters in the soles give it foot-rocket jumps and flight. The body swaps between a gloss-white look and a brushed-silver look through the game's `tint` hook.

It's plain vanilla JavaScript with no dependencies. The file calls `BL.characters.add({ handle, github, display, joined, lastCommit, look, voice, dress })`, the format described in upstream `AGENTS.md`.

## Adding it to the island

1. Fork [OogaBoogaX/oogaboogaland](https://github.com/OogaBoogaX/oogaboogaland) and work from the `rock` branch.
2. Copy `src/characters/ibrihamturay-coder.js` into `src/characters/` in your fork. Add only this file and change nothing else: no shared lists, tests or other files.
3. Run `npm run build`. It regenerates the gitignored `src/js/characters.gen.js` and `oogaboogaland.html`. Then run `node --check src/characters/ibrihamturay-coder.js`. You can also run `npm run characters` to list the cast and `npm run test:unit` for the "characters" checks. That needs no Chrome, and upstream asks for Node 22+.
4. Commit only the character file. Don't commit `oogaboogaland.html` or `characters.gen.js`, because both are gitignored build output.
5. Open a pull request against the `rock` branch.
6. Once it's merged, CI's Pages workflow rebuilds and deploys the site, and Optimus Ooga shows up on the island.

## License

Upstream Ooga Booga Land uses **THE OOGA BOOGA LICENSE**, which works like a public-domain dedication (`package.json` says `"Unlicense"`): "Me throw away all 'mine.' Code for all tribe..." This character file is contributed under the same terms.
