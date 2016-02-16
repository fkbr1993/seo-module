1. Для списка в админке во представлении (во вьюшке) index перед гридом:

`<?= SeoWidget::widget(
    [
        'model' => new \news\models\News(),
        'form' => true,
        'style' => 'btn btn-primary btn-xs',
        'onlyForm' => true
    ]
) ?>`

2. Для отдельной новости, в представлении _form.php перед
кнопкой "сохранить" (или сверху можно)

`<?= \seo\widgets\SeoWidget::widget(['model' => $model, 'tab' => true]) ?>`

3. На фронте выводятся в представлении, в самом верху там же
где регаются ассеты (как для списка так и для отдельных объектов)

`Seo::RegisterMetaTags($this, $product);`