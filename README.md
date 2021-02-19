# @bobthered/svelte-modal

Svelte component for creating modals with tailwindcss

## Installation

```
npm i -D @bobthered/svelte-modal
```

## Basic Usage

```
<script>
  import Modal from '@bobthered/svelte-modal'
</script>

<Modal>Modal Body</Modal>
```

## Core Props

| Prop         | Default | Description                                         |
| ------------ | ------- | --------------------------------------------------- |
| closeable    | `true`  | Determine if the modal can be closed by the user    |
| container    | `{}`    | Container classes ( see below for available props ) |
| modal        | `{}`    | Modal classes ( see below for available props )     |
| overlay      | `{}`    | Overlay classes ( see below for available props )   |
| show         | `false` | Set whether the modal is visible or not             |
| showTitleBar | `true`  | Set whether the modal title bar is visible or not   |
| title        | `""`    | Set the modal title text                            |
| titleBar     | `{}`    | Title bar classes ( see below for available props ) |

## Styling

Multiple components can be styled. Each component has it's own default classes that can be overwritten

### Container Props

| Prop           | Default               |
| -------------- | --------------------- |
| alignItems     | `items-center`        |
| class          | `""`                  |
| display        | `flex`                |
| height         | `h-screen`            |
| justifyContent | `justify-center`      |
| left           | `left-0`              |
| pointerEvents  | `pointer-events-none` |
| position       | `fixed`               |
| top            | `top-0`               |
| width          | `w-screen`            |
| zIndex         | `z-30`                |

### Modal Props

| Prop          | Default                                                                                                             |
| ------------- | ------------------------------------------------------------------------------------------------------------------- |
| bg            | `bg-white`                                                                                                          |
| class         | `""`                                                                                                                |
| display       | `flex`                                                                                                              |
| duration      | `duration-200`                                                                                                      |
| flexDirection | `flex-col`                                                                                                          |
| maxHeight     | `max-h-full`                                                                                                        |
| maxWidth      | `max-w-4xl`                                                                                                         |
| overflow      | `overflow-hidden`                                                                                                   |
| rounded       | `rounded`                                                                                                           |
| shadow        | `shadow`                                                                                                            |
| show          | `{ false : "opacity-0 pointer-events-none -translate-y-8", true : "opacity-100 pointer-events-auto translate-y-0"}` |
| transform     | `transform`                                                                                                         |
| transition    | `transition`                                                                                                        |

### Overlay Props

| Prop       | Default                                                                                |
| ---------- | -------------------------------------------------------------------------------------- |
| bg         | `bg-black`                                                                             |
| class      | `""`                                                                                   |
| duration   | `duration-200`                                                                         |
| height     | `h-screen`                                                                             |
| left       | `left-0`                                                                               |
| position   | `absolute`                                                                             |
| show       | `{ false : "opacity-0 pointer-events-none", true : "opacity-70 pointer-events-auto" }` |
| top        | `top-0`                                                                                |
| transition | `transition`                                                                           |
| width      | `w-screen`                                                                             |

### Title Bar Props

| Prop           | Default                    |
| -------------- | -------------------------- |
| border         | `border-b border-gray-300` |
| class          | `""`                       |
| display        | `flex`                     |
| justifyContent | `justify-between`          |
| padding        | `p-4`                      |
