# Риппинг

## Риппинг компакт-дисков

Для риппинга я использую [Exact Audio Copy v1.8](https://www.exactaudiocopy.de/) и привод ASUS SDRW-08D2S-U Lite.  
Этот привод полностью пригоден для точного извлечения аудиоданных с диска, однако он не имеет постоянного оффсета. Для его калибровки необходимо три тестовых диска, которые уже находятся в базе данных [AccurateRip](https://www.accuraterip.com/).  
Подробнее об этом можно узнать на [странице AccurateRip, посвященной оффсетам приводов](https://accuraterip.com/driveoffsets.htm).

> [!TIP]
> О риппинге можно прочитать в [MusicHoarders вики](https://musichoarders.xyz/guides/ripping-cds/).  
>
> Я следую этим инструкциям для получения 100% лога:
>
> - Настройки Exact Audio Copy: [MusicHoarders вики](https://musichoarders.xyz/guides/ripping-cds/ripping-on-windows/#setup) и [DoujinStyle](https://doujinstyle.com/eac/setup.html).  
> - Процесс риппинга на Windows: [MusicHoarders вики](https://musichoarders.xyz/guides/ripping-cds/ripping-on-windows/#ripping) и [DoujinStyle](https://doujinstyle.com/eac/ripping.html).

Для проверки логов рипа (log score) с компакт-дисков я использую [cambia](https://logs.musichoarders.xyz/).

## .cue, .log и .accurip файлы

Файлы `.cue`, `.log` и `.accurip` именуются по шаблону `CD<Номер диска>`: `CD1.cue`, `CD1.log`, `CD1.accurip`, `CD2.cue` и так далее.  
Если релиз состоит всего из одного диска, то префикс с номером опускается: `CD.cue`, `CD.log`, `CD.accurip`.

Я генерирую `.accurip` файлы с помощью [CUETools v2.2.6](https://cue.tools/wiki/CUETools) для повторной верификации сторонних рипов на основе существующих `.log` файлов.
