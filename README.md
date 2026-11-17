# Sail to Lead: Water Sports for Youth Work

Статичний сайт (GitHub Pages). Головна сторінка: `index.html`.

## Структура
- `index.html`: уся сторінка (дві мови UA/EN, стилі та скрипти всередині)
- `assets/photos/`: фото для каруселі
- `assets/logos/`: логотипи Erasmus+ та Co-funded by the EU
- `assets/deck/<мова>/`: слайди презентації як картинки (`s-01.jpg`, `s-02.jpg` ...)
- `downloads/`: PDF для завантаження

## Як додати презентацію іншою мовою (en або sk)
1. Покладіть PDF у `downloads/`, наприклад `Sail_to_Lead_presentation_EN.pdf`.
2. Перетворіть його на слайди (потрібен poppler):
   `mkdir -p assets/deck/en && pdftoppm -jpeg -jpegopt quality=68 -scale-to-x 1100 -scale-to-y -1 downloads/Sail_to_Lead_presentation_EN.pdf assets/deck/en/s`
3. В `index.html` знайдіть рядок `var D={uk:{...},en:null,sk:null};` і замініть `en:null` на
   `en:{n:КІЛЬКІСТЬ_СЛАЙДІВ,dir:'assets/deck/en/',pdf:'downloads/Sail_to_Lead_presentation_EN.pdf'}`
   (для словацької так само з `sk`). Кнопка мови активується автоматично.

## Що ще треба уточнити
- Ліцензія та дата останньої перевірки у футері (зараз «буде уточнена»).
- Розділи матеріалів позначені «Незабаром», доки групи не передали фінальні версії.
