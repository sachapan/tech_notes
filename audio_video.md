# Audio and Video related

## increase volume with ffmpeg

`ffmpeg -i input.mkv -filter:a "volume=4.0" output.mkv`

## Convert all .avi files to .mkv

`for i in *.avi; do ffmpeg -i "$i" "${i%.*}.mkv"; done`

## Re-encode a directory tree to H265 recursively

`find /path/to/media -iname '*.mkv' -exec ffmpeg -n -i '{}' -map 0 -map_metadata 0 -c:v libx265 -crf 24 -preset veryslow -c:a libopus -scodec copy '{}'.h265 \;`
