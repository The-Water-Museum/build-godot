# Godot Engine Build Action

This action wraps [The-Water-Museum/godot-export](https://github.com/The-Water-Museum/godot-export) with pre-build steps to add support for:

- A local Wine installation.
  - Used by Godot to update Windows exe icons.
- A local [Osxcross](https://github.com/tpoechtrager/osxcross) installation.
  - Targets macOS SDK v13.0 by default.
  - Used by Godot to cross-compile the project for macOS, and enable ad-hoc signing.
- Metadata embedding.
  - Embeds information about the build into the project's `export_presets.cfg`.
- (future work) Feature flag management.
  - Used to manage the availability of features between different builds.

The action outputs builds for each platform configured in the project's `export_presets.cfg` file, which is based on the [Water Museum base template](https://github.com/The-Water-Museum/build-godot/blob/main/export_presets.cfg). 

Each platform's finished build is then archived and uploaded as a workflow artifact for use in later stages.

## :children_crossing: Disclaimer :framed_picture: :potable_water:

**This repository is used as part of The Water Museum's internal build processes for games. It is not necessarily intended for public use or consumption, as the underlying code may contain changes that are specific to our needs and environments.** While you're welcome to adapt our public projects to your own use cases, we are unable to offer additional support or guidance.

At times, specific improvements and features from our internal forks may be backported to their sources. Thus, we strongly recommend using the original upstream repository for your projects.
