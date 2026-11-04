# Temporary Russian integration-test source

**Test-only repository. Do not select this source for ordinary learning.**
It is a separately authorized, disposable source for Ensō Nihongo's C5 integration checks,
not the official Russian edition or a translation-alignment checkpoint.

The initial `main` contains the exact 51 reviewed runtime files from
[`stop-cran/learning-japanese-ru` at `544dd15f6a07e53042bdb488b9d7a04da9685313`](https://github.com/stop-cran/learning-japanese-ru/tree/544dd15f6a07e53042bdb488b9d7a04da9685313):
12 kanji, 27 words and 12 unchanged stroke files. No learner data, exports, backups or
device captures are included. Original runtime hashes, licenses and notices are retained.
The [source translation ledger](https://github.com/stop-cran/learning-japanese-ru/blob/544dd15f6a07e53042bdb488b9d7a04da9685313/docs/translation-ledger.json)
and [independent teaching review](https://github.com/stop-cran/learning-japanese-ru/issues/3#issuecomment-6603245447)
remain the provenance records.

## Deliberately invalid fixtures

- `valid-pilot`: immutable initial valid content.
- `corrupt-hash`: one deliberately incorrect kanji checksum; content bytes remain unchanged.
- `repaired`: restores the correct manifest after `corrupt-hash`.
- `unsupported-language`: unsupported language metadata; not a new translation.
- `missing-language`: schema 2 without required language metadata.

During testing, `main` may advance through the corrupt and repaired commits to exercise
rejection and recovery of a real update to an already accepted repository. These faults
must never be copied into an official content repository. A failed or interrupted update
must retain last-known-good content, selected source/language and existing progress.

Text and derived dictionary data retain [CC BY-SA 4.0](LICENSE).
KanjiVG-derived strokes retain CC BY-SA 3.0; see [NOTICE](NOTICE.md).
Only this test README and explicitly documented manifest/configuration faults differ from
the public pilot. The normal Russian rollout remains disabled.
