# Administration of local networks
Year 3 - Module 3

## Laboratory Work №1 - Getting to know Cisco Packet Tracer

Purpose of the work: installing the Cisco Packet Tracer Network Configuration Modeling Tool and getting to know its interface.

## Laboratory Work №2 - Preliminary configuration of Cisco equipment

Purpose of the work: Get basic skills in the initial configuration of equipment Cisco.

## Laboratory Work №3 - Planning the organization's local network

Purpose of the work: Get acquainted with the principles of planning the organization's local network.

## Laboratory Work №4 - Initial network configuration

Purpose of the work: To carry out preparatory work on the initial setup of the network switches.

## Laboratory Work №5 - VLAN Configuration

Purpose of the work: Get basic VLAN configuration skills on network switches.

## Laboratory Work №6 - Static VLAN routing

Purpose of the work: Configure static VLAN routing on the network.

## Laboratory Work №7 - Accounting for the physical parameters of the network

Purpose of the work: Get the skills to work with the physical workspace of Packet Tracer, as well as take into account the physical parameters of the network.

## Laboratory Work №8 - Configuring network services DHCP

Purpose of the work: Acquisition of practical skills in setting up dynamic IP address allocation via the DHCP protocol (Dynamic Host Configuration protocol) in a local network.

## Laboratory Work №9 - Using the STP protocol. Channel aggregation

Purpose of the work: Study of the capabilities of the STP protocol and its modifications to ensure network fault tolerance, interface aggregation and load redistribution between them.

## Laboratory Work №10 - Configuring Access Control Lists (ACL)

Purpose of the work: Master setting up user access rights to network resources.

# Основные идеи

-   Стандартные соглашения об именах
-   Стандартное соглашение для путей к файлам
-   Стандартная настройка курса внутри шаблона курса

# Общие правила

-   Рабочее пространство по предмету располагается в следующей иерархии:

    ``` bash
    ~/work/study/
    └── <учебный год>/
        └── <название предмета>/
            └── <код предмета>/
    ```

-   Например, для 2022--2023 учебного года и предмета «Операционные
    системы» (код предмета `os-intro`) структура каталогов
    примет следующий вид:

    ``` bash
    ~/work/study/
    └── 2022-2023/
        └── Операционные системы/
            └── os-intro/
    ```

-   Название проекта на хостинге git имеет вид:

    ``` example
    study_<учебный год>_<код предмета>
    ```

-   Например, для 2022--2023 учебного года и предмета «Операционные
    системы» (код предмета `os-intro`) название проекта
    примет следующий вид:

    ``` example
    study_2022-2023_os-intro
    ```

-   Каталог для лабораторных работ имеет вид `labs`.

-   Каталоги для лабораторных работ имеют вид `lab<номер>`,
    например: `lab01`, `lab02` и т.д.

-   Каталог для групповых проектов имеет вид `group-project`.

-   Каталог для персональных проектов имеет вид
    `personal-project`.

-   Если проектов несколько, то они нумеруются подобно лабораторным
    работам.

-   Этапы проекта обозначаются как `stage<номер>`.

# Шаблон для рабочего пространства

-   Репозиторий:
    <https://github.com/yamadharma/course-directory-student-template>.

## Сознание репозитория курса на основе шаблона

-   Репозиторий на основе шаблона можно создать либо вручную, через
    web-интерфейс, либо с помощью утилит `gh` (см. [github:
    утилиты командной строки](id:d1925a41-6b4c-4a3a-b102-6337891b8841)).

-   Создание с помощью утилит.

-   Создание выглядит следующим образом:

    ``` shell
    gh repo create <new-repo-name> --template="<owner/template-repo>"
    ```

-   Например, для 2022--2023 учебного года и предмета «Операционные
    системы» (код предмета `os-intro`) создание репозитория
    примет следующий вид:

    ``` shell
    mkdir -p ~/work/study/2022-2023/"Операционные системы"
    cd ~/work/study/2022-2023/"Операционные системы"
    gh repo create study_2022-2023_os-intro --template=yamadharma/course-directory-student-template --public
    git clone --recursive git@github.com:<owner>/study_2022-2023_os-intro.git os-intro
    ```

-   Сделать свой репозиторий на основе шаблона можно и вручную.

## Настройка каталога курса

-   Перейдите в каталог курса:

    ``` shell
    cd ~/work/study/2022-2023/"Операционные системы"/os-intro
    ```

-   Удалите лишние файлы:

    ``` shell
    rm package.json
    ```

-   Создайте необходимые каталоги:

    ``` shell
    echo os-intro > COURSE
    make
    ```

-   Отправьте файлы на сервер:

    ``` shell
    git add .
    git commit -am 'feat(main): make course structure'
    git push
    ```
