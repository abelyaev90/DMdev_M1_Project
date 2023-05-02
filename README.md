# DMdev_M1_Project
--«Библиотекари — Читальные залы»
CREATE TABLE IF NOT EXISTS librarian_room
(
id_room      INT NOT NULL,
id_librarian INT NOT NULL,
PRIMARY KEY (id_room, id_librarian), -- не до конца понимаю для чего может быть нужна эта таблица и как тут поможет составной первичный ключ
CONSTRAINT id_lr_room --не понимаю для чего мы объявляем  CONSTRAINT id_lr_room и что он нам дает?
FOREIGN KEY (id_room)
REFERENCES room (id)
ON DELETE CASCADE
ON UPDATE CASCADE,
CONSTRAINT id_lr_librarian
FOREIGN KEY (id_librarian)
REFERENCES librarian (id)
ON DELETE NO ACTION
ON UPDATE CASCADE
);