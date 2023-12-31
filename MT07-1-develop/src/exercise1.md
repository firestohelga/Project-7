## Алгоритмы балансировки нагрузки (особенности и недостатки).

1. `RR (round robin циклическая очередь)` - алгоритм распределения  нагрузки  методом перебора и упорядочения её элементов (серверов)по круговому циклу. Запросы направляются поочередно, первый запрос передаётся одному серверу, затем следующий запрос передаётся другому и так до достижения последнего сервера, а затем всё начинается сначала.   

Плюсы подхода: простота, дешевизна, эффективность. Это одна из самых простых разновидностей балансировки нагрузок, которая хорошо работает, когда серверы имеют одинаковую мощность, а запросы одинаково затратны. Не требует связи между серверами, поэтому он может использоваться как для локальной, так и для глобальной балансировки. 

Минус подхода:  Чтобы распределение нагрузки по этому алгоритму отвечало упомянутым выше критериями справедливости и эффективности, нужно, чтобы у каждого сервера был в наличии одинаковый набор ресурсов. При выполнении всех операций также должно быть задействовано одинаковое количество ресурсов. В реальной практике эти условия в большинстве случаев оказываются невыполнимыми. Также при балансировке по алгоритму Round Robin совершенно не учитывается загруженность того или иного сервера в составе кластера. Слабое место round robin: колебания мощности серверов.  

2. `WRR (weighted round robin. взвешенная циклическая очередь)` - это алгоритм распределения  нагрузки  методом перебора и упорядочения её элементов (серверов)по круговому циклу с учетом производительности и мощности сервера, т.е. каждому серверу присваивается весовой коэффициент. Это способствует более равномерному распределению нагрузки: серверы с большим весом обрабатывают больше запросов. Для эффективной работы WRR необходимо правильно подобрать вес.

Плюсы подхода: этот алгоритм позволяет лучше справляться с колебаниями мощности и производительности серверов, чем стандартный round robin

Минус подхода: сложно свести производительность сервера к одному числу, поэтому данный алгоритм вопрос с отказоустойчивостью не решает, нам всё равно нужно решить вопрос колебаний запросов. Слабое место  weighted round robin: колебания запросов . Более эффективную балансировку обеспечивают другие методы, в которых при планировании и распределении нагрузки учитывается большее количество параметров.

3. `DWRR (dynamic weighted round robin. динамическая взвешенная циклическая очередь)` -это алгоритм балансировки нагрузки с динамическим вычислением веса  при помощи вспомогательной метрики: задержки. Адаптивная балансировка подбирается динамически на основании относительного различия в задержках.

Плюсы подхода: отсутствует необходимость заранее указывать коэфициент каждого сервера, алгоритм  учитывает колебания и мощности сервера, и затраты на запросы. 

Минус подхода: Сложность алгоритма. В алгоритме не учитывается количество активных на данный момент подключений.

4. `LC (least connections наименьшее количество соединений)` - алгоритм, при котором каждый новый запрос передается на тот сервер, на котором в данный момент меньше всего активных подключений. Этот метод позволяет распределять нагрузку на серверы достаточно равномерно. 

Плюсы подхода:  алгоритм гарантирует, что все серверы используются одинаково и ни один из них не перегружен.

Минус подхода: не учитывается весовой коэффициент серверов. LC справляется с перегрузками гораздо лучше RR, WRR, но ценой чуть больших задержек.

5. `PEWMA (peak exponentially weighted moving average пиковая экспоненциально взвешенная скользящая средняя)`- алгоритм, используемый в системах балансировки нагрузки, который основывается на методе экспоненциально взвешенного скользящего среднего (EWMA). Алгоритм peak EWMA следит за средней нагрузкой на каждом сервере в кластере и сравнивает ее с заданной пороговой нагрузкой. Если средняя нагрузка превышает порог, алгоритм начинает уменьшать количество запросов, отправляемых на данный сервер, чтобы снизить его нагрузку. Это достигается путем вычисления взвешенного среднего значения нагрузки на сервере за определенный период времени. Чем больше весовой коэффициент, тем больше учитывается последняя нагрузка на сервере. После вычисления среднего значения алгоритм сравнивает его с порогом и принимает решение о том, какое количество запросов должно быть отправлено на сервер.

 Плюсы подхода: Алгоритм имеет показатели задержки weighted round robin и надёжность least connections, позволяет балансировать нагрузку на разных серверах в кластере и эффективно распределять запросы для оптимальной производительности системы. PEWMA имеет множество параметров, которые можно настраивать.
 
 Минус подхода: PEWMA оппортунистичен, он пытается добиться наилучшей задержки, а это значит, что он иногда может обеспечивать неполную загрузку сервера, это связано с тем, что  чем старее задержка, тем меньше она влияет на сумму. Недавние запросы влияют на расчёт сильнее, чем старые. Сложность настройки.


6. `Sticky Sessions липкие сессии` - это алгоритм распределения нагрузки, при котором соединения распределяются в зависимости от IP-адреса пользователя. Sticky Sessions предполагает, что обращения от одного клиента будут направляться на один и тот же сервер, а не скакать в пуле
Клиент сменит сервер только в том случае, если ранее использовавшийся больше недоступен. 

Плюсы подхода: Использование "липких сеансов" может помочь улучшить пользовательский опыт и оптимизировать использование сетевых ресурсов. Липкие" сеансы позволяют повышать скорость реагирования.

Минус подхода: Применение этого метода сопряжено с некоторыми проблемами. Проблемы с привязкой сессий могут возникнуть, если клиент использует динамический IP. Отсутствие отказоустойчивости. Если сервер, к которому в данный момент обращаются, выходит из строя, запрос перенаправляется на другие серверы, и пользователю необходимо снова войти в систему. 
