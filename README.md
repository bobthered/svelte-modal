# @bobthered/svelte-input

Svelte component for creating inputs with tailwindcss

## Installation

```
npm i -D @bobthered/svelte-input
```

## Basic Usage

```
<script>
  import Input from '@bobthered/svelte-input'
</script>

<Input name="name" value="John Doe" />
```

## Attribute Props

| Prop        | Default | Description               |
| ----------- | ------- | ------------------------- |
| name        | `""`    | Set name attribute        |
| placeholder | `""`    | Set placeholder attribute |
| type        | `text`  | Set type attribute        |
| value       | `""`    | Set value attribute       |

## Class Props

| Prop       | Default                                                                      | Description             |
| ---------- | ---------------------------------------------------------------------------- | ----------------------- |
| bg         | `bg-transparent`                                                             | Set bg class(s)         |
| border     | `border-gray-300 border-b hover:border-primary-500 focus:border-primary-500` | Set border class(s)     |
| class      | `""`                                                                         | Add additional class(s) |
| duration   | `duration-200`                                                               | Set duration class(s)   |
| outline    | `focus:outline-none`                                                         | Set outline class(s)    |
| padding    | `py-2`                                                                       | Set padding class(s)    |
| textAlign  | `text-left`                                                                  | Set text align class(s) |
| transition | `transition`                                                                 | Set transition class(s) |
| width      | `width`                                                                      | Set width class(s)      |
