# Аварийное восстановление

#### Что делать, если диски виртуальной машины работают со сбоями

{% note warning %}

Не пытайтесь перезагрузить ВМ самостоятельно. Это может привести к потере данных.

{% endnote %}

Если вы заметили, что обращение к одному или нескольким дискам вашей ВМ происходит с ошибками:

1. [Создайте новый диск](../operations/disk-create/empty.md) и подключите его к виртуальной машине.
1. Скопируйте важные данные с поврежденных дисков на новый диск. Не используйте при чтении файлов флаг [O_DIRECT](https://man7.org/linux/man-pages/man2/open.2.html).
1. После того, как все важные данные скопированы, отключите поврежденные диски от ВМ и удалите их.
1. Если скопировать данные не удалось и диск важно сохранить, [напишите нам](https://console.cloud.yandex.ru/support). Мы сами выключим ВМ и проведем проверку целостности диска. Проверка может занять несколько дней.