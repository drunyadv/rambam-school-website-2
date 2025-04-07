
ссылка на виедо:
https://youtu.be/sS5pq0JiRME?si=wHuY7kaXWAZuk_qs

код презентации:

Sub CreatePresentation()
    ' Объявляем переменные
    Dim pptApp As PowerPoint.Application
    Dim pptPres As PowerPoint.Presentation
    Dim sld As PowerPoint.Slide
    Dim shp As PowerPoint.Shape
    
    ' Создаем новый экземпляр PowerPoint
    Set pptApp = New PowerPoint.Application
    pptApp.Visible = True
    Set pptPres = pptApp.Presentations.Add
    
    ' Слайд 1: Титульный
    Set sld = pptPres.Slides.Add(1, ppLayoutText)
    With sld.Shapes.Title
        .TextFrame.TextRange.Text = "Презентация сайта Теоретического лицея имени Рамбама"
        .TextFrame.TextRange.Font.Size = 44
        .TextFrame.TextRange.Font.Bold = True
        .TextFrame.TextRange.Font.Color.RGB = RGB(0, 94, 184) ' Синий цвет
    End With
    With sld.Shapes.Item(2).TextFrame.TextRange
        .Text = "Автор: [Ваше имя]" & vbNewLine & "Дата: 07.04.2025"
        .Font.Size = 28
        .Font.Color.RGB = RGB(0, 0, 0)
    End With
    
    ' Слайд 2: Обзор сайта
    Set sld = pptPres.Slides.Add(2, ppLayoutText)
    With sld.Shapes.Title
        .TextFrame.TextRange.Text = "Обзор сайта"
        .TextFrame.TextRange.Font.Size = 36
        .TextFrame.TextRange.Font.Bold = True
        .TextFrame.TextRange.Font.Color.RGB = RGB(0, 94, 184)
    End With
    With sld.Shapes.Item(2).TextFrame.TextRange
        .Text = "• Сайт для Теоретического лицея имени Рамбама" & vbNewLine & _
                "• Цель: представить лицей, его деятельность и новости" & vbNewLine & _
                "• Разделы: Главная, О нас, Новости, Деятельность, Расписание, Вакансии, Контакты" & vbNewLine & _
                "• Современный дизайн с интерактивными функциями"
        .Font.Size = 24
        .Font.Color.RGB = RGB(0, 0, 0)
    End With
    
    ' Слайд 3: Дизайн и интерфейс
    Set sld = pptPres.Slides.Add(3, ppLayoutText)
    With sld.Shapes.Title
        .TextFrame.TextRange.Text = "Дизайн и интерфейс"
        .TextFrame.TextRange.Font.Size = 36
        .TextFrame.TextRange.Font.Bold = True
        .TextFrame.TextRange.Font.Color.RGB = RGB(0, 94, 184)
    End With
    With sld.Shapes.Item(2).TextFrame.TextRange
        .Text = "• Адаптивный дизайн: работает на ПК и мобильных устройствах" & vbNewLine & _
                "• Переключатель тем: светлая и темная (с плавным переходом)" & vbNewLine & _
                "• Липкая навигационная панель с логотипом (звезда Давида)" & vbNewLine & _
                "• Кнопка 'Наверх' с плавной прокруткой"
        .Font.Size = 24
        .Font.Color.RGB = RGB(0, 0, 0)
    End With
    
    ' Слайд 4: Раздел "Новости"
    Set sld = pptPres.Slides.Add(4, ppLayoutText)
    With sld.Shapes.Title
        .TextFrame.TextRange.Text = "Раздел 'Новости'"
        .TextFrame.TextRange.Font.Size = 36
        .TextFrame.TextRange.Font.Bold = True
        .TextFrame.TextRange.Font.Color.RGB = RGB(0, 94, 184)
    End With
    With sld.Shapes.Item(2).TextFrame.TextRange
        .Text = "• Слайдер с карточками новостей (прокрутка влево/вправо)" & vbNewLine & _
                "• Фильтр по дате (от новых к старым и наоборот)" & vbNewLine & _
                "• Поиск новостей по ключевым словам" & vbNewLine & _
                "• Анимация появления карточек (слева/справа) при прокрутке" & vbNewLine & _
                "• Всплывающее уведомление о новых событиях (с кнопкой закрытия)" & vbNewLine & _
                "• Модальное окно с деталями новости"
        .Font.Size = 24
        .Font.Color.RGB = RGB(0, 0, 0)
    End With
    
    ' Слайд 5: Другие разделы
    Set sld = pptPres.Slides.Add(5, ppLayoutText)
    With sld.Shapes.Title
        .TextFrame.TextRange.Text = "Другие разделы"
        .TextFrame.TextRange.Font.Size = 36
        .TextFrame.TextRange.Font.Bold = True
        .TextFrame.TextRange.Font.Color.RGB = RGB(0, 94, 184)
    End With
    With sld.Shapes.Item(2).TextFrame.TextRange
        .Text = "• Расписание: фильтры по классу и дню, таблица уроков" & vbNewLine & _
                "• Контакты: интерактивная карта Google Maps и форма обратной связи" & vbNewLine & _
                "• Вакансии: список с описанием требований и контактами" & vbNewLine & _
                "• Деятельность: ссылки на отчеты, бюджет и планы"
        .Font.Size = 24
        .Font.Color.RGB = RGB(0, 0, 0)
    End With
    
    ' Слайд 6: Заключение
    Set sld = pptPres.Slides.Add(6, ppLayoutText)
    With sld.Shapes.Title
        .TextFrame.TextRange.Text = "Заключение"
        .TextFrame.TextRange.Font.Size = 36
        .TextFrame.TextRange.Font.Bold = True
        .TextFrame.TextRange.Font.Color.RGB = RGB(0, 94, 184)
    End With
    With sld.Shapes.Item(2).TextFrame.TextRange
        .Text = "• Сайт — современный и удобный прототип для лицея" & vbNewLine & _
                "• Интерактивные функции: фильтры, уведомления, карта" & vbNewLine & _
                "• Адаптивность и анимации для лучшего опыта" & vbNewLine & _
                "• Готов к демонстрации и дальнейшей доработке"
        .Font.Size = 24
        .Font.Color.RGB = RGB(0, 0, 0)
    End With
    
    ' Применяем цвет фона ко всем слайдам
    Dim i As Integer
    For i = 1 To pptPres.Slides.Count
        pptPres.Slides(i).Background.Fill.ForeColor.RGB = RGB(230, 240, 250) ' Светло-голубой фон
    Next i
    
    ' Освобождаем ресурсы
    Set sld = Nothing
    Set pptPres = Nothing
    Set pptApp = Nothing
End Sub
