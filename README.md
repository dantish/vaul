


https://github.com/emilkowalski/vaul/assets/36730035/fdf8c5e8-ade8-433b-8bb0-4ce10e722516


Vaul is an unstyled drawer component for React that can be used as a Dialog replacement on tablet and mobile devices. It uses [Radix's Dialog primitive](https://www.radix-ui.com/docs/primitives/components/dialog#trigger) under the hood and is inspired by [this tweet](https://twitter.com/devongovett/status/1674470185783402496).

## Usage

To start using the library, install it in your project:

```bash
npm install vaul
```

Use the drawer in your app.

```jsx
import { Drawer } from 'vaul';

function MyComponent() {
  return (
    <Drawer.Root>
      <Drawer.Trigger>Open</Drawer.Trigger>
      <Drawer.Portal>
        <Drawer.Content>
          <p>Content</p>
        </Drawer.Content>
        <Drawer.Overlay />
      </Drawer.Portal>
    </Drawer.Root>
  );
}
```

## Examples

Play around with the examples on codesandbox: 

- [With scaled background](https://codesandbox.io/p/sandbox/drawer-with-scale-g24vvh?file=%2Fapp%2Fmy-drawer.tsx%3A1%2C1)
- [Without scaled background](https://codesandbox.io/p/sandbox/drawer-with-scale-forked-nx2glp?file=%2Fapp%2Fmy-drawer.tsx%3A4%2C1)
- [Scrollable with inputs](https://codesandbox.io/p/sandbox/drawer-with-scale-forked-73f8jw?file=%2Fapp%2Fmy-drawer.tsx%3A1%2C1)

## API Reference

### Root

Contains all parts of a dialog. Use `shouldScaleBackground` to enable background scaling, it requires an element with `[vaul-drawer-wrapper]` data attribute to scale its background.
Can be controlled with the `value` and `onOpenChange` props. Can be opened by default via `defaultOpen` prop.

### Trigger

The button that opens the dialog. [Props](https://www.radix-ui.com/docs/primitives/components/dialog#trigger).

### Content

Content that should be rendered in the drawer. [Props](https://www.radix-ui.com/docs/primitives/components/dialog#content).

### Overlay

A layer that covers the inert portion of the view when the dialog is open. [Props](https://www.radix-ui.com/docs/primitives/components/dialog#overlay).

### Title

An accessible title to be announced when the dialog is opened. [Props](https://www.radix-ui.com/docs/primitives/components/dialog#title).

### Description

An optional accessible description to be announced when the dialog is opened. [Props](https://www.radix-ui.com/docs/primitives/components/dialog#description).

### Close

The button that closes the dialog. [Props](https://www.radix-ui.com/docs/primitives/components/dialog#close).

### Portal

Portals your drawer into the body.
