### bleve
---
https://github.com/blevesearch/bleve

```go
message := struct{
  Id string
  From string
  Body string
}{
  Id: "example",
  From: "marty.schoch@gmail.com",
  Body: "bleve indexing is easy",
}

index, _ := bleve.Open("example.bleve")
query := bleve.NewQueryStringQuery("bleve")
searchRequest := bleve.NewSearchRequest(query)
searchResult, _ := index.Search(searchRequest)
```

```go
import "github.com/blevesearch/blev"

func main() {
  mapping := bleve.NewIndexMapping()
  index, err := bleve.New("example.bleve", mapping)
  
  err = index.Index(identifier, your_data)
  
  query := bleve.NewMatchQuery("text")
  search := bleve.NewSearchRequest(query)
  searchResults, err := index.Search(search)
}
```

```
```


