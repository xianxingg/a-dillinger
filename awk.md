```awk
    # print first column
    awk '{ print $1}' src.txt
    
    # print line number
    awk '{ n++ } END { print n }' src.txt
    awk 'END { print NR }'
    
    # pipe who.count()
    awk 'BEGIN { { while ( "who" | getline ) n++ } print n }'
    who | awk '{ n++ } END { print n }'
    
    # word-start-with-A / min-value 100
    $1 ~ /^A.*/ { $3 *= 1.05 } $3 < 100 { $3 = 100 }
    
    # set ( array ) count
    awk '{ for (i = 2; i <= NF; i++) Numbers[$i] ++ } END { for (course in Numbers) printf("%10s %d\n", course, Numbers[course] }' src.txt
    
    # redirect
    awk 'BEGIN { print "header" > "outFile.txt"  }'
    
    # # # 2:18 @ 5.24 2015
    # 7.2
    # http://www.blogjava.net/jasmine214--love/archive/2011/01/25/343478.html
    # http://www.360doc.com/content/11/1211/17/3508740_171494913.shtml
```
