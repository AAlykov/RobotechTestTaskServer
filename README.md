# RobotechTestTaskServer

## Сборка проекта на Linux

1. Установить зависимости
Убедитесь, что все необходимые инструменты и библиотеки установлены:
```bash
sudo apt update
sudo apt install cmake build-essential qtbase5-dev libqt5widgets5 qtdeclarative5-dev qttools5-dev-tools
```

2. Сборка проекта
2.1. Зайдите в каталог скаченного проекта. Создайте папку для сборки (рекомендуется использовать отдельный каталог для сборки):
```bash
mkdir build
cd build
```
2.2. Сгенерируйте файлы сборки с помощью CMake:
```bash
cmake .. -DCMAKE_BUILD_TYPE=Release
```
Если Qt установлен в пользовательской директории (например, через Qt Installer)
```bash
cmake .. -DCMAKE_PREFIX_PATH=/opt/Qt/5.15.2/gcc_64
```
2.3. Соберите проект:
```bash
make
```
3.Также проект можно собрать с помощью Qt Creator через основной cmake-файл.

## Сборка проекта на Windows

1. Конфигурация и сборка
Откройте Qt Command Prompt (если используете MinGW) или откройте терминал Developer Command Prompt for VS (если используете MSVC).

2. Создайте папку для сборки:
```bash
mkdir build
cd build
```

3. Запустите CMake с указанием пути к Qt:
```bash
cmake .. -G "MinGW Makefiles" -DCMAKE_PREFIX_PATH="C:/Qt/5.x/mingw_x64" -DCMAKE_BUILD_TYPE=Release
```
Если используете Visual Studio:
```bash
cmake .. -G "Visual Studio 16 2019" -A x64 -DCMAKE_PREFIX_PATH="C:/Qt/5.x/msvc2019_64"
```
или без дополнительных параметров:
```bash
cmake ..
```

4. Соберите проект:
Для MinGW:
```bash
mingw32-make
```
Для Visual Studio:
```bash
cmake --build . --config Release
```

5. Также проект можно собрать с помощью Qt Creator через основной cmake-файл.

![server](https://github.com/user-attachments/assets/2e88874a-c600-49f0-a6d7-7b63e7375a1d)

