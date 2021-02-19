<script>
  export let bg = "bg-white";
  export let border = "border border-gray-300";
  export let display = "flex";
  export let flexDirection = "flex-col";
  export let padding = "p-8";
  export let rounded = "rounded";
  export let shadow = "shadow";

  $: classes = Object.values({
    bg,
    border,
    display,
    flexDirection,
    padding,
    rounded,
    shadow,
    props: $$props.class,
  }).join(" ");
</script>

<div class={classes}>
  <slot />
</div>
