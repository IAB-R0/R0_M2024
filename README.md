# R0_M2024
Точный и быстрый расчёт движения астероидов в Солнечной системе

Архив содержит две похожих программы вместе с файлом используемых эфемерид. Программа R0_HP производит расёт траектории одного астероида. R0_M2024, соответственно, для большого количества астероидов. В приложенных файлах ввода задаются начальные координаты, скорости и параметры негравитационных эффектов (отдельно для каждого астероида). Расчёт обеими программами идентичен, но R0_M2024 позволяет достичь в 5 раз более высокой производительности.

==================

Компиляция (Linux, gcc):

gcc R0_HP.c -lm -O3 -o R0_HP

gcc R0_M2024.c -lm -O3 -o R0_M2024

==================

Файлы ввода-вывода:

XV0.dat -> R0_HP -> XV1.dat

input.dat -> R0_M2024 -> output.dat

==================

Текущая версия создана для демонстрации работы метода расчёта траекторий и обладает некоторыми ограничениями. Расчёт производится только вперёд во времени и конечный промежуток времени кратен 4 дням. Выводятся только конечные координаты и скорости. Параметры негравитационных эффектов задаются в файле ввода и не меняются со временем.
