# Rename all jpg files to pdfs
`for file in `ls | grep jpg`; do echo $file | cut -f 1 -d . | { read myvar; mv "${myvar}.jpg" "${myvar}.pdf"; } done`

# Recursive wc 
`find <PATH> -type f | xargs wc -l`
