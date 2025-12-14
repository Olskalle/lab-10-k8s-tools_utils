Устанавливаем Helm:

![Pasted image 20251214013323.png](attachments/Pasted%20image%2020251214013323.png)

Устанавливаем Kompose:

![Pasted image 20251214013652.png](attachments/Pasted%20image%2020251214013652.png)

![Pasted image 20251214013752.png](attachments/Pasted%20image%2020251214013752.png)

![Pasted image 20251214014239.png](attachments/Pasted%20image%2020251214014239.png)

После конвертации дорабатываем файлы и переименовываем чарт. Упаковываем:

![Pasted image 20251214014551.png](attachments/Pasted%20image%2020251214014551.png)

![Pasted image 20251214014604.png](attachments/Pasted%20image%2020251214014604.png)

Устанавливаем релиз:

![Pasted image 20251214015019.png](attachments/Pasted%20image%2020251214015019.png)

![Pasted image 20251214015853.png](attachments/Pasted%20image%2020251214015853.png)

Добавляем образы (+ настраиваем зеркала):

![Pasted image 20251214015931.png](attachments/Pasted%20image%2020251214015931.png)

Проверяем:

![Pasted image 20251214020020.png](attachments/Pasted%20image%2020251214020020.png)

![Pasted image 20251214020040.png](attachments/Pasted%20image%2020251214020040.png)

Добавляем values:

![Pasted image 20251214020316.png](attachments/Pasted%20image%2020251214020316.png)

![Pasted image 20251214020432.png](attachments/Pasted%20image%2020251214020432.png)

![Pasted image 20251214020744.png](attachments/Pasted%20image%2020251214020744.png)

![Pasted image 20251214020803.png](attachments/Pasted%20image%2020251214020803.png)

Проведем апдейт релиза:

![Pasted image 20251214021018.png](attachments/Pasted%20image%2020251214021018.png)

Пробросим порты:

![Pasted image 20251214021116.png](attachments/Pasted%20image%2020251214021116.png)

Проверим:

![Pasted image 20251214023952.png](attachments/Pasted%20image%2020251214023952.png)

Установка Kustomize:

![Pasted image 20251214024459.png](attachments/Pasted%20image%2020251214024459.png)

![Pasted image 20251214024940.png](attachments/Pasted%20image%2020251214024940.png)

![Pasted image 20251214025649.png](attachments/Pasted%20image%2020251214025649.png)

![Pasted image 20251214031529.png](attachments/Pasted%20image%2020251214031529.png)

![Pasted image 20251214031547.png](attachments/Pasted%20image%2020251214031547.png)

Создаем патч и проверяем:

``` yaml
- op: replace
  path: /spec/ports/0/port
  value: 54321
```

![Pasted image 20251214032018.png](attachments/Pasted%20image%2020251214032018.png)

Применяем манифесты и проверяем:

![Pasted image 20251214032509.png](attachments/Pasted%20image%2020251214032509.png)

![Pasted image 20251214032625.png](attachments/Pasted%20image%2020251214032625.png)

Меняем кол-во реплик в devи проверяем:

![Pasted image 20251214035116.png](attachments/Pasted%20image%2020251214035116.png)

Далее выносим имя Redis в переменную окружения:

![Pasted image 20251214040536.png](attachments/Pasted%20image%2020251214040536.png)

Проверяем:

![Pasted image 20251214133054.png](attachments/Pasted%20image%2020251214133054.png)

