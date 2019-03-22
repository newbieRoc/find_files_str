#!/bin/sh
find_str(){

        for file in `ls $1`
        do
                #echo $file
                if test -f $1"/"${file}
                then
                        ret=`cat $1"/"${file} | grep -c $2`
                        if test $ret -gt 0
                        then
                                echo ">>>>>> "$1"/"${file} 
                        fi
                elif test -d $1"/"${file}
                then
                #       echo $1"/"${file}":dir"
                        find_str $1"/"${file} $2

                #else
                #       echo "???"
                fi

        done
}
find_str $1 $2
