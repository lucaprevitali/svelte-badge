<script>
  export let text = "default";
  export let ref;
</script>

<span {ref} class="svelte-badge">{text}</span>

<svelte:head>
  <style>
    .svelte-badge {
      padding: 4px;
      font-size: 12px;
      background-color: #edf2f7;
      color: #1a202c;
      text-transform: uppercase;
      font-weight: 700;
      border-radius: 2px;
    }
  </style>
</svelte:head>
