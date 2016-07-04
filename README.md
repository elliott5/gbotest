Example of using go binary-only packages.

This example assumes you're on "darwin_amd64" with go version go1.7beta2 :		 

```		
go get github.com/elliott5/gbotest
# go to the repo
cd $GOPATH/src/github.com/elliott5/gbotest
# run the little test 
go run *.go		
# should have failed		
# now create the correct place to put the .a file
mkdir -p $GOPATH/pkg/darwin_amd64/github.com/elliott5/gbotest/vendor/github.com/elliott5/local
# now copy it over
cp $GOPATH/src/github.com/elliott5/gbotest/gboplay.a $GOPATH/pkg/darwin_amd64/github.com/elliott5/gbotest/vendor/github.com/elliott5/local 		
# now try agian
go run *.go		
# should have worked		
```		
		