# @bobthered/svelte-card

Svelte component for creating cards with tailwindcss

## Installation

```
npm i -D @bobthered/svelte-card
```

## Basic Usage

```
<script>
  import Card from '@bobthered/svelte-card'
</script>

<Card>Card Body</Card>
```

## Available Props

| Prop          | Default                  | Description                 |
| ------------- | ------------------------ | --------------------------- |
| bg            | `bg-white`               | Set bg class(s)             |
| border        | `border border-gray-300` | Set border class(s)         |
| class         | `""`                     | Add additional class(s)     |
| display       | `flex`                   | Set display class(s)        |
| flexDirection | `flex-col`               | Set flex direction class(s) |
| padding       | `p-8`                    | Set padding class(s)        |
| rounded       | `rounded`                | Set rounded class(s)        |
| shadow        | `shadow`                 | Set shadow class(s)         |
