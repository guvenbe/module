go mod init example.com/module
go test
go get rsc.io/sampler
go get rsc.io/quote
go get rsc.io/sampler@v1.99.99
go list -m -versions rsc.io/sample
go list -m al

#### Manuall install go
cd ~
mkdir exampledir
cd exampledir
mkdir golang_1_15
cd golang_1_15
#assume the following go install package was downloaded from the official site already:
tar -xzvf ~/Downloads/go1.15.3.linux-amd64.tar.gz
cd ..
ln -s golang_1_15/go go

export GOROOT=/home/myusername/exampledir/go
export PATH=$PATH:$GOROOT/bin

go build
go install
go package

● go build
○ builds go code; if code is package main, it creates a binary executable and drops it in the package main’s
folder; if code is just a package, it builds it then throws away the binary.
● go install
○ builds and installs go code; if code is package main, it creates a binary executable and drops it in the
workspace’s bin folder; if code is a package, it builds it then drops it in the pkg folder (a file with a .a
extension)
● import
○ import path is everything after the “src” folder in your workspace
○ use the last folder in the import path to reference the package in your code
○ you can alias packages in your imports

https://go.dev/blog/using-go-modules
https://research.swtch.com/deps
https://teemukanstren.com/2020/10/27/understanding-golang-project-structure/