# HTTP-Haiku-Codes

Haiku Messages for HTTP Status Codes

---

## what's missing

To find info about where haikus are missing, run:

```bash
declare -a l
for f in ./codes/*; do
    if [[ $(cat "${f}" | jq '.messages|length') -lt 1 ]]; then
        l+=( "$(cat "${f}" | jq '.code')" )
    fi
done
printf "no haikus for: %s\n" "${l[*]}"
```

## stolen from

[3digitdev/Haiku-TTP-Codes](https://github.com/3digitdev/Haiku-TTP-Codes)

`(•_•)   ( •_•)>⌐■-■   (⌐■_■)`
