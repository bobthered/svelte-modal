<script>
  // components
  import { X } from "@bobthered/svelte-heroicons/small";

  // defaults
  const defaults = {
    container: {
      alignItems: "items-center",
      class: "",
      display: "flex",
      height: "h-screen",
      justifyContent: "justify-center",
      left: "left-0",
      pointerEvents: "pointer-events-none",
      position: "fixed",
      top: "top-0",
      width: "w-screen",
      zIndex: "z-30",
    },
    modal: {
      bg: "bg-white",
      class: "",
      display: "flex",
      duration: "duration-200",
      flexDirection: "flex-col",
      maxHeight: "max-h-full",
      maxWidth: "max-w-4xl",
      overflow: "overflow-hidden",
      rounded: "rounded",
      shadow: "shadow",
      show: {
        false: "opacity-0 pointer-events-none -translate-y-8",
        true: "opacity-100 pointer-events-auto translate-y-0",
      },
      transform: "transform",
      transition: "transition",
    },
    overlay: {
      bg: "bg-black",
      class: "",
      duration: "duration-200",
      height: "h-screen",
      left: "left-0",
      position: "absolute",
      show: {
        false: "opacity-0 pointer-events-none",
        true: "opacity-70 pointer-events-auto",
      },
      top: "top-0",
      transition: "transition",
      width: "w-screen",
    },
    titleBar: {
      border: "border-b border-gray-300",
      class: "",
      display: "flex",
      justifyContent: "justify-between",
      padding: "p-4",
    },
  };

  // props
  export let closeable = true;
  export let container = {};
  export let modal = {};
  export let overlay = {};
  export let show = false;
  export let showTitleBar = true;
  export let title = "";
  export let titleBar = {};

  $: classes = {
    container: Object.values(Object.assign(defaults.container, container)).join(
      " "
    ),
    modal: Object.values(Object.assign(defaults.modal, modal))
      .map((value) => (typeof value === "string" ? value : value[show]))
      .join(" "),
    overlay: Object.values(Object.assign(defaults.overlay, overlay))
      .map((value) => (typeof value === "string" ? value : value[show]))
      .join(" "),
    titleBar: Object.values(Object.assign(defaults.titleBar, titleBar)).join(
      " "
    ),
  };

  const clickHandler = () => {
    if (closeable) show = !show;
  };
</script>

<div class={classes.container}>
  <div class={classes.overlay} on:click={clickHandler} />
  <div class={classes.modal}>
    {#if showTitleBar}
      <div class={classes.titleBar}>
        <div class="text-xl">{title}</div>
        <a href="#close" on:click|preventDefault={clickHandler} class="w-6 h-6">
          <X />
        </a>
      </div>
    {/if}
    <slot />
  </div>
</div>
