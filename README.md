# saucenao-go
A wrapper for the SauceNao API in Golang.

Use `go get github.com/GenDoNL/saucenao-go` to install.

## Example 
```
client := New("SAUCE_NAO_API_KEY_HERE")
result, err := client.FromURL("DIRECT_LINK_TO_IMAGE_HERE")
  
if err != nil {
	fmt.Print("Error retrieving: %s", err)
}
  
// Retrieve the source URL of the image.
// Note that this could panic if saucenao could not find any matches.
result.Data[0].Data.ExtUrls[0]
```

## Limitations
  -  This wrapper currently only supports Pixiv and Danbooru. While these suited my purpose, the wrapper could easily be extended to support other source websites. They can be added in the `SaucenaoResultData` struct.
