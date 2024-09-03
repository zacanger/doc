# jq

`jq` is a command-line tool for working with JSON.

Use your package manager to get it, or build it from source.

See [GitHub](https://github.com/stedolan/jq).

* Pretty-print JSON.

    jq

* Print JSON in a compact format.

    jq -c

* Print the sum of a list of numbers. `-s` (`--slurp`) creates an array for the input lines after parsing each line as JSON, or as a number in this case.

    jq -s add

* Print the maximum of a list of numbers.

    jq -s max

* Print the average of a list of numbers.

    jq -s add/length

* Print the RMS of a list of numbers, like `awk '{x+=$0*$0}END{print sqrt(x/NR)}'`.

    jq -s 'map(.*.)|add/length|sqrt'

* Print the length of the longest line, like `wc -L` in GNU `wc`. `-R` (`--raw-input`) treats each input line as a string.

    jq -R length|jq -s max

* Apply percent encoding. `-sR` reads the input into a single string. `-r` (`--raw-output`) outputs the contents of strings instead of JSON string literals.

    jq -sRr @uri

* Escape HTML or XML, like `xml esc` or `recode ..xml`.

    jq -sRr @html

* Print the number nearest to 50 on a list of numbers.

    jq -s 'min_by(.-50*.-50)'

* Like `awk '$0<100{exit 1}'`. `-e` sets the exit status to 1 if the last output value is false or null.

    jq -es 'map(.>=100)|all'>/dev/null

* Round each number on a list of numbers down to the nearest multiple of 20.

    jq -R 'tonumber/20|floor*20'

* Like `awk 'length<=80'`.

    jq -Rr 'select(length<=80)'

* Sort a single line list where items are delimited by a comma followed by a space, like `gsed 's/, /\n/g'|sort|sed '$!s/$/, /'|paste -sd\\0 -`. The `/` operator is overloaded to split strings.

    jq -Rr './", "|sort|join(", ")'

* Convert a list of lines into a JSON array of strings. `jq -R .` prints each input line as a JSON string literal so that the input can be slurped with `-s`.

    jq -R .|jq -s .

* Sort by length, like `awk '{print length,$0}'|sort -n|cut -d' ' -f2-`.

    jq -R .|jq -sr 'sort_by(length)[]'

* Like `sort -t\; -uk3,3`. `unique_by` also sorts items.

    jq -R .|jq -sr 'unique_by(split(";")[2])[]'

* Like `x="$x" awk '{print ENVIRON["x"]$0}'`.

    jq --arg x "$x" -Rr '$x+.'

* Transpose a matrix, like `rs -c' ' -C' ' -T`.

    jq -R .|jq -sr 'map(./" ")|transpose|map(join(" "))[]'

* Print lines that end with the specified string.

    jq --arg x "$string" -Rr 'select(endswith($x))'

* Print the product of a list of numbers.

    jq -s 'reduce.[]as$x(1;.*$x)'

* Print the factorial of 6. `-n` is `--null-input`. The end point for `range` is exclusive like in Python.

    jq -n 'reduce range(1;7)as$x(1;.*$x)'

* Merge JSON files.

    jq -s add *.json

* Merge two JSON files recursively. The `*` operator is overloaded to merge objects recursively.

    jq -s '.[0]*.[1]' [12].json

* Merge multiple JSON files recursively.

    jq -s 'reduce.[]as$x({};.*$x)' *.json

* Print 2-tuples (2-permutations with repetition) of the letters a, b, and c, like `printf %s\\n {a,b,c}{a,b,c}`.

    jq -nr '"abc"/""|combinations(2)|join("")'

* Subtract the minimum number from each number a list of numbers.

    jq -s 'min as$x|map(.-$x)[]'

* Like `awk '{if(/pattern/)print;else x=x$0"\n"}END{printf"%s",x}'`. `test` is like `match` but it only returns true or false instead of a match object.

    jq -R .|jq -sr 'group_by(test("pattern")|not)[][]'

* Like `while IFS= read -r l;do printf %s\\n "${x//aa/$l}";done`.

    jq --arg x "$x" -Rr '. as$in|$x|gsub("aa";$in)'

* Like `pcregrep -M -o1 -o2 --om-separator=' ' '(?s)<a href="([^"]*)">MP3 Download.*?Rated <strong>([^<]*)'`.

    jq -Rsr 'scan("(?s)<a href=\"([^\"]*)\">MP3 Download.*?Rated <strong>([^<]*)")|join(" ")'

* Like `grep -Ff file1 file2`.

    jq --slurpfile a <(jq -R . file1) -Rr '. as$in|select($a|map(inside($in))|any)' file2

* Like `awk '{split($3,a,"/");$3=a[5]}1' FS=\; OFS=\;`. `|=` is the update operator.

    jq -Rr './";"|.[2]|=(./"/")[4]|join(";")'

* Print the geometric mean of a list of numbers, like `awk '{x*=$0}END{print x^(1/NR)}' x=1`.

    jq -s 'length as$l|reduce.[]as$x(1;.*$x)|pow(.;1/$l)'

* Like `awk '{if(length<=80)print;else x=x$0"\n"}END{printf"%s",x}'`.

    jq -R .|jq -sr 'group_by(length>80)[][]'

* Like `awk -F\; 'NR==FNR{a[$0]=NR;next}{print a[$3],$0}' file1 file2|sort -n|cut -d' ' -f2-`, assuming that `file1` contains each line only once.

    jq -R . file2|jq --slurpfile a <(jq -R . file1) -s 'sort_by((./";")[2]as$x|$a|indices($x))'

* Print the standard deviation of a list of numbers, like `awk '{x+=$0;y+=$0^2}END{print sqrt(y/NR-(x/NR)^2)}'`.

    jq -s '(map(.*.)|add/length)-pow(add/length;2)|sqrt'

* Like `grep -Fxf file1 file2;grep -Fxvf file1 file2`.

    jq -R . file2|jq --slurpfile a <(jq -R . file1) -rs 'group_by([.]|inside($a))[][]'

* Scale a list of numbers so the smallest number becomes 0.0 and the largest becomes 1.0.

    jq -rs 'min as$min|max as$max|map((.-$min)/($max-$min))[]'

* Floor each number on a list of numbers, like `awk '{x=int($0);print(x==$0||$0>0)?x:x-1}'`.

    jq -s 'map(floor)[]'

* Round each number on a list of numbers down to a multiple of 100.

    jq -s 'map(./100|floor|.*100)[]'

* Count how many numbers are between each multiple of 100 on a list of numbers, where the start of each block is inclusive and the end is exclusive.

    jq -sr 'map(./100|floor|.*100)|group_by(.)[]|(length|tostring)+" "+(.[0]|tostring)'

* Print the sum of numbers in each column in a table of numbers where columns are separated by tabs, assuming that each row has the same number of columns.

    jq -R .|jq -sr 'map(./"\t"|map(tonumber))|transpose|map(add|tostring)|join("\t")'

* Sort a Markdown file that consists of sections that start with second level ATX headings by the headings. `(?s)` makes period match a newline and `(?m)` makes `^` match the start of a line and `$` match the end of a line.

    jq -Rsr '[scan("(?sm)^## .*?(?=\n\n## |\\Z)")]|sort|join("\n\n")'

* Print the lines of the input that contain all substrings in `substrings.txt`.

    jq --slurpfile a <(jq -R . substrings.txt) -Rr 'select(. as$in|$a|map(inside($in))|all)'

* Reverse words on each line, like `awk -F'[ ]' '{for(i=NF;i>=1;i--)printf"%s",$i (i==1?"\n":" ")}'`.

    jq -Rr './" "|reverse|join(" ")'

* Sort lines by the number of lines of the input whose second field the second field is.

    jq -R .|jq -sr 'group_by((./" ")[1])|sort_by(length)[][]'

* Like `sort|uniq -c|awk '$1<=2'|sed 's/^ *[^ ]* //'` but without sorting.

    jq -R .|jq -sr 'group_by(.)[]|select(length<=2)[0]'

* Open a `spotify:` URL for the first Spotify search result. Without `//empty` the `jq` command would print `null` when the result of the filter is null.

    curl -sG --data-urlencode q='Artist - Title' 'https://api.spotify.com/v1/search?type=track'|jq -r '.tracks.items[0].uri//empty'|xargs open -g

* Print the WikiText source of a Wikipedia article. `."*"` selects a key whose name consists of an asterisk.

    curl -s 'https://en.wikipedia.org/w/api.php?action=query&prop=revisions&rvprop=content&format=json&titles=Example'|jq -r '.query.pages[].revisions[]."*"'

* Get similar artists for an artist from Last.fm.

    curl -s "http://ws.audioscrobbler.com/2.0/?api_key=$lastfmapi&format=json&method=artist.getsimilar&artist=$artist"|jq -r '.similarartists.artist[].name'

