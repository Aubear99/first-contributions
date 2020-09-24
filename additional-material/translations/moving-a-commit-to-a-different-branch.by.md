# Перамяшчэнне камітаў ў іншую галінку
Што рабіць, калі вы здзяйсняеце змены, а потым разумееце, што вы здзейснілі іншую галіну?
Як вы можаце гэта змяніць? Вось што ахоплівае гэты падручнік.

## Перамяшчэнне апошніх камітаў ў існуючую галінку
Для такога перамяшчэння, набярыце:

`` `git reset HEAD ~ --soft` `` - Адмяняе апошняе commit, але пакідае даступныя змены.
`` `git stash` `` - Захоўвае стан дырэкторыі.

`` `git checkout <імя правільнай галінкі>` `` - Перамыкаецца на іншую галінку.
`` `git stash pop` `` - Вяртае апошняе захаванае стан.
`` `git add .` `` - Дадае індывідуальныя файлы.
`` `git commit -m "your message here"``` - Захоўвае і ўносіць змены.

Зараз вашы змены - у правільнай галінцы.


### Перамяшчэнне апошніх камітаў ў новую галінку
Для такога перамяшчэння, набярыце:
`` `git branch newbranch` `` - Стварае новую галінку, захоўваючы ўсе камітаў.
`` `git reset --hard HEAD ~ [n]` `` - Вяртае галінку master назад на n камітаў. Майце на ўвазе, што змены змяшчаюцца ў гэтых камітаў будуць цалкам выдалены з галінкі master.
`` `git checkout newbranch` `` - Перамыкаецца на галінку, якую вы стварылі. Гэтая галінка цяпер змяшчае ўсе commits.

Запомніце: Любыя змены, якія не былі ўключаныя ў commit, будуць цалкам страчаныя.