# saucenao-go
A wrapper for the [SauceNao](https://saucenao.com/) API in Golang.

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
  -  This wrapper currently supports saucenao output of Pixiv and Danbooru. While these suited my own purposes, the wrapper could easily be extended to support other source websites. The fields, which can be found in the JSON of the response object, can be added in the `SaucenaoResultData` struct.
  -  Currently it is only possible to provide URLs as input. Support for `image` of the standard library might be added somewhere in the near future. As a workaround, you could use one of the various imgur wrappers for Go to get a URL for your image.
