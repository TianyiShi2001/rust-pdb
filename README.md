## Description
Primarily a hobby project to work more with Rust, but with a bit of luck it could end up being useful for someone. For now (27 Dec 2020) it can parse simple (crystallographic) PDBs, edit the PDB in place, gives some handy functionality and is able to save the PDB.

## Functionality
(not guarenteed complete) and stuff to do
- Parse PDB
  - [x] ANISOU
  - [x] ATOM
  - [x] CRYST
  - [x] HETATM
  - [x] MODEL
  - [x] REMARK
  - [x] SCALEn
  - [x] ORIGXn
  - [x] MTRIXn
  - [x] Use streams (minimise memory usage)
- Save PDB
  - [x] ANISOU
  - [x] ATOM
  - [x] CRYST
  - [x] HETATM
  - [x] MODEL
  - [x] REMARK
  - [x] SCALEn
  - [x] ORIGXn
  - [x] MTRIXn
  - [ ] Test with other software
     - [x] 1ubq.pdb works with Chimera
     - [ ] pTLS-6484.pdb does not work with Chimera
- Edit PDB
  - [x] Create getters/setters for internal data (plus checks)
  - [x] Create iterators to children
  - [x] Create reference to parent
  - [ ] Create adders for each struct
    - [x] Add_atom
    - [ ] Add_(1 level down)
  - [x] Remove
    - [x] Remove() - itself from parent
    - [x] Remove child from itself (some different selecting options)
- Helping
  - [x] Tell if a residue is an amino acid
  - [x] Tell if an atom is in the backbone
  - [x] Renumber PDB
  - [x] Apply affine transformations to atoms
  - [ ] Find symmetry partners (affine) transformations for space_group
- General
  - [ ] Create different abstraction for models, they are defined to be the same atoms so enforce that and help with that
    - [x] Created a simple validator which is stricter then chimera :/
  - [ ] Add documentation to EVERY function
  - [ ] Add unit tests + continuous integration
  - [ ] Create fancy (helpful) errors + warnings
  - [ ] Measure parser to find suboptimal coding (faster is always better)
    - [x] Using 'opt-level = 3' makes the execution more than 10x faster
    - [ ] Use perf or similar to find hotspots in the code


## License
MIT, just use it if you can use it, if you use it for something cool I would like to hear, but no obligations!

## PDB format
PDB 3.30 as published by wwPDB in 2008 (newest at time of creation)

## Why
Just for fun, to play with fancy abstractions. But at the same time I think tht using Rust in scientific computing would be really cool and this library would be needed if I where to be doing my internship in Rust. So by creating it I hope to extend the usability of Rust a little bit more.