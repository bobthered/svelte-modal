<script>
  export let name = "";
  export let placeholder = "";
  export let type = "text";
  export let value = "";

  // style
  export let bg = "bg-transparent";
  export let border =
    "border-gray-300 border-b hover:border-primary-500 focus:border-primary-500";
  export let duration = "duration-200";
  export let outline = "focus:outline-none";
  export let padding = "py-2";
  export let textAlign = "text-left";
  export let transition = "transition";
  export let width = "w-full";

  let classes = {
    bg,
    border,
    duration,
    outline,
    padding,
    textAlign,
    transition,
    width,
    class: $$props.class,
  };
</script>

{#if type === 'email'}
  <input
    bind:value
    on:change
    on:keyup
    class={Object.values(classes).join(' ')}
    type="email"
    {name}
    {placeholder} />
{:else if type === 'number'}
  <input
    bind:value
    on:change
    on:keyup
    class={Object.values(classes).join(' ')}
    type="number"
    {name}
    {placeholder} />
{:else if type === 'text'}
  <input
    bind:value
    on:change
    on:keyup
    class={Object.values(classes).join(' ')}
    type="text"
    {name}
    {placeholder} />
{/if}
