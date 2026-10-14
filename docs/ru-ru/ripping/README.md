# Риппинг

## Риппинг компакт-дисков

Для риппинга я использую [Exact Audio Copy v1.8](https://www.exactaudiocopy.de/) и привод ASUS SDRW-08D2S-U Lite.  
Данная модель полностью пригодна для точного извлечения аудиоданных с диска, однако она не имеет постоянного оффсета (возможно из-за различий партий или прошивок). Для калибровки привода в Exact Audio Copy необходимо три тестовых диска, которые уже находятся в базе данных [AccurateRip](https://www.accuraterip.com/).  
Подробнее об этом можно узнать на [странице AccurateRip, посвященной оффсетам приводов](https://accuraterip.com/driveoffsets.htm).

Для проверки логов рипа (log score) с компакт-дисков я использую [cambia](https://logs.musichoarders.xyz/).

> [!TIP]
> О риппинге можно прочитать в [MusicHoarders вики](https://musichoarders.xyz/guides/ripping-cds/).  
>
> Я следую этим инструкциям для получения 100% лога в cambia:
>
> - Настройки Exact Audio Copy: [MusicHoarders вики](https://musichoarders.xyz/guides/ripping-cds/ripping-on-windows/#setup) и [DoujinStyle](https://doujinstyle.com/eac/setup.html).  
> - Процесс риппинга на Windows: [MusicHoarders вики](https://musichoarders.xyz/guides/ripping-cds/ripping-on-windows/#ripping) и [DoujinStyle](https://doujinstyle.com/eac/ripping.html).

## .cue, .log и .accurip файлы

Файлы `.cue`, `.log` и `.accurip` именуются по шаблону `CD<Номер диска>`: `CD1.cue`, `CD1.log`, `CD1.accurip`, `CD2.cue` и так далее.  
Если релиз состоит всего из одного диска, то номер диска опускается: `CD.cue`, `CD.log`, `CD.accurip`.

Я генерирую `.accurip` файлы с помощью [CUETools v2.2.6](https://cue.tools/wiki/CUETools) для повторной верификации сторонних рипов по базам данных [AccurateRip](https://www.accuraterip.com/) и [CTDB](https://cue.tools/wiki/CUETools_Database).
