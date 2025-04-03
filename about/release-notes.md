---
sort: 1
---

# Release notes

---

## What's new in solids4foam-v2.2?

The main changes from `v2.1` to `v2.2` are:

- solids4foam-v2.2 compiles with OpenFOAM-v2012 to OpenFOAM-v2412, OpenFOAM-9,
  and foam-extend-4.1

- Added CITATION.cff file

- Introduced OPENFOAM_NOT_EXTEND, OPENFOAM_COM, OPENFOAM_ORG defs aligning more
  with swak4foam, improve readability etc
    * OPENFOAM_COM         (replaces: OPENFOAMESI)
    * OPENFOAM_ORG         (replaces: OPENFOAMFOUNDATION)
    * OPENFOAM_NOT_EXTEND  (replaces: OPENFOAMESIORFOUNDATION)

- Centralise wmake-options, provision for OpenFOAM/modules integration

- Parse Allwmake arguments in high-level Allwmake

- New tutorials and README.mds, and fixes for existing tutorials

- Update Alltest to catch non-foam errors

- New GitHub actions to catch whitespace, enforce lint rules and check
  copyrights

- Added applications/utilities/README.md

- Added contact patch test tutorial

- Added applications/scripts/README.md

- Fixes and updates for material models

- Added README for functionObjects

- Write all dicts with default values to show the users the silent options

- Added vertex centred solid model

- Added transformStressToCylindrical function object

- Added README.md for punch tutorial case

- Added layeredPipe README.md

- Added curvedBeams case

- Added elastoplasticity curvedBeams README.md

- Updated the README.md in flexibleDamBreak

- Added README for slabCooling case

- Added readme for hotCylinder

- Added README for viscoTube

- Added README file for pressurisedCylinder case

- Added README file for neckingBar case

- Added README file for cylinderExpansion

- Boundary condition updates and fixes

- Add README.md for HronTurekFsi3

- 3dTube merged with 3dTubeRobin

- fluidSolidInterface: add new residual calculation option, but defaults to original incrementalResiduals approach

- Add optionalFixes/README.md

- Add segment-to-segment contact procedure based on volume intersection

- Added GuccioneElastic and electroMechanicalLaw mechanical laws

- Added enhancedVolPointInterpolation

- Ports more cases to all variants of OpenFOAM

- Add rigidRotation README

- Create LICENSE file

- linearElasticity/plateHole: use analytical solution and boundary conditions

- Added CONTRIBUTING.md file

- Added markdownlint.yml for checking all markdown files

- Added GitHub action to update the soldis4foam.github.io repository

- Add GitHub Action to remove trailing whitespace

- Add normalDisplacementZeroShear boundary condition


---

## What's new in solids4foam-v2.1?

The main changes from `v2.0` to `v2.1` are:

- solids4foam-v2.1 compiles with OpenFOAM-v2012 to OpenFOAM-v2312, OpenFOAM-9,
  and foam-extend-4.1;
- Conjugate heat transfer and thermo-fluid-solid interaction capabilities have
  been added;
- README.md files have been added to more tutorials and to the website;
- New tutorials have been added;
- A segment-to-segment contact procedure has been added to the `solidContact`
  boundary condition;
- Many bugs have been fixed, and refactorings have been performed;
- A new general vertex-centred solid model `vertexCentredLinearGeometry` has
  been created, allowing run-time selection of a block-coupled, segregated or
  explicit solution algorithm;
- A new block-coupled nonlinear geometry vertex-centred solid model has been
  added: `vertexCentredNonLinTotalLagGeometry`;
- The general `electroMechanicalLaw` has been added;
- The general `poroMechLaw` has been added;
- The `GuccioneElastic` mechanical law has been added;
- The Robin-Neumann fluid-solid interaction coupling now works with OpenFOAM.com
  and OpenFOAM.org versions;
- Centralised the wmake-options and made a provision for OpenFOAM/modules
  integration;
- Refactored compiler directives for the different versions, e.g.
  OPENFOAMESIORFOUNDATION -> OPENFOAM_NOT_EXTEND;
- Case dictionaries now get written with their default values to
  `<dictName>.withDefaultValues`;
- Refactoring of GitHub actions;
- Ported kirchhoffPlateSolid solid model and the squarePlate tutorial to
  OpenFOAM.com.

---

## What's new in solids4foam-v2.0?

The main changes from `v1.0` and `v1.1` to `v2.0` are:

- solids4foam-v2.0 compiles with newer versions of OpenFOAM and foam-extend;
- solids4foam has moved from
  [bitbucket](https://bitbucket.org/philip_cardiff/solids4foam-release/src/master/)
  to [GitHub](https://github.com/solids4foam/solids4foam);
- solids4foam has a new website (you are here now!);
- In collaboration with the preCICE development team, support has been added for
  using solids4foam with [preCICE](https://precice.org);
- The latest versions of solids4foam are now automatically added to the
  [solids4foam Docker Hub page](https://hub.docker.com/u/solids4foam);
- New solid mechanical laws have been added, including Mooney-Rivlin, Yeoh, and
  isotropic Fung (and Ogden
  [soon](https://github.com/solids4foam/solids4foam/issues/22));
- New solid models have been added, such as the
  [block-coupled vertex-centred](https://github.com/solids4foam/solids4foam/tree/nextRelease/src/solids4FoamModels/solidModels/vertexCentredLinGeomSolid)
  approach built on the [PETSc](https://petsc.org/release/) linear solver
  toolbox;
- The fluid models more closely follow the code from the underlying OpenFOAM
  version;
- The build and test scripts have been re-designed;
- A
  [tutorials benchmark data repository](https://github.com/solids4foam/solids4foam-tutorials-benchmark-data)
  has been created for storing reference data and results for the tutorials;
- solids4foam has a new logo! It is a deformed green nabla (like a deformed
  structure) with strings; the strings are a hat tip to the
  [origins of the nabla symbol](https://en.wikipedia.org/wiki/Nabla_symbol) and
  the
  [national symbol of Ireland](https://www.askaboutireland.ie/reading-room/life-society/life-society-in-ireland/overview-life-and-society/irelands-emblem/);
- The `filesToReplaceInOF` has been removed, although `optionalFixes` are still
  recommended when using foam-extend;
- foam-extend is no longer the primary development fork for solids4foam;
  instead, it is equally likely that new features will be developed in any of
  the three supported forks;
- Greater support is available for OpenFOAM.com and OpenFOAM.org versions; for
  example, multi-material and solid-to-solid contact is now supported.
