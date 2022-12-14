# Event Handlers

<div style="text-align: center; font-style: italic; font-weight: 100;">
    <br />
    <img style="width: 400px; border: 10px solid rgb(242,242,207);" src="./DALL·E finger on a touch-screen emitting lightning where it touches.png" />
    <br />
    A finger on a touch-screen, emitting lightning where it touches
    <br />
    <br />
</div>

```rust
#[pax(
    <Rectangle @click=self.handle_click>
)]
pub struct HelloEvents {}
impl HelloEvents {
    pub fn handle_click(&mut self, args: ArgsClick) {

    }
}

```

In the above example, `on_click=self.handle_click` binds a the `handle_click` method defined in the host codebase to the built-in `click` event which Pax fires when a user clicks the mouse on this element.

Events fire as "interrupts" and are allowed to execute arbitrary, side-effectful, imperative logic — anything you can write or use in Rust.

It is inside event handlers that you will normally [change property values](./start-key-concepts-properties-settings.md#settings-at-runtime), using `.set` or `.ease_to`.

Pax includes a number of built-in user interaction events like `@click` and `@tap`.  These can all be bound and handled in the same manner.




<!-- TODO: describe how to create & bind custom events -->

