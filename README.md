# gtranslate!

This is fork of https://github.com/bregydoc/gtranslate repository.

Google Translate API for unlimited and free translations 📢.
This project was inspired by [google-translate-api](https://github.com/matheuss/google-translate-api) and [google-translate-token](https://github.com/matheuss/google-translate-token).

# Install

    go get github.com/Stanly1995/gtranslate

# Use

```go
gtranslate.Translate("I'm alive", language.English, language.Spanish)
```

```go
gtranslate.TranslateWithParams("I'm alive", gtranslate.TranslateWithParams{From: "en", To: "es"})
```

# Example

```go
package main

import (
	"fmt"

	"github.com/Stanly1995/gtranslate"
)

func main() {
	text := "Hello World"
	translated, err := gtranslate.TranslateWithParams(
		text,
		gtranslate.TranslationParams{
			From: "en",
			To:   "ja",
		},
	)
	if err != nil {
		panic(err)
	}

	fmt.Printf("en: %s | ja: %s \n", text, translated)
	// en: Hello World | ja: こんにちは世界
}
```
