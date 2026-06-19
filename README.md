# MuJoCo Description Files (MJCF) for OpenArm
<img height="546" alt="image" src="media/v2.png" />

This repository contains assets for OpenArm v2 (above), Cell, v1 and v0.3 (below) simulation in MuJoCo.

## Usage

Install openarm-mujoco:

```bash
pip install openarm-mujoco
```

Launch the simulation:

```bash
openarm-mujoco-launch
```

Without White Sheet:

```bash
openarm-mujoco-launch --no-sheet
```

With Wall Collisions:

```bash
openarm-mujoco-launch --walls
```

## Task scenes

ALOHA-style bimanual manipulation scenes are provided under `v2/`:

- `v2/transfer_cube.xml` — the right arm picks up a cube and hands it to the left arm.
- `v2/insertion.xml` — the right arm grasps a red peg and the left arm grasps a blue socket, then the peg is inserted into the socket.
- `v2/two_arm_lift.xml` — both arms grasp the handles of a pot and lift it off the table together while keeping it level.

Launch one by passing its path to the launcher, for example:

```bash
openarm-mujoco-launch "$(python -c 'import openarm_mujoco.v2 as m; print(m.openarm_insertion_xml())')"
```

The matching path helpers are `openarm_transfer_cube_xml()` and `openarm_insertion_xml()` in `openarm_mujoco.v2`.

## Collision Visualization
- To view collision meshes, activate `Rendering`>`Model Elements`>`Convex Hull` and `Group Enable`>`Geom groups`>`Geom 3` in the left sidebar
- It may also help to hide the visual meshes by deselecting `Geom 2`

## Related links

- 📚 Read the [documentation](https://docs.openarm.dev/simulation/mujoco)
- 💬 Join the community on [Discord](https://discord.gg/FsZaZ4z3We)
- 📬 Contact us through <openarm@enactic.ai>

## License

Licensed under the Apache License 2.0. See `LICENSE` for details.

Copyright 2025 Enactic, Inc.

## Code of Conduct

All participation in the OpenArm project is governed by our
[Code of Conduct](CODE_OF_CONDUCT.md).
