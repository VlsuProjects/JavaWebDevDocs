# Проблемы транзакций

Как вы уже поняли - транзакции - это мощный инструмент, который позволяет обеспечить целостность данных в базе. Однако,
транзакции могут привести к некоторым проблемам, которые вам нужно уметь решать. Как вы скорее всего уже поняли, в
большинстве приложений использование транзакций не ограничивается одной атомарной операцией, в большинстве случаев
транзакций бывает много и все они выполняются одновременно. И так часто случается, что разные транзакции могут работать 
с одними и теми же данными. Вот именно в этом случае могут возникнуть проблемы.

Существует несколько видов проблем в таких случаях:
- [**Dirty reads**](problems/dirty-reads.md)
- [**Non-repeatable reads**](problems/non-repeatable-reads.md)
- [**Phantom reads**](problems/phantom-reads.md)
- [**Lost updates**](problems/lost-updates.md)

Как видите все эти проблемы очень похожи и имеют один и тот же источник - невнимательное использование транзакций или 
недостаточное понимание работы других транзакций в приложении.