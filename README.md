Example of using go binary-only packages.

For this example to work, do NOT "go get github.com/elliott5/gboplay"

This example assumes you're on "darwin_amd64" with go version go1.7beta2 :		 

```		
# get this repo
go get github.com/elliott5/gbotest
# run the little test 
go run $GOPATH/src/github.com/elliott5/gbotest/*.go		
# should have failed		
# now create somewhere to put the .a file
mkdir -p $GOPATH/pkg/darwin_amd64/github.com/elliott5/gbotest/test/vendor/github.com/elliott5 		
# now copy it over
cp $GOPATH/src/github.com/elliott5/gboplay.a $GOPATH/pkg/darwin_amd64/github.com/elliott5/gbotest/vendor/github.com/elliott5 		
# now try agian
go run $GOPATH/src/github.com/elliott5/gbotest/*.go		
# should have worked		
```		
		