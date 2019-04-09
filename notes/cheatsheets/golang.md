## Iterate over elements of a slice or array:

### index and value
`for i, v := range slice {}`

### index only
`for i := range slice {}`

### value only
`for _, v := range slice {}`

## Open a file:
```go
file, err := os.Open("path/to/file")
    if err != nil {
        log.Fatal(err)
    }
	defer file.Close()
```
## Read a file line by line:
```go
scanner := bufio.NewScanner(file)
    for scanner.Scan() {
		// Do yo thang
	}
```
