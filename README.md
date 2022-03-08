# Svelte Badge
Simple badge component made in Svelte

Try it in the [Svelte REPL](https://svelte.dev/repl/c54719faac3e4fedb6739a83bbd2f566)

## Installation

**Yarn**

```bash
yarn add -D svelte-badge
```

**NPM**

```bash
npm i -D svelte-badge
```

## Usage

### Basic

```svelte
<script>
  import Badge from "svelte-badge";
</script>

<Badge text="default" />
```

### Styling

Use the `ref` prop for overriding the style of a specific component.

```svelte
<div class="badges-container">
  <Badge text="default" />
  <Badge ref="success" text="success" />
  <Badge ref="removed" text="failed" />
</div>

<style>
  :global(.badges-container .svelte-badge) {
    font-size: 16px;
  }
  :global(.svelte-badge[ref="success"]) {
    color: #22543d;
    background-color: #c6f6d5;
  }
  :global(.svelte-badge[ref="removed"]) {
    color: #822727;
    background-color: #fed7d7;
  }
</style>

```

## Props

| Prop name      | Default value                            |
| :------------- | :--------------------------------------- |
| text           | `"default"`                              |
| ref            | `null`                                   |