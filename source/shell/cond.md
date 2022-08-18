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

	rp*)
	echo "rp0, rp1, rp2 ..."
	;;

	[2-5]
	echo "the num is 2 - 5"
	;;

    *)
    echo "unknown cmd $ARG"
    ;;
esac
```
