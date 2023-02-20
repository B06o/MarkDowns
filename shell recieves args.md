# How to recieve args via "-"



```
#!/bin/bash


while getopts ":a:b:c" opt ;
do
    case $opt in
    a)  echo "I got a, whose value is: $OPTARG"
    ;;
    b)  echo "Hi there I got a b: $OPTARG"
    ;;
    c)  echo "Yeah I got a b: $OPTARG"
    ;;
    
    # unknown options would raise abort.
    ?)  echo "wtf are you talking about?"
        exit 1
    ;;
    esac
done


```

