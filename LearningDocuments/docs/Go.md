# GO Useeful tricks

## Skip test based on tag
More info on (ReferenceLink)[https://stackoverflow.com/questions/24030059/skip-some-tests-with-go-test]
Must read Blog(GOLang Skipe Tests)[https://blog.dharnitski.com/2019/04/29/skip-tests-in-go/]
```
// +build !feature1

package tags

import "testing"

func TestB(t *testing.T) {}


go test -v -tags feature1 
```

## Clean cache
```
go clean -testcache
go test -count=1

```

## Code Coverage gocov
May be outdated but using this toll can integraed in CICD pipeline
(GO COde Coverage) [https://blog.dharnitski.com/2019/04/28/golang-coverage-circleci/]
```
go-acc ./...
```