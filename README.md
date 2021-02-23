# Array bug

Running `cargo test` causes a crash on macOS during the stack probe in `get`.
It appears to be attempting to allocate enough space on the stack for _n_
copies of `ARRAY`, one per match arm.
