# @bobthered/svelte-button

Svelte component for creating buttons with tailwindcss

## Installation

```
npm i -D @bobthered/svelte-button
```

## Basic Usage

```
<script>
  import Button from '@bobthered/svelte-button'
</script>

<Button>Click Here</Button>
```

## Available Props

| Prop          | Default                           | Description                                                      |
| ------------- | --------------------------------- | ---------------------------------------------------------------- |
| bg            | bg-primary-500 hover:bg-white     | Set bg class(s)                                                  |
| class         | _empty_                           | Add additional class(s)                                          |
| cursor        | cursor-pointer                    | Set cursor class(s)                                              |
| display       | inline-flex                       | Set display class(s)                                             |
| duration      | duration-200                      | Set duration class(s)                                            |
| fontSize      | text-sm                           | Set font size class(s)                                           |
| fontWeight    | font-medium                       | Set font weight class(s)                                         |
| items         | items-center                      | Set items class(s)                                               |
| href          | _empty_                           | If "type" prop is set to "link" use this to set the link address |
| outline       | focus:outline-none                | Set outline class(s)                                             |
| padding       | py-4 px-10                        | Set padding class(s)                                             |
| rounded       | rounded                           | Set rounded class(s)                                             |
| textColor     | text-white hover:text-primary-500 | Set text color class(s)                                          |
| textTransform | uppercase                         | Set text transform class(s)                                      |
| transition    | transition                        | Set transition class(s)                                          |
| type          | link                              | Set this to either "link" or "submit" to change node type        |
