## Описание ответа api для вкладки "Деятельность"
##### Ответ в формате JSON

-  Главный обьект имеет поля:
    
    + length:number - количество обьектов (специализаций) хронящихся в главном обьекте
    + Все остальные поля:object - это обьекты (специализации) которые будут переданы
    + Пример (приведен в формате js object):
``` 
{
 0: {},
 1: {},
 length: 2
} 
```
- Обьект специализаций имеет поля:
    + title:string - Название специализации
    + dop_fields:object - Дополнительные параметры специализации
    + pod_spec:object - Подспециализации
    + Пример (приведен в формате js object):
```
{
 0: {
    title: 'Фотограф',
    dop_fields: {},
    pod_spec: {},
 1: {
     title: 'Видеограф',
     dop_fields: {},
     pod_spec: {},
 },
 length: 2
} 
```

- dop_fields:object имеет поля:
    + length:number - количество обьектов (дополнительных параметров) хронящихся в обьекте специализация
    +  Все остальные поля:object - это обьекты (дополнительные параметры) которые будут переданы
    + Пример (приведен в формате js object):
```
{
   0: {
      title: 'Фотограф',
      dop_fields: {
        0: {},
        1: {},
        length: 2
      },
      pod_spec: {},
   1: {
       title: 'Видеограф',
       dop_fields: {
        0: {},
        1: {},
        length: 2
       },
       pod_spec: {},
   },
   length: 2
  } 
```

- Обьект дополнительный параметр имеет поля:
    + type:string - тип поля ('price', 'checkbox')
    + title:string - название поля
    + placeholder:string - подсказка для поля ввода (если type == price)
    + Пример (приведен в формате js object):
    
```
{
   0: {
      title: 'Фотограф',
      dop_fields: {
        0: {
         type: 'price',
         title: 'Стоимость дня работы',
         placeholder: 'Введите значение'
        },
        1: {
         type: 'checkbox',
         title: 'Выезд'
        },
        length: 2
      },
      pod_spec: {},
   1: {
       title: 'Видеограф',
       dop_fields: {
        0: {
            type: 'price',
            title: 'Стоимость дня работы',
            placeholder: 'Введите значение'
            },
        1: {
           type: 'checkbox',
           title: 'Выезд'
           },
        length: 2
       },
       pod_spec: {},
   },
   length: 2
  } 
```

- pod_spec:object имеет поля:
    
    + length:number - количество обьектов (подспециализаций) хронящихся в обьекте специализация
    + Все остальные поля:object - это обьекты (подспециализации) которые будут переданы
    + Пример (приведен в формате js object):
    
```
{
   0: {
      title: 'Фотограф',
      dop_fields: {
        0: {
         type: 'price',
         title: 'Стоимость дня работы',
         placeholder: 'Введите значение'
        },
        1: {
         type: 'checkbox',
         title: 'Выезд'
        },
        length: 2
      },
      pod_spec: {
      0: {},
      1: {},
      length: 2
      },
   1: {
       title: 'Видеограф',
       dop_fields: {
        0: {
            type: 'price',
            title: 'Стоимость дня работы',
            placeholder: 'Введите значение'
            },
        1: {
           type: 'checkbox',
           title: 'Выезд'
           },
        length: 2
       },
       pod_spec: {
        0: {},
        1: {},
        length: 2
      },
   },
   length: 2
  } 
```

- Обьект подспециализация имеет поля:

    + title:string - название подспециализации
    + dop_fields:object - работает так же как со специализациями
    + Пример (приведен в формате js object):
        
    ```
    {
       0: {
          title: 'Фотограф',
          dop_fields: {
            0: {
             type: 'price',
             title: 'Стоимость дня работы',
             placeholder: 'Введите значение'
            },
            1: {
             type: 'checkbox',
             title: 'Выезд'
            },
            length: 2
          },
          pod_spec: {
          0: {
          title: 'Свадебный',
          dop_fields: {}
          },
          1: {
          title: 'Свадебный',
          dop_fields: {}
           },
          length: 2
          },
       1: {
           title: 'Видеограф',
           dop_fields: {
            0: {
                type: 'price',
                title: 'Стоимость дня работы',
                placeholder: 'Введите значение'
                },
            1: {
               type: 'checkbox',
               title: 'Выезд'
               },
            length: 2
           },
           pod_spec: {
            0: {
            title: 'Свадебный',
            dop_fields: {}
            },
            1: {
            title: 'Свадебный',
            dop_fields: {}
            },
            length: 2
          },
       },
       length: 2
      } 
    ```
   