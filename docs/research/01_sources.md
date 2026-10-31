# Источники

## Правила добавления источника

1. Выдать новому источнику **следующий свободный идентификатор** `[S#]`. Существующие идентификаторы не менять, даже если источники впоследствии сортируются или удаляются из обзора.
2. Указать авторов, точное название, год, место публикации (если есть), DOI или устойчивую ссылку. Различать опубликованную статью и препринт.
3. Написать **краткую аннотацию по существу**: какой вход использован, что делает метод, что он выдаёт и чем полезен для темы.
4. Отметить существенные ограничения: класс объектов, число видов, необходимость разметки и степень проверенности результата.
5. При упоминании источника в других файлах использовать его идентификатор, например `[S3]`.

## Обзоры

**[S1]** Zhang C., Pinquié R., Polette A., Iida M., De Charnace H., Pernot J.-P. **3D CAD Models Reconstruction from 2D Drawings: A Survey and Future Challenges.** *Computer-Aided Design & Applications*, 23(6), 646–678, 2026. DOI: [10.14733/cadaps.2026.646-678](https://doi.org/10.14733/cadaps.2026.646-678). [Полный текст](https://cad-journal.net/files/vol_23/CAD_23%286%29_2026_646-678.pdf).

> Обзор подходов к восстановлению CAD по 2D-чертежам, классификация CSG-, B-Rep- и нейросетевых методов, обсуждение данных, метрик и нерешённых задач. Используется **для систематизации**, а не как первичный источник экспериментальных результатов отдельных алгоритмов.

**[S7]** Baumeister F., Bönsch J., Chaumet C., Dörr L., Meyer A. **Learning-based 3D CAD model generation in mechanical engineering: A survey.** *Advanced Engineering Informatics*, 76, article 104990, 2026 (опубликовано онлайн в 2026 году; журнальный выпуск датирован ноябрём). DOI: [10.1016/j.aei.2026.104990](https://doi.org/10.1016/j.aei.2026.104990). [Репозиторий KIT](https://publikationen.bibliothek.kit.edu/1000194899).

> Обзор обучаемых подходов к созданию CAD-моделей, их входов, выходных представлений, датасетов и метрик. Полезен для различения целевого CAD-результата и способов его генерации, а также для понимания, почему метрики разных экспериментов нельзя сравнивать напрямую.

## Исследования непосредственно по чертежам

**[S2]** Hu W., Zheng J., Zhang Z., Yuan X., Yin J., Zhou Z. **PlankAssembly: Robust 3D Reconstruction from Three Orthographic Views with Learnt Shape Programs.** *ICCV*, 18495–18505, 2023. [Статья](https://openaccess.thecvf.com/content/ICCV2023/html/Hu_PlankAssembly_Robust_3D_Reconstruction_from_Three_Orthographic_Views_with_Learnt_ICCV_2023_paper.html).

> **Вход:** три ортогональных линейных вида. **Метод:** Transformer генерирует shape programs. **Результат:** реконструируемая CAD-геометрия. **Ограничение:** программа и тестовые объекты соответствуют специальному классу форм; применимость к произвольным деталям требует проверки.

**[S3]** Wang X., Zheng J., Hu Y., Zhu H., Yu Q., Zhou Z. **From 2D CAD Drawings to 3D Parametric Models: A Vision-Language Approach.** *Proceedings of the AAAI Conference on Artificial Intelligence*, 39(8), 7961–7969, 2025. DOI: [10.1609/aaai.v39i8.32858](https://doi.org/10.1609/aaai.v39i8.32858). [Страница проекта CAD2Program](https://manycore-research.github.io/CAD2Program/).

> **Вход:** растровый чертёж. **Метод:** ViT и авторегрессионная Vision-Language Model. **Результат:** текстовое параметрическое описание 3D-модели. **Ограничение:** эксперименты проведены на параметрических моделях шкафов, а не на произвольных машиностроительных деталях.

**[S4]** Zhang C., Polette A., Pinquié R., Iida M., De Charnace H., Pernot J.-P. **Reinforcement learning-based parametric CAD models reconstruction from 2D orthographic drawings.** *Computer-Aided Design*, 188, 103925, 2025. DOI: [10.1016/j.cad.2025.103925](https://doi.org/10.1016/j.cad.2025.103925). [Аннотация и описание](https://www.sciencedirect.com/science/article/pii/S0010448525000867).

> **Вход:** ортогональные чертежи после выделения рёбер и вершин. **Метод:** DQN выбирает пары loop-path, задающие конструктивные действия. **Результат:** редактируемая параметрическая CAD-модель. **Ограничение:** экспериментально проверены прежде всего sketch-extrude операции; чертежи не содержат размерных аннотаций и допусков.

**[S5]** Jong W.-R., Lin Y.-H., Lin Y.-C. **Deep Learning-Based Automation for Converting 2D Engineering Drawings into 3D Solid Models.** *Machines*, 14(7), 781, 2026. DOI: [10.3390/machines14070781](https://doi.org/10.3390/machines14070781).

> **Вход:** чертежи с геометрическими элементами и размерами. **Метод:** несколько YOLOv4 для распознавания видов, контуров и размерных данных; сопоставление результатов. **Результат:** построение 3D-модели средствами Siemens NX/NX Open. **Ограничение:** узкий класс исходных геометрических элементов (включая ограничение двумя элементами); точность детекторов не равна точности итоговой CAD-модели.

**[S6]** Ravichandran H., Inkermann D. **Automatic Reverse Engineering of Parametric CAD Models from Multi-View 2D Projections Using Deep Learning.** *Procedia CIRP*, 142, 55–60, 2026. DOI: [10.1016/j.procir.2026.05.223](https://doi.org/10.1016/j.procir.2026.05.223). [Репозиторий реализации](https://github.com/hariravi15/Automatic_Reverse_Engineering).

> **Вход:** шесть ортогональных 2D-проекций. **Метод:** MVCNN и Transformer предсказывают процедурную CAD-последовательность; отдельный модуль оценивает размеры. **Результат:** параметрическая модель, собираемая в Siemens NX. **Ограничение:** результаты зависят от дополнительного измерительного этапа и фиксированного набора видов.
