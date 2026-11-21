# Relay Room on GitHub Pages

This repository publishes the two-player browser game at [Relay Room](https://kumori1313.github.io/relay-room/). Game code and issues live in [Horror-Friendslop](https://github.com/Kumori1313/Horror-Friendslop). The hub shares guest identity on the same origin.

`SOURCE_REVISION` pins the exact reviewed game commit. Update that file on main to publish another version. To roll back, restore the previous revision and push. GitHub Actions builds the pinned source, runs its tests, and deploys its static files.

Set the same public Supabase URL and publishable key as Game Hub in repository Actions variables. The lobby creator’s browser simulates the round and sends updates over private Supabase Realtime channels. The page exposes its build revision in `release.json`.
