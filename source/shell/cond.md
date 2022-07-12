# 条件判断

## if

```shell
if [ $# -lt 2 ];then
    echo "usage: zwg <-e/-s/-t> <file>"
    exit 1
else
	echo "hello"
fi
```

## case

```shell
ARG=$1

case $ARG in
    -e)
    echo "-e"
    ;;

    -s)
    echo "-s"
    ;;

    -t)
    echo "-t"
    ;;
esac
```
