<script>
  export let href = "";
  export let type = "link";

  // styling
  export let bg = "bg-primary-500 hover:bg-white";
  export let cursor = "cursor-pointer";
  export let display = "inline-flex";
  export let duration = "duration-200";
  export let fontSize = "text-sm";
  export let fontWeight = "font-medium";
  export let items = "items-center";
  export let outline = "focus:outline-none";
  export let padding = "py-4 px-10";
  export let rounded = "rounded";
  export let textColor = "text-white hover:text-primary-500";
  export let textTransform = "uppercase";
  export let transition = "transition";

  let classes = {
    bg,
    cursor,
    display,
    duration,
    fontSize,
    fontWeight,
    items,
    outline,
    padding,
    rounded,
    textColor,
    textTransform,
    transition,
  };

  $: clazz = [...Object.values(classes), $$props.class].join(" ");
</script>

{#if type === 'link'}
  <a {href} class={clazz} on:click><slot /></a>
{:else if type === 'submit'}
  <button type="submit" class={clazz} on:click><slot /></button>
{/if}
