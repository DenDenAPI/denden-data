# DenDen data

The open dataset behind [DenDen API](https://github.com/DenDenAPI/denden-api): structured One Piece data in YAML, with one file per record.

| Folder | Content |
| --- | --- |
| `characters/` | Characters |
| `devil-fruits/` | Devil fruits |
| `crews/` | Pirate crews |
| `organizations/` | Organizations |
| `locations/` | Islands, kingdoms and other places |
| `ships/` | Ships and vehicles |
| `sagas/` | Story sagas |
| `arcs/` | Story, filler, special and cover story arcs |
| `chapters/` | Manga chapters |
| `volumes/` | Manga volumes |
| `episodes/` | Anime episodes |

## Conventions

- The file name is the record slug, and slugs never change.
- Each relation is written on one side only. The API generates its inverse.
- `canon` is one of `manga`, `anime_only`, `movie` or `other`.
- Ranges are inclusive, and a `null` end means the range is still ongoing.

## Contributing

Fix or add a record in a pull request. CI checks its schema, relations and attribution. To run the same check locally, clone [`denden-api`](https://github.com/DenDenAPI/denden-api) next to this repository:

```shell
pnpm install
pnpm validate:data ../denden-data
```

The data may contain errors and has not been verified against the manga. Corrections are welcome.

## License and attribution

This dataset is licensed under [CC BY-SA 3.0](LICENSE.md). It contains material from [One Piece Wiki](https://onepiece.fandom.com/wiki/One_Piece_Wiki) at Fandom. `ATTRIBUTION.yaml` lists the source article for each record.

If you reuse this data, keep the attribution and share your adaptations under the same license.

One Piece is owned by Eiichiro Oda, Shueisha and Toei Animation. This is an unofficial fan project and grants no rights over that intellectual property.
