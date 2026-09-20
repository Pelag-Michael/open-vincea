# Generative asset workflows

Vincea includes a creative asset-generation layer intended to sit inside the same workflow as application editing.

## Media families

The implemented product direction includes generation workflows for:

- images;
- video;
- speech/audio;
- music;
- 3D assets.

## Workflow principle

Generation is not treated as an isolated chatbot feature.

A useful workflow can:

1. describe the asset needed;
2. choose an appropriate generation path;
3. create the asset;
4. keep the result as a local creative artifact;
5. use that artifact in the user's ongoing project.

## Provider independence

Generation can be backed by different external or local providers depending on user configuration and the requested media type.

## Long-running generation

Some media jobs take substantially longer than text generation. The product therefore treats generation as asynchronous work that can expose progress or a completion token rather than blocking a single request indefinitely.

The public repository does not publish provider credentials, internal registries, or production storage details.
