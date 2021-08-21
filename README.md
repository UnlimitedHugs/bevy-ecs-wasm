A stripped down version of Bevy ECS, optimized for single-threaded platforms, such as WASM.  
Several low-impact dependencies were also removed to reduce build size and time.  

Without parallel execution, the stock systems scheduler adds a lot of unnecessary complexity (ordering, stages, etc.), so, making a custom scheduler may be a good idea. [Here's one I wrote.](https://github.com/UnlimitedHugs/MazeWalk/blob/a09bbe719c63e9407cd399437347d13efb590de3/src/app.rs)  
More fat trimming and optimizing could be done to the library, but the gains would likely be minimal, as the compiler already eliminates unused code.

Original project found here: [Bevy Engine](https://github.com/bevyengine/bevy)
