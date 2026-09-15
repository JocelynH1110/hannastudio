## Handover doc

`HANDOVER.md` is not committed in plaintext — this repo is public, and it
contains internal notes not meant for public visibility. The encrypted
version, `HANDOVER.md.age`, is tracked instead (encrypted with `age` for
GitHub users JocelynH1110 and moroz's SSH keys as recipients).

To read it, decrypt with a matching SSH private key:

```
age -d -i ~/.ssh/id_ed25519 HANDOVER.md.age > HANDOVER.md
```

To update it: edit the decrypted `HANDOVER.md`, then re-encrypt and
re-stage the `.age` file (the plaintext stays gitignored):

```
age -r <recipient1> -r <recipient2> ... -o HANDOVER.md.age HANDOVER.md
```

## Development

When starting the dev server, use background mode:

```
astro dev --background
```

Manage the background server with `astro dev stop`, `astro dev status`, and `astro dev logs`.

## Documentation

Full documentation: https://docs.astro.build

Consult these guides before working on related tasks:

- [Adding pages, dynamic routes, or middleware](https://docs.astro.build/en/guides/routing/)
- [Working with Astro components](https://docs.astro.build/en/basics/astro-components/)
- [Using React, Vue, Svelte, or other framework components](https://docs.astro.build/en/guides/framework-components/)
- [Adding or managing content](https://docs.astro.build/en/guides/content-collections/)
- [Adding styles or using Tailwind](https://docs.astro.build/en/guides/styling/)
- [Supporting multiple languages](https://docs.astro.build/en/guides/internationalization/)
