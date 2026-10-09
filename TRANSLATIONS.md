# Add a language / Додати мову

1. In the app click **Save translation template…**, or copy `translations/template.json` from this repository.
2. Change `id` to the language code, e.g. `de`, `fr`, `pl`, or `pt-BR`. Use two or three lowercase letters, optionally followed by a regional subtag. File names are normally `<id>.json`.
3. Change `name` to the language's native name, e.g. `Deutsch`.
4. Translate the VALUES in `strings`. Keep the keys unchanged. Preserve placeholders such as `{device}` exactly.
5. Save as UTF-8 JSON. In the app click **Add language from file…**, select the file, and review the translated interface.
6. To share it, submit a pull request adding your JSON file to this repository's `translations/` directory.

The app accepts partial translations and uses English for missing keys. Unknown keys, wrong placeholders, unsafe IDs, empty values, and files larger than 128 KiB are rejected. Built-in `en` and `uk` cannot be overridden via file import; improvements can be proposed here and included in a future app release.

Example of a partial translation:

```json
{
  "id": "de",
  "name": "Deutsch",
  "strings": {
    "heading": "Mikrofonpriorität",
    "current_input": "Aktuell verwendet: {device}"
  }
}
```

Installed translations are stored in `~/Library/Application Support/MacInputGuard/Translations/`. Files are never downloaded automatically. Close and reopen the app after editing a previously imported file on disk, or import its new version through the app.

## Українською

Збережи шаблон через кнопку у програмі або скопіюй `translations/template.json`, зміни `id` та `name`, переклади значення в `strings`, зберігаючи ключі й підстановки `{device}`. Додай файл через кнопку у програмі. Щоб поділитися перекладом, створи pull request у цей репозиторій. Відсутні рядки підставляються з англійської; змінювати вихідний код або збирати програму не потрібно.
