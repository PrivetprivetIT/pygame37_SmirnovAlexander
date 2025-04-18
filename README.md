### Описание игры "Pac-Man наоборот"
Цель игры: 
--
Управляйте Пакманом с помощью мыши, собирайте призраков разных цветов, чтобы зарабатывать очки. Избегайте вишен (cherry), которые отнимают жизни. Игра продолжается, пока у вас не закончатся жизни (3 шанса) или пока вы не соберете 30 очков.

---
## Основные элементы и логика игры:
### 1. Управление Пакманом:
- Пакман автоматически движется к курсору мыши.
- Направление его движения (и анимация) меняется в зависимости от положения мыши (вверх, вниз, влево, вправо, по диагонали).

### 2. Призраки:
- На экране появляются призраки 4 цветов (красный, розовый, синий, оранжевый) и вишня (cherry).
- При столкновении:
  + С призраком: +1 очко.
  + С вишней: -1 жизнь.
- Призраки исчезают через 1.5 секунды и появляются в новом месте на расстоянии не менее 100 пикселей от Пакмана.

### 3. Система очков и жизней:
- Начальное количество жизней: 3.
- Для победы нужно набрать 30 очков.
- Если жизни закончатся, игра завершится поражением.

### 4. Завершение игры:
- При победе (30 очков) на экране появится сообщение: "**Вы выиграли!**".
- При поражении (0 жизней) — "**Вы проиграли!**".
- В конце игры Пакман останавливается, а призраки перестают появляться.

### 5. Основной игровой цикл:
- Обрабатывает события (например, закрытие окна).
- Обновляет позиции Пакмана и призраков.
- Проверяет столкновения и условия победы/поражения.
- Отображает графику (Пакмана, призраков, текст с очками и жизнями).

---
## Ключевые функции:
1. *get_direction(pos1, pos2):*
   - Определяет направление движения Пакмана (8 направлений) на основе разницы координат между Пакманом и курсором.

2. *move_towards(pos1, pos2, speed):*
   - Плавно перемещает Пакмана к курсору с заданной скоростью.

3. *check_collision(pos1, pos2, radius=50):*
   - Проверяет столкновение Пакмана с призраком/вишней на основе расстояния между объектами.

4. *spawn(pacman_pos, size, min_distance=100):*
   - Генерирует новую позицию для призрака, гарантируя, что он появится не ближе 100 пикселей к Пакману.


 
