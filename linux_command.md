## xargs curl with option
cat url.txt | xargs -P0 -n3 -t curl -X POST >/dev/null

->url.txt :-d "name=test" localhost:8000
