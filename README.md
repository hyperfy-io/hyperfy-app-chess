# Hyperfy Chess App

This is an example of how to build your own Chess app for Hyperfy Worlds.

## Getting Started

To view or work on the app:

1. Run `yarn` and `yarn dev` to start the SDK.
2. Visit `http://localhost:4000` in the browser
3. Open the editor with `Tab` and add the Chess app to the world.

## Customization

You can customize the chess board and pieces with a little bit of effort. The following notes explain how they were to set up.

All models come from a single `scene.blend` but have an optimization pipeline that follows.

- Export the board as GLB `assets/board.glb`
- Export the pieces as GLB `src/{b|w}-{name}.glb`

Then we optimize the pieces using gltfpack and store them in the assets folder:

```shell
gltfpack -i b-bishop.glb -o ../assets/b-bishop-opt.glb -cc -tc -mm -tl 512
gltfpack -i b-king.glb -o ../assets/b-king-opt.glb -cc -tc -mm -tl 512
gltfpack -i b-knight.glb -o ../assets/b-knight-opt.glb -cc -tc -mm -tl 512
gltfpack -i b-pawn.glb -o ../assets/b-pawn-opt.glb -cc -tc -mm -tl 512
gltfpack -i b-queen.glb -o ../assets/b-queen-opt.glb -cc -tc -mm -tl 512
gltfpack -i b-rook.glb -o ../assets/b-rook-opt.glb -cc -tc -mm -tl 512
gltfpack -i w-bishop.glb -o ../assets/w-bishop-opt.glb -cc -tc -mm -tl 512
gltfpack -i w-king.glb -o ../assets/w-king-opt.glb -cc -tc -mm -tl 512
gltfpack -i w-knight.glb -o ../assets/w-knight-opt.glb -cc -tc -mm -tl 512
gltfpack -i w-pawn.glb -o ../assets/w-pawn-opt.glb -cc -tc -mm -tl 512
gltfpack -i w-queen.glb -o ../assets/w-queen-opt.glb -cc -tc -mm -tl 512
gltfpack -i w-rook.glb -o ../assets/w-rook-opt.glb -cc -tc -mm -tl 512
```
