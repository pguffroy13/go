# GO

## INSTALL

- Download RPM 

```console
cd /var/tmp/
wget -k https://depot:443/.../go1.20.linux-amd64.tar.gz
```

- Install package

```console
sudo tar -C /usr/local -xzf go1.20.linux-amd64.tar.gz
```

- Add GO in ``$PATH``

```console
export PATH=/usr/local/go/bin:$PATH
which go
go version
```

- Remove package
  
```console
rm /var/tmp/go1.20.linux-amd64.tar.gz
```

- Test install

```console
cd
mkdir go
mkdir -p ~/go/src/hello
cd ~/go/src/hello
vi hello.go
```

```go
package main

import "fmt"

func main() {
    fmt.Printf("Hello, World\n")
}
```

- Compile 
  
```console
go env -w GO111MODULE=off
go build
./hello
```

- Execute
  
```sh
$ ./hello
Hello, World
```

