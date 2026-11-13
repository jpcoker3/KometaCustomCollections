# Kometa franchise YAML files

Each YAML file contains one collection definition and, where supplied in the original
MoviePosters.yml, matching individual movie poster metadata.

## Install

Place this folder in your Kometa config directory, for example:

`/config/Franchises/`

Then add the folder under BOTH sections in your main `config.yml`:

```yaml
libraries:
  Movies:
    collection_files:
      - folder: config/Franchises

    metadata_files:
      - folder: config/Franchises
```

If your Quickstart configuration already has `collection_files` or `metadata_files`,
add the folder entry to the existing lists rather than replacing them.

## Files

- HarryPotter.yml — Harry Potter collection + 8 movie posters
- Batman.yml — Batman collection
- DC.yml — DC Movies collection
- Marvel.yml — Marvel Movies collection
- Scream.yml — Scream collection
- Avatar.yml — Avatar collection + 3 movie posters
- MonsterVerse.yml — MonsterVerse Extended collection + 6 supplied movie posters
- ScaryMovie.yml — Scary Movie collection + 6 movie posters
- ToyStory.yml — Toy Story collection + 5 movie posters
- VHS.yml — V/H/S collection
- Pixar.yml — Pixar Movies collection
- FinalDestination.yml — Final Destination collection + 6 movie posters
- Tron.yml — Tron collection + 3 movie posters

## Notes on source cleanup

- Fixed the indentation of the Scary Movie 2 poster entry so the YAML is valid.
- Corrected `yer: 2005` to `year: 2005` for King Kong (2005), so Kometa can use the supplied year match.
- Preserved the supplied Scary Movie (2026) match title/year pairing (`title: Scary Movie`, `year: 2026`) rather than guessing a different Plex title.
- Kept King Kong (2005) in MonsterVerse.yml because it appeared in the MonsterVerse section of the supplied poster file. It is not added to the collection builder itself; the collection's TMDb IDs remain exactly as supplied.
- No individual posters were invented for collections that had no matching entries in the supplied MoviePosters.yml.
- The original sort title `+012_Tron` is preserved, even though it shares the numeric prefix `+012` with Final Destination.
