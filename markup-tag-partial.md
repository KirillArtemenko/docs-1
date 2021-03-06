# {% partial %}

Тег `{% partial %}` анализирует содержимое [фрагмента](./cms/partials) и отображает его на странице. Для этого Вы должны указать название файла в качестве параметра:

    {% partial "footer" %}

Вы также можете указать название папки, в котором лежит файл:

    {% partial "sidebar/menu" %}

> **Примечание**: В разделе [Темы ( Themes )](./cms/themes#subdirectories) Вы сможете найти больше информации о работе с подпапками.

Вы можете использовать переменную, чтобы указать название файла:

    {% set tabName = "profile" %}
    {% partial tabName %}

<a name="variables"></a>
## Переменные

Вы можете передавать параметры в фрагменты, указав их после названия файла:

    {% partial "blog-posts" posts=posts %}

Вы также можете указать произвольные переменные:

    {% partial "location" city="Vancouver" country="Canada" %}

Пример:

    <p>Country: {{ country }}, city: {{ city }}.</p>
