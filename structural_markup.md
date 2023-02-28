# Regex Structural Markdown Process: Acts

1. SPECIAL CHARACTERS FROM HELL.
1. replaced `\n{3,}` w `\n\n` to standardize whitespace
1. had to put `p` lines around every character AUGHHHHHH
1. `<p>([0-9])+\/([0-9])+\/([0-9])+<p>` w `<date d="\1" m="\2" y="\3">\0</date>` to capture dates of each post
1. for the purposes of this the commands are what are on TOP of the page
1. command tagging: `(.+?)(\n<date)` w `<command>\1</command>\2`
1. ok so i had to put a shit ton of whitespaces before every `<command>` to get this regex to work
1. `(<command>.+?)\n{3,}(\n)` w `<entry>\1</entry>\2`
1. normalized whitespace (eliminated) i.e. empty lines and spaces
1. manually (oh my god) put image text in `img-text` elements