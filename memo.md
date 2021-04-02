
* `DefaultPlugins`
    * `LogPlugin`: Adds customizable logging to your app
    * `CorePlugin`
        * Adds `Time` resource: tracks elapsed time since last update and since app started
        * Adds `EntityLabels` resource: maps Entity ids to labels, and maps labels to Entites
        * Adds `FixedTimesteps` resource: configures game's "tick" time period (1/60 seconds by default)
    * `TransformPlugin`: Allows you to perform coordinates transformations or rotations
    * `DiagnosticsPlugin`: Allows you to gather debug information, such as frames per second, CPU usage, network latency, etc.
    * `InputPlugin`: Adds keyboard and mouse to your app
    * `WindowPlugin`: Adds window support, so you can create windows, resize them, focus, move, drag & drop, etc.
    * `AssetPlugin`: Adds support for Assets, which are typed collections with change tracking, such as textures, sounds, 3d models, maps, scenes, etc.
    * `ScenePlugin`: Adds support for Scenes, which store and expose operations on entities and components.
    * `RenderPlugin` (needs "bevy_render" feature): Adds base render types and systems to your app, using a render graph, such as having 2D/3D cameras, depth textures, etc.
    * `SpritePlugin` (needs "bevy_sprite" feature): Adds support for Sprites, which are single images containing several other images such as textures or graphical elements (items, characters, etc.) that you can use as assets, manipulate, resize, move, etc.
    * `PbrPlugin` (needs "bevy_pbr" feature): Enables Physically Based Rendering, which aims at improving 3D rendering by using lighting, reflectance or metallic roughness to make 3D items more "realistic"
    * `UiPlugin` (needs "bevy_ui" feature): Adds support for in-game User Interface
    * `TextPlugin` (needs "bevy_text" feature): Adds support for in-game text display, with font sets and loaders
    * `AudioPlugin` (needs "bevy_audio" feature): Adds support for audio playback to your app
    * `GilrsPlugin` (needs "bevy_gilrs" feature): Adds support for Gilrs (Game Input Library for RuSt), an interface to work with gamepads and remote controllers
    * `GltfPlugin` (needs "bevy_gltf" feature): Adds support for Gltf (GL Transmission Format), an API-agnostic 3D asset format you can import in your app as asset
    * `WinitPlugin` (needs "bevy_winit" feature): Adds support for Winit, a cross-platform window creation and management, using components from the WindowPlugin
    * `WgpuPlugin` (needs "bevy_wgpu" feature): Adds support for WebGPU, an API for the web and Javascript to provide 3D graphics in a web browser.
* `GamePlugin` (Bevy starter, so this part is **YOUR CODE**)
    * `LoadingPlugin`: Adds support for automatically loading fonts, textures and audio as resources in your app, based on the configuration you provide in the `game_plugin/src/loading/` directory.
    * `ActionsPlugin`: Adds a resource that will execute the `set_movement_actions` function everytime the system updates (on every "tick"), allowing you to determine whether the user has pressed some keys, and what to do after that (update player's movement, etc.)
    * `MenuPlugin`: Adds the main menu where you press the "Play" button, which you can freely customize
    * `InternalAudioPlugin`: Allows you to apply conditional sound effects, by default there's the "flying" sound when you move the Bevy logo in the game
    * `PlayerPlugin`: spawns the player when game starts (during `GameState::playing` event), also spawns the camera, and applies the player movements that were calculated during the execution of the `ActionsPlugin` events when game updates on every "tick"
    * `FrameTimeDiagnosticsPlugin` (optional): TBD
    * `LogDiagnosticsPlugin` (optional): TBD