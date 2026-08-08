# oni-assets-asteroids

Procedurally generated asteroid and small-body meshes for
[ONI](https://github.com/kafeg/oni), consumed as a Git submodule at
`public/assets/models/asteroids/`. Stored with Git LFS.

Around 130 bodies, each as a GLB plus its baked surface texture and a JSON manifest
carrying the generation parameters. Bodies that have per-site terrain also ship a
`<bodyId>/` directory with landing-site patches, optimized GLBs and BVH sidecars.

Generated with [rocktools studio](https://github.com/kafeg/rocktools) — deterministic per
body id, so a mesh can always be regenerated from its manifest. The main repository's
build strips the raw sources and ships only the optimized set.

## Licensing

Original work of the ONI maintainer, source-available under the
[PolyForm Noncommercial License 1.0.0](LICENSE) — the same terms as the game.

Two things are worth stating precisely:

- **The meshes are output of rocktools, not a derivative of it.** rocktools studio is
  GPL-2.0-or-later (it forks Mark J. Stock's rocktools), but running a GPL tool does not
  place its output under the GPL. No rocktools code is present here.
- **The baked surface textures** derive from [ambientCG](https://ambientcg.com/) source
  materials, released under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/)
  (public domain — no attribution required, credited here anyway), combined with
  procedural noise authored for the project.
