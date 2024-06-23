## Web Fuzzer
Source: https://github.com/ffuf/ffuf

### Build
```
docker build -t ffuf .
```
### Example
```
docker run --rm -v $(pwd)/wordlist.txt:/wordlist.txt ffuf -w /wordlist.txt -u https://targetsite.com/FUZZ
```
