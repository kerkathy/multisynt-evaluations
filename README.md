# MultiSynt Nemotron-CC Models by Language

Models follow the naming convention `MultiSynt/nemotron-cc-{language}-{translation-model}`.

| Language   | tower9b | tower72b | opus | include | belebele | flores |
|------------|:-------:|:--------:|:----:|:-------:|:--------:|:------:|
| Basque     | ✗       | ✗        | ✓    | ✓       | ✗        | ✗      |
| Catalan    | ✗       | ✗        | ✓    | ✗       | ✗        | ✗      |
| Danish     | ✓       | ✗        | ✓    | ✗       | ✓        | ✓      |
| Dutch      | ✓       | ✗        | ✓    | ✓       | ✓        | ✓      |
| Finnish    | ✓       | ✓        | ✓    | ✓       | ✓        | ✓      |
| French     | ✓       | ✗        | ✓    | ✓       | ✓        | ✓      |
| German     | ✓       | ✓        | ✓    | ✓       | ✓        | ✓      |
| Icelandic  | ✓       | ✗        | ✓    | ✗       | ✗        | ✗      |
| Italian    | ✓       | ✓        | ✓    | ✓       | ✓        | ✓      |
| Norwegian  | ✓       | ✗        | ✗    | ✗       | ✗        | ✗      |
| Polish     | ✓       | ✗        | ✓    | ✓       | ✓        | ✓      |
| Portuguese | ✗       | ✗        | ✓    | ✓       | ✓        | ✓      |
| Romanian   | ✓       | ✗        | ✓    | ✗       | ✓        | ✓      |
| Spanish    | ✓       | ✓        | ✓    | ✓       | ✓        | ✓      |
| Swedish    | ✓       | ✓        | ✓    | ✗       | ✓        | ✓      |

## Analysis

Unlike HPLT2 monolingual models, no model has intermediate checkpoints available.

### Model coverage
- **Full coverage** (all 3 models): Finnish, German, Italian, Spanish, Swedish
- **Missing tower72b only**: Danish, Dutch, French, Icelandic, Polish, Romanian
- **Missing tower9b + tower72b**: Basque, Catalan, Portuguese
- **Missing opus only**: Norwegian
- Norwegian is the only language missing opus while having tower9b.

### Benchmark coverage
- **include**: Basque, Dutch, Finnish, French, German, Italian, Polish, Portuguese, Spanish (9/15 languages)
- **belebele**: Danish, Dutch, Finnish, French, German, Italian, Polish, Portuguese, Romanian, Spanish, Swedish (11/15 languages)
- **flores**: Danish, Dutch, Finnish, French, German, Italian, Polish, Portuguese, Romanian, Spanish, Swedish (11/15 languages)
- **No benchmark coverage**: Catalan, Icelandic, Norwegian
- **Only include (not belebele/flores)**: Basque
- **belebele and flores but not include**: Danish, Romanian, Swedish



Steps:
* evaluate multisynt models with tower72b > tower9B > opus on all languages
* evaluate hplt models on all languages
* add missing evaluation noreval etc in oellm-cli