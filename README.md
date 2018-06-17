# saucenao-go
A wrapper for the SauceNao API in Golang.

## Example 
```
  client := New("SAUCE_NAO_API_KEY_HERE")
  result, err := client.FromURL("DIRECT_LINK_TO_IMAGE_HERE")
  
  if err != nil {
		t.Errorf("Retrieving: %s", err)
	}
  
  // Retreive the source URL of the image.
  // Note that this could panic if saucenao could not find any matches.
  result.Data[0].Data.ExtUrls[0]
```

