# local-tabby
Empty Repository, required for using homebrew to manage a local tabby LLM service.

## Configuring mods

To use the locally served LLM with `mods`, you'll need to add the following
to your local `~/.config/mods/mods.yml` file, under the `apis` section:

```yaml
  tabby:
    base-url: http://localhost:9595/v1beta
    models:
      tabby:
        aliases: ["tabby"]
        max-input-chars: 98000
```

Next, set your `default` model to `tabby` instead of `gpt4`.

You can test it by running this command:

```bash
mods -f "Tell me about the company 37signals."
```
