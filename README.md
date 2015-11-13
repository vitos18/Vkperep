# Vkperep
android pkk

Просмотр файлов
Первоначальный импорт
 мастер
0 родители фиксации 5eff7cb0f447c52f7c49c6285583b9fc9a41c304 @ thest1 thest1 совершено on 13 Apr 2012
Единая Сплит
Показ  61 измененные файлы  с 3623 дополнений и 0 удалений.
8      AndroidVkSdk / .classpath
@@-0,0 +1,8@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <Классам>
+ <Classpathentry  вид = "SRC" Путь = "SRC" /> 
+ <Classpathentry  вид = "SRC" Путь = "поколения" /> 
+ <Classpathentry  вид = "кон" Путь = "com.android.ide.eclipse.adt.ANDROID_FRAMEWORK" /> 
+ <Classpathentry  вид = "мошенники" путь = "com.android.ide.eclipse.adt.LIBRARIES" /> 
+ <Classpathentry  вид = "Выход" Путь = "Bin / классы" /> 
+ </ Классам>
33      AndroidVkSdk / .project
@@-0,0 +1,33@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <ProjectDescription>
+ <Имя> AndroidVkSdk </ имя>
+ <Комментарий> </ комментарий>
+ <Проекты>
+ </ Проекты>
+ <BuildSpec>
+ <BuildCommand>
+ <Имя> com.android.ide.eclipse.adt.ResourceManagerBuilder </ имя>
+ <Аргументы>
+ </ Аргументы>
+ </ BuildCommand>
+ <BuildCommand>
+ <Имя> com.android.ide.eclipse.adt.PreCompilerBuilder </ имя>
+ <Аргументы>
+ </ Аргументы>
+ </ BuildCommand>
+ <BuildCommand>
+ <Имя> org.eclipse.jdt.core.javabuilder </ имя>
+ <Аргументы>
+ </ Аргументы>
+ </ BuildCommand>
+ <BuildCommand>
+ <Имя> com.android.ide.eclipse.adt.ApkBuilder </ имя>
+ <Аргументы>
+ </ Аргументы>
+ </ BuildCommand>
+ </ BuildSpec>
+ <Натуры>
+ <Природа> com.android.ide.eclipse.adt.AndroidNature </ природа>
+ <Природа> org.eclipse.jdt.core.javanature </ природа>
+ </ Природа>
+ </ ProjectDescription>
8      AndroidVkSdk / AndroidManifest.xml
@@-0,0 +1,8@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <Проявляются  XMLNS: Android = "http://schemas.android.com/apk/res/android"
+     Пакет = "com.perm.kate"
+     Андроид: versionCode = "1"
+     Андроид: versionName = "1.0" 
+>
+ <Использования  SDK-андроид: minSdkVersion = "4" />
+ </ Проявляются> 
83      AndroidVkSdk / build.xml
@@-0,0 +1,83@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <Проект  название = "AndroidVkSdk" по умолчанию = "помощь"> 
+
+     <! - Файл local.properties создается и обновляется '' андроид инструмента.
+          Он содержит путь к SDK. Следует * не * быть проверены в
+          Версия системы управления. ->
+ <Свойство  файла = "local.properties" />
+
+     <! - Файл ant.properties могут быть созданы вами. Это только отредактирован
+          '' Андроид инструмент для добавления свойства к нему.
+          Это место, чтобы изменить некоторые специфические свойства Ant сборки.
+          Вот некоторые свойства, вы можете захотеть изменить / обновления:
+
+          Source.dir
+              Название директории с исходниками. По умолчанию "SRC".
+          Out.dir
+              Название выходном каталоге. По умолчанию это «бен».
+
+          Для других перегружаемых свойств, посмотрите в начале правил
+          Файлы в SDK, на инструменты / муравей / build.xml
+
+          Свойства, на место SDK или цели проекта должны
+          Обновлены с помощью '' андроид инструмент с 'Update' действия.
+
+          Этот файл является неотъемлемой частью системы сборки для вашего
+          Приложение и должны быть проверены в системах контроля версий.
+
+          ->
+ <Свойство  файла = "ant.properties" />
+
+     <! - Файл project.properties создается и обновляется "андроид"
+          Инструмент, а также ADT.
+
+          Он содержит проект специфические свойства, такие как цели проекта, и библиотеки
+          Зависимостей. Свойства сборки нижнего уровня хранятся в ant.properties
+          (Или в .classpath проектов Eclipse).
+
+          Этот файл является неотъемлемой частью системы сборки для вашего
+          Приложение и должны быть проверены в системах контроля версий. ->
+ <Loadproperties  srcFile = "project.properties" />
+
+     <! - Быстрая проверка sdk.dir ->
+ <Неудачу
+             Сообщение = "sdk.dir отсутствует. Убедитесь в том, чтобы генерировать local.properties используя" андроид проект обновления "или вводить его через окр вар"
Не            +, если = "sdk.dir"
+ />
+
+     <! -
+         Импорт за проект обычай строить правила, если присутствующие на корню проекта.
+         Это место, чтобы поместить пользовательские посреднические цели, такие как:
+             -pre-Сборки
+             -pre-Компиляции
+             -post Компиляции (Это, как правило, используется для запутывания кода.
+                            Составитель расположение код: $ {} out.classes.absolute.dir
+                            Если это не будет сделано на месте, переопределить $ {} out.dex.input.absolute.dir)
+             -post-Пакет
+             -post-Сборки
+             -pre-Чистый
+     ->
+ <Импорта  файла = "custom_rules.xml" дополнительный = "истинный" /> 
+
+     <! - Импорт сам файл сборки.
+
+          Чтобы настроить существующие цели, есть два варианта:
+          - Настройка только одну цель:
+              - Копировать / вставить цель в этом файле, * перед *
+                <Импорт> задача.
+              - Настроить его для ваших нужд.
+          - Настройка все содержимое build.xml
+              - Копировать / вставить содержимое файлов правил (минус верхний узел)
+                В этом файле, заменяя <импорт> задачи.
+              - Настроить для ваших нужд.
+
+          ***********************
+          ****** ****** ВАЖНО
+          ***********************
+          Во всех случаях необходимо обновить значение версии тега ниже, чтобы прочитать "обычай", а не целое число,
+          Для того, чтобы избежать необходимости ваш файл быть отменено инструментов, таких, как "андроид проекта обновления"
+     ->
+     <! - Версия тег: 1 ->
+ <Импорта  файла = "$ {sdk.dir} /tools/ant/build.xml" />
+
+ </ Проект>
10      AndroidVkSdk / local.properties
@@-0,0 +1,10@@
+ # Этот файл автоматически генерируется Android Tools.
+ # Не изменяйте этот файл - ваши изменения будут стерты!
+ #
+ # Этот файл должен * не * быть проверены в системах контроля версий,
+ #, Поскольку он содержит информацию, относящуюся к вашей локальной конфигурации.
+
+ # Местонахождение SDK. Это используется только Ant
+ # Для настройки при использовании системы контроля версий, пожалуйста, прочтите
+ # Заголовок записка.
+ Sdk.dir = C: \\ Android-SDK-окна
20      AndroidVkSdk / ProGuard-project.txt
@@-0,0 +1,20@@
+ # Чтобы включить ProGuard в вашем проекте, редактировать project.properties
 + #, Чтобы определить свойство proguard.config, как описано в этом файле.
 + #
 + # Добавить проект конкретные правила Proguard здесь.
 + # По умолчанию, флаги этого файла добавляются к флагам, указанным
 + # В $ {} /tools/proguard/proguard-android.txt sdk.dir
 + # Вы можете отредактировать включают путь и порядок путем изменения ProGuard
 + # Включить имущество в project.properties.
 + #
 + # Для более подробной информации см
 + # Http://developer.android.com/guide/developing/tools/proguard.html
 +
 + # Добавьте любые варианты конкретного проекта держать здесь:
 +
 + # Если ваш проект использует WebView с JS, раскомментировать следующие
 + # И указать полное имя класса интерфейса JavaScript
 + # Класс:
 + # - класс keepclassmembers fqcn.of.javascript.interface.for.webview {
 + # * Общественность;
 + #}
40      AndroidVkSdk / proguard.cfg
@@-0,0 +1,40@@
+ -optimizationpasses 5
+ -dontusemixedcaseclassnames
+ -dontskipnonpubliclibraryclasses
+ -dontpreverify
+ -verbose
+ -optimizations! Код / упрощение / арифметика, поля! / * ,! класс / слияния / *
+
+ -keep общественного класса * расширяет android.app.Activity
+ -keep общественного класса * расширяет android.app.Application
+ -keep общественного класса * расширяет android.app.Service
+ -keep общественного класса * расширяет android.content.BroadcastReceiver
+ -keep общественного класса * расширяет android.content.ContentProvider
+ -keep общественного класса * расширяет android.app.backup.BackupAgentHelper
+ -keep общественного класса * расширяет android.preference.Preference
+ -keep общественного класса com.android.vending.licensing.ILicensingService
+
+ -keepclasseswithmembernames класс * {
+ Родные <методы>;
+}
+
+ -keepclasseswithmembers класс * {
+ Общественного <инициализации> (android.content.Context, android.util.AttributeSet);
+}
+
+ -keepclasseswithmembers класс * {
+ Общественного <инициализации> (android.content.Context, android.util.AttributeSet, INT);
+}
+
+ -keepclassmembers класс * расширяет android.app.Activity {
+ Общественного недействительными * (android.view.View);
+}
+
+ -keepclassmembers перечисление * {
+ Общественности статической ** [] значения ();
+ Общественности статической ** valueOf (java.lang.String);
+}
+
+ -keep класс * реализует android.os.Parcelable {
+ Общественности статической окончательный android.os.Parcelable $ Творец *;
+}
12      AndroidVkSdk / project.properties
@@-0,0 +1,12@@
+ # Этот файл автоматически генерируется Android Tools.
+ # Не изменяйте этот файл - ваши изменения будут стерты!
+ #
+ # Этот файл должен быть проверен в системах контроля версий.
+ #
+ # Чтобы настроить свойства, используемые Ant использования системы сборки,
+ # "Ant.properties", и значения вручную, чтобы адаптировать сценарий к вашему
+ # Структура проекта.
+
+ # Цель проекта.
+ Цель = андроид-4
+ Android.library = правда
32      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Album.java
@@-0,0 +1,32@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Альбом {
+     Общественного  долго помощи;
+     Общественного  долго thumb_id;
+     Общественного  долго owner_id;
+     Общественного  Строка Название;
+     Общественного  Строка Описание;
+     Общественного  долго создано;
+     Общественного  долго обновляются;
+     Общественного  долго размер;
+     Общественного  долго конфиденциальности;
+
+     Общественного  статического  Альбом  разбора (JSONObject  о) бросает  JSONException {
+         Альбом =  новый  альбом ();
+ А. Название =  Апи. Экранирования (о. Строка_опций ("название"));
+ А. Помощь =  Длинные. ParseLong (о. GetString ("помощь"));
+ А. Owner_id =  Long. ParseLong (о. GetString ("owner_id"));
+ А. Описание =  Апи. Экранирования (о. Строка_опций ("Описание"));
+ А. Thumb_id =  Long. ParseLong (о. Строка_опций ("thumb_id"));
+ А. Созданный =  Long. ParseLong (о. Строка_опций ("создана"));
+         Строка конфиденциальности = O. Строка_опций ("конфиденциальность");
+         Если (конфиденциальность! = NULL &&! Конфиденциальности. Равно (""))  
+ А. Конфиденциальности =  Длинные. ParseLong (конфиденциальности);
+ А. Размер =  Длинные. ParseLong (о. Строка_опций ("размер"));
+ А. Обновленный =  Long. ParseLong (о. Строка_опций ("обновляются"));
+         Возвращения а;
+}
+}
1709      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Api.java
1,709 дополнения, 0 делеции не показаны
58      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Attachment.java
@@-0,0 +1,58@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.util.ArrayList;
+ Импорт  org.json.JSONArray;
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Приложение {
+     Общественного  Строка типа; // фото, posted_photo, видео, аудио, ссылки, обратите внимание, приложение, опрос
+     Общественного  фотография фото;
+     // Общественного Фото posted_photo;
+     Общественного  Видео видео;
+     Общественного  Аудио аудио;
+     Общественного  Ссылка ссылку;
+     Общественного  Примечание записка;
+     Общественного  Граффити граффити;
+     Общественного  VkApp приложение;
+     Общественного  VkPoll опрос;
+
+     public  static  ArrayList< Attachment >  parseAttachments ( JSONArray  attachments , long  from_id , long  copy_owner_id ) throws  JSONException {
+         ArrayList <Приложение> attachments_arr = новый  ArrayList <Приложение> ();
+         INT размер = вложения. Длина ();
+         Для (INT J = 0, J <размер; ++ J) {
+             Объект Att = вложения. Получить (J);
+             Если (ATT экземпляром  JSONObject == ложь)
+                 Продолжить;
+             JSONObject json_attachment = (JSONObject) Att;
+             Приложение привязанности = новый  Вложений ();
+ Крепление. Тип = json_attachment. GetString ("тип");
+             Если (приложение. Тип. Равно ("фото") || привязанность. Тип. Равно ("posted_photo")) {
+                 JSONObject х = json_attachment. OptJSONObject ("фото");
+                 Если (х! = NULL)
+ Крепление. Фото = фото. Разбора (х);
+}
+             Если (приложение. Тип. Равно ("граффити"))
+ Крепление. Граффити = Граффити. Разбора (json_attachment. GetJSONObject ("граффити"));
+             Если (приложение. Тип. Равно ("ссылка"))
+ Крепление. Ссылку = Ссылка. Разбора (json_attachment. GetJSONObject ("ссылка"));
+             Если (приложение. Тип. Равно ("аудио"))
+ Крепление. Аудио = аудио. Разбора (json_attachment. GetJSONObject ("аудио"));
+             Если (приложение. Тип. Равно ("внимание"))
+ Крепление. Примечание = Примечание. Разбора (json_attachment. GetJSONObject ("внимание"), ложные);
+             Если (приложение. Тип. Равно ("видео"))
+ Крепление. Видео = Видео. Разбора (json_attachment. GetJSONObject ("видео"));
+             Если (приложение. Тип. Равно ("опрос")) {
+ Крепление. Опрос = VkPoll. Разбора (json_attachment. GetJSONObject ("опрос"));
+                 Если (приложение. Опрос. Owner_id == 0) {
+                     Если (copy_owner_id! = 0)
+ Крепление. Опрос. Owner_id = copy_owner_id;
+                     Еще
+ Крепление. Опрос. Owner_id = from_id;
+}
+}
+ Attachments_arr. Добавить (приложение);
+}
+         Возврат attachments_arr;
+}
+}
32      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Audio.java
@@-0,0 +1,32@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Аудио {
+     Общественного  долго помощи;
+     Общественного  долго owner_id;
+     Общественного  Строка художник;
+     Общественного  Строка Название;
+     Общественного  долго продолжительность;
+     Общественного  Строка URL;
+     Общественного  Длинные lyrics_id;
+
+     Общественного  статического  Аудио  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Аудио аудио =  новый  Аудио ();
+ Аудио. Помощь =  Длинные. ParseLong (о. GetString ("помощь"));
+ Аудио. Owner_id =  Длинные. ParseLong (о. GetString ("owner_id"));
+         Если (о. Имеет ("исполнитель"))
+ Аудио. Художник =  Апи. Экранирования (о. GetString ("исполнитель"));
+         Еще  если (о. Имеет ("Художник"))
+ Аудио. Художник =  Апи. Экранирования (о. GetString ("Художник"));
+ Аудио. Название =  Апи. Экранирования (о. GetString ("название"));
+ Аудио. Продолжительность =  Длинные. ParseLong (о. GetString ("Продолжительность"));
+ Аудио. Гиперссылка = O. Строка_опций ("гиперссылка", NULL);
+        
+         Строка TMP = O. Строка_опций ("lyrics_id");
+         Если (TMP! = NULL &&! TMP. Равно ("")) // в противном случае lyrics_id = NULL  
+ Аудио. Lyrics_id =  Длинные. ParseLong (TMP);
+         Возврат аудио;
+}
+} 
52      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Auth.java
@@-0,0 +1,52@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.net.URLEncoder;
+ Импорт  android.util.Log;
+ Импортные  com.perm.utils.Utils;
+
+ Общественного  класса  Авт {
+    
+     Частный  статический  финал  Строка  TAG  =  "Kate.Auth";
+     Общественного  статического  Строка REDIRECT_URL = "http://oauth.vk.com/blank.html";
+    
+     Общественного  статического  Строка  GetURL (Строка  api_id, струнных  настройки) {
+         String url = " http://oauth.vk.com/authorize?client_id= " + api_id + " &display=touch&scope= " + settings + " &redirect_uri= " + URLEncoder . encode(redirect_url) + " &response_type=token " ;
+         Возврат гиперссылка,
+}
+    
+     Общественные  статические  Струнные  getSettings () {
+         //http://vk.com/developers.php?oid=-1&p=%D0%9F%D1%80%D0%B0%D0%B2%D0%B0_%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0_%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B9
+         // + 1 Ïîëüçîâàòåëü ðàçðåøèë îòïðàâëÿòü AIO óâåäîìëåíèÿ.
+         // + 2 Äîñòóï ê äðóçüÿì.
+         // + 4 Äîñòóï ê ôîòîãðàôèÿì.
+         // + 8 Äîñòóï ê àóäèîçàïèñÿì.
+         // + 16 Äîñòóï ê âèäåîçàïèñÿì.
+         // + 32 Äîñòóï ê ïðåäëîæåíèÿì.
+         // + 64 Äîñòóï ê âîïðîñàì.
+         // + 128 Äîñòóï ê вики-ñòðàíèöàì.
+         // + 256 Äîáàâëåíèå ññûëêè íà â ìåíþ ïðèëîæåíèå ñëåâà.
+         // + 512 Äîáàâëåíèå ññûëêè íà ïðèëîæåíèå Aey áûñòðîé ïóáëèêàöèè íà ñòåíàõ ïîëüçîâàòåëåé.
+         // + 1024 Äîñòóï Новичок ñòàòóñàì ïîëüçîâàòåëÿ.
+         // + 2 048 Äîñòóï çàìåòêàì ïîëüçîâàòåëÿ.
+         // + 4096 (AEY Обои для рабочего ïðèëîæåíèé) Äîñòóï Новичок ðàñøèðåííûì ìåòîäàì ðàáîòû ñ ñîîáùåíèÿìè.
+         // + 8192 Äîñòóï Новичок МАС ÷ è ВМИ ðàñøèðåííûì ìåòîäàì ðàáîòû Ni ñòåíîé.
+         // + 65536 форума
+         // + 131072 Äîñòóï Новичок äîêóìåíòàì ïîëüçîâàòåëÿ.
+         // + 262144 Äîñòóï Новичок ãðóïïàì ïîëüçîâàòåëÿ.
+         INT настройки = 1 + 2 + 4 + 8 + 16 + 32 + 64 + 128 + 1 024 + 2 048 + 4096 + 8192 + 65536 + 131072 + 262144;
+         // Ia õâàòàåò ïðàâà уведомления
+         Возвращения  Integer. ToString (настройки);
+         // Возврат "друзья, фото, аудио, видео, документы, заметки, страницы, стены, группы, сообщения, форума";
+}
+    
+     Общественного  статического  Строка [] parseRedirectUrl (Строка  гиперссылка) бросает  исключение {
+         // Гиперссылка что-то вроде http://api.vkontakte.ru/blank.html#access_token=66e8f7a266af0dd477fcd3916366b17436e66af77ac352aeb270be99df7deeb&expires_in=0&user_id=7657164
+         Строка access_token = Utils. ExtractPattern (гиперссылка, "access_token = (*) &.?");
+         Авторизация. Я (TAG, "access_token =" + access_token); 
+         Строка user_id = Utils. ExtractPattern (URL, "user_id = (\\ д *)");
+         Авторизация. Я (TAG, "user_id =" + user_id); 
+         Если (user_id == NULL  || user_id. Длина () == 0  || access_token == NULL  || access_token. Длина () == 0)
+             Бросить  новый  Exception ("Не удалось разобрать URL переадресации" + URL);
+         Возвращения  новый  Струнный [] {access_token, user_id};
+}
+} 
16      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / City.java
@@-0,0 +1,16@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Город {
+     Общественного  долго CID;
+     Общественного  Строка имя,
+
+     Общественного  статического  Город  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Город с =  новый  Город ();
+ С. Чид =  Длинные. ParseLong (о. GetString ("Сид"));
+ С. Имя = O. GetString ("имя");
+         Возврат с;
+}
+}
76      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Comment.java
@@-0,0 +1,76@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Комментарий {
+     Общественного  долго CID;
+     Общественного  долго from_id;
+     Общественного  долго дата;
+     Общественного  Строка сообщений;
+     Общественного  долго reply_to_uid;
+     Общественного  долго reply_to_cid;
+
+     // Понравилось
+     Общественного  INT like_count;
+     Общественного  логическое user_like;
+     Общественного  логическое can_like;
+
+     Общественного  статического  Комментарий  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Комментарий комментарий = новый  комментарий ();
+ Комментарий. Чид =  Длинные. ParseLong (о. GetString ("Сид"));
+ Комментарий. From_id =  Длинные. ParseLong (о. GetString ("UID"));
+ Комментарий. Дата =  Длинные. ParseLong (о. GetString ("Дата"));
+ Комментарий. Сообщение =  Апи. Экранирования (о. GetString ("Текст"));
+         Строка reply_to_uid = O. Строка_опций ("reply_to_uid");
+         Если (reply_to_uid! = NULL &&! Reply_to_uid. Равно (""))   
+ Комментарий. Reply_to_uid =  Длинные. ParseLong (reply_to_uid);
+         Строка reply_to_cid = O. Строка_опций ("reply_to_cid");
+         Если (reply_to_cid! = NULL &&! Reply_to_cid. Равно (""))   
+ Комментарий. Reply_to_cid =  Длинные. ParseLong (reply_to_cid);
+         Если (о. Имеет ("любит")) {
+             JSONObject jlikes = O. GetJSONObject ("Понравилось");
+ Комментарий. Like_count = jlikes. GetInt ("рассчитывать");
+ Комментарий. User_like = jlikes. GetInt ("user_likes") == 1;
+ Комментарий. Can_like = jlikes. GetInt ("can_like") == 1;
+}
+         Возврат комментарий;
+}
+
+     // Для группы теме Комментарии
+     Общественного  статического  Комментарий  parseTopicComment (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Комментарий комментарий =  новый  комментарий ();
+ Комментарий. Чид =  Длинные. ParseLong (о. GetString ("ID"));
+ Комментарий. From_id =  Длинные. ParseLong (о. GetString ("from_id"));
+ Комментарий. Дата =  Длинные. ParseLong (о. GetString ("Дата"));
+ Комментарий. Сообщение =  Апи. Экранирования (о. GetString ("Текст"));
+         Возврат комментарий;
+}
+     
+     Общественного  статического  Комментарий  parseNoteComment (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Комментарий комментарий =  новый  комментарий ();
+ Комментарий. Чид =  Длинные. ParseLong (о. GetString ("ID"));
+ Комментарий. From_id =  Длинные. ParseLong (о. GetString ("UID"));
+ Комментарий. Дата =  Длинные. ParseLong (о. GetString ("Дата"));
+ Комментарий. Сообщение =  Апи. Экранирования (о. GetString ("сообщение"));
+         Возврат комментарий;
+}
+    
+     Общественного  статического  Комментарий  parseVideoComment (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Комментарий комментарий =  новый  комментарий ();
+ Комментарий. Чид = O. GetLong ("ID");
+ Комментарий. From_id = O. GetLong ("from_id");
+ Комментарий. Дата = о. GetLong ("Дата");
+ Комментарий. Сообщение =  Апи. Экранирования (о. GetString ("сообщение"));
+         Возврат комментарий;
+}
+    
+     Общественного  статического  Комментарий  parsePhotoComment (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Комментарий комментарий =  новый  комментарий ();
+ Комментарий. Чид = O. GetLong ("Сид");
+ Комментарий. From_id = O. GetLong ("from_id");
+ Комментарий. Дата = о. GetLong ("Дата");
+ Комментарий. Сообщение =  Апи. Экранирования (о. GetString ("сообщение"));
+         Возврат комментарий;
+}
+}
9      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / CommentList.java
@@-0,0 +1,9@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.util.ArrayList;
+
+ Общественного  класса  CommentList {
+     Общественного  INT Количество;
+     Общественного  ArrayList <комментарий> комментарии = новый  ArrayList <комментарий> ();
+
+}
17      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Constants.java
@@-0,0 +1,17@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  Константы {
+
+     // Конфиденциальности
+     Общественного  статический  финал  Строка PrivacyAll =  "0";	
+     Общественные  статические  окончательные  Струнные PrivacyOnlyFriends =  "1";
+     Общественные  статические  окончательные  Струнные PrivacyAllFriends =  "2";
+     Общественного  статический  финал  Строка PrivacyOnlyMe =  "3";
+
+     // Комментарий конфиденциальности
+     Общественного  статический  финал  Строка CommentPrivacyAll =  "0";	      
+     Общественные  статические  окончательные  Струнные CommentPrivacyOnlyFriends =  "1";
+     Общественные  статические  окончательные  Струнные CommentPrivacyAllFriends =  "2";
+     Общественного  статический  финал  Строка CommentPrivacyOnlyMe =  "3";
+
+}
16      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Country.java
@@-0,0 +1,16@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Страна {
+     Общественного  долго CID;
+     Общественного  Строка имя,
+
+     Общественного  статического  Страна  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Страна с =  новый  Страна ();
+ С. Чид =  Длинные. ParseLong (о. GetString ("Сид"));
+ С. Имя = O. GetString ("имя");
+         Возврат с;
+}
+}
17      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / FriendsList.java
@@-0,0 +1,17@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  FriendsList {
+
+     Общественного  INT крышка;
+     Общественного  Строка имя,
+
+     Общественного  статического  FriendsList  разбора (JSONObject  о) бросает  JSONException {
+         FriendsList FL =  новый  FriendsList ();
+ FL. Крышка = O. GetInt ("крышка");
+ FL. Имя = O. GetString ("имя");
+         Возврат FL;
+}
+}
7      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Geo.java
@@-0,0 +1,7@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  Гео {
+     Общественного  Строка типа;
+     Общественного  Строка координат;
+     Общественного  Место Место;
+}
20      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Graffiti.java
@@-0,0 +1,20@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Граффити {
+     Общественного  долго ID;
+     Общественного  долго owner_id;
+     Общественного  Строка SRC; // 200 * 100 http://cs10730.vkontakte.ru/u110317842/s_5a43e302.png
+     Общественного  Строка src_big; // 586 * 293 http://cs10730.vkontakte.ru/u110317842/l_f8bc298f.png
+    
+     Общественного  статического  Граффити  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Граффити Граффити =  новый  Граффити ();
+ Граффити. ID = O. OptLong ("GID");
+ Граффити. Owner_id = O. OptLong ("owner_id");
+ Граффити. SRC = о. Строка_опций ("SRC");
+ Граффити. Src_big = O. Строка_опций ("src_big");
+         Возвращения граффити;
+}
+}
54      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Group.java
@@-0,0 +1,54@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.util.ArrayList;
+
+ Импорт  org.json.JSONArray;
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Группа {
+     Общественного  долго GID;
+     Общественного  Строка имя,
+     Общественного  Строка фото; // 50 * 50
+     Общественного  Логическое is_closed;
+    
+     // Это новые поля, которых у нас пока нет в базе
+     // Общественного Строка screen_name;
+     // Общественного Логическое is_admin;
+     Общественного  Строка photo_medium; // 100 * 100
+     Общественного  Строка photo_big; // 200 * 200
+
+     Общественного  статический  Группа  разбора (JSONObject  о) бросает  JSONException {
+         Группа г = новая  группа ();
+ Г. GID = O. GetLong ("GID");
+ Г. Название =  Апи. Экранирования (о. GetString ("Имя"));
+ Г. Фото = O. GetString ("фото");
+ Г. Photo_medium = O. Строка_опций ("photo_medium");
+ Г. Photo_big = O. Строка_опций ("photo_big");
+         Строка is_closed = O. Строка_опций ("is_closed");
+         Если (is_closed! = NULL)
+ Г. Is_closed = is_closed. Равна ("1");
+        
+         // Это новые поля, которых у нас пока нет в базе
+         //g.screen_name=o.optString("screen_name ");
+         // Строка is_admin = o.optString ("is_admin");
+         // Если (is_admin! = NULL)
+         // G.is_admin = is_admin.equals ("1");
+         //g.photo_medium = O.getString ("photo_medium");
+         //g.photo_big = O.getString ("photo_big");
+         Возврат г;
+}
+    
+     Общественные  статические  ArrayList <Группа>  parseGroups (JSONArray  JGroups) бросает  JSONException {
+         ArrayList <Группа> группы = новый  ArrayList <Группа> ();
+         Для (INT я =  0; я <JGroups. Длина (); я ++) {
+             // Для метода groups.get первый элемент - количество
+             Если (! (JGroups. Получить (я) экземпляром  JSONObject))
+                 Продолжить;
+             JSONObject jgroup = (JSONObject) JGroups. Получить (I);
+             Группа группа =  группа. Разбора (jgroup);
+ Группы. Добавить (группу);
+}
+         Возвращения группы;
+}
+}
31      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / GroupTopic.java
@@-0,0 +1,31@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  GroupTopic {
+     Общественного  долго раза в сутки;
+     Общественного  долго GID;
+     Общественного  Строка Название;
+     Общественного  долго создано;
+     Общественного  долго CREATED_BY;
+     Общественного  долго обновляются;
+     Общественного  долго updated_by;
+     Общественного  INT is_closed;
+     Общественного  INT is_fixed;
+     Общественные  INT комментарии;
+    
+     Общественного  статического  GroupTopic  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         GroupTopic тема =  новое  GroupTopic ();
+ Тема. Три раза в день =  Длинные. ParseLong (о. GetString ("три раза в день"));
+ Тема. Название =  Апи. Экранирования (о. GetString ("название"));
+ Тема. Создано =  Длинные. ParseLong (о. GetString ("создана"));
+ Тема. CREATED_BY =  Длинные. ParseLong (о. GetString ("CREATED_BY"));
+ Тема. Обновление =  Длинные. ParseLong (о. GetString ("обновляются"));
+ Тема. Updated_by =  Длинные. ParseLong (о. GetString ("updated_by"));
+ Тема. Is_closed =  Целое. ParseInt (о. GetString ("is_closed"));
+ Тема. Is_fixed =  Целое. ParseInt (о. GetString ("is_fixed"));
+ Тема. Комментарии =  Целое. ParseInt (о. GetString ("комментарии"));
+         Возврат тема;
+}
+}
13      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / KException.java
@@-0,0 +1,13@@
+ Пакет  com.perm.kate.api;
+
+ @ SuppressWarnings ("последовательный")
+ Общественного  класса  KException  распространяется  исключение {
+     KException (INT  код, Строка  сообщение) {
+         Супер (сообщение);
+ Код_ошибки = код;
+}
+     Общественного  INT код_ошибки;
+     // Для капчи
+     Общественного  Строка captcha_img;
+     Общественного  Строка captcha_sid;
+}
20      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Link.java
@@-0,0 +1,20@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Ссылка {
+     Общественного  Строка URL;
+     Общественного  Строка Название;
+     Общественного  Строка Описание;
+     Общественного  Строка image_src;
+
+     Общественного  статического  Ссылка  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Ссылка ссылку =  новый  Ссылка ();
+ Ссылка. Гиперссылка = O. Строка_опций ("гиперссылка");
+ Ссылка. Название =  Апи. Экранирования (о. Строка_опций ("название"));
+ Ссылка. Описание =  Апи. Экранирования (о. Строка_опций ("Описание"));
+ Ссылка. Image_src = O. Строка_опций ("image_src");
+         Возврат ссылку;
+}
+}
9      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Media.java
@@-0,0 +1,9@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  СМИ {
+     Общественного  Строка типа; // приложение, граффити, видео, аудио, фото, posted_photo
+     Общественного  Строка item_id;
+     Общественного  Строка owner_id; // кроме граффити
+     Общественного  Строка thumb_src; // кроме аудио и видео
+     Общественного  Строка app_id; // только приложение
+}
81      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Message.java
@@-0,0 +1,81@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.util.ArrayList;
+ Импорт  org.json.JSONArray;
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Сообщение {
+     Общественного  Строка Дата;
+     Общественного  долго UID;
+     // TODO сделать давно
+     Общественного  Строка середине;
+     Общественного  Строка Название;
+     Общественного  Строка тела;
+     // TODO делают логическое
+     Общественного  Строка read_state;
+     Общественного  логическое is_out;
+     Общественные  ArrayList <Приложение> вложения = новый  ArrayList <Приложение> ();
+     Общественного  Длинные chat_id;
+
+     public  static  Message  parse ( JSONObject  o , boolean  from_history , long  history_uid , boolean  from_chat , long  me ) throws  NumberFormatException , JSONException {
+         Сообщение м =  новый  сообщение ();
+         Если (from_chat) {
+             Долго from_id = O. GetLong ("from_id");
+ М. UID = from_id;
+ М. Is_out = (from_id == меня);
+} Еще,  если (from_history) {
+ М. UID = history_uid;
+             Длинные from_id = O. GetLong ("from_id");
+ М. Is_out =! (From_id == history_uid);
+} Еще {
+             // Тут не очень, потому что при получении списка диалогов если есть моё сообщение, которое я написал в беседу, то в нём UID будет мой. Хотя в других случайх UID всегда собеседника.
+ М. UID = O. GetLong ("UID");
+ М. Is_out = O. GetInt ("из") == 1;
+}
+ М. В середине = O. GetString ("середина");
+ М. Дата = о. GetString ("Дата");
+         Если (! From_history &&! From_chat) 
+ М. Название =  Апи. Экранирования (о. GetString ("название"));
+ М. Тело =  Апи. Экранирования (о. GetString ("тело"));
+ М. Read_state = O. GetString ("read_state");
+         Если (о. Имеет ("chat_id"))
+ М. Chat_id = O. GetLong ("chat_id");
+
+         JSONArray вложения = O. OptJSONArray ("вложения");
+         Если (оборудование! = NULL)
+ М. Вложения = Вложений. ParseAttachments (оборудование, 0, 0);
+         Возврат м;
+}
+
+     Общественного  статического  INT  UNREAD  =  1;	 	 // сообщение не прочитано
+     Общественного  статического  INT  Исходящие  =  2;	 	 // исходящее сообщение
+     Общественного  статического  INT  ответил:  =  4;	 	 // на сообщение был создан ответ
+     Общественного  статического  INT  ВАЖНО  =  8; 	 // помеченное сообщение
+     Общественного  статического  INT  ЧАТ  =  16;    	 // сообщение отправлено через диалог
+     Общественные  статические  INT  ДРУЗЬЯ  =  32;		 // сообщение отправлено другом
+     Общественного  статического  INT  СПАМ  =  64;		 // сообщение помечено как "Спам"
+     Общественного  статического  INT  DELETED  =  128;	 // сообщение удалено (в корзине)
+     Общественного  статического  INT  FIXED  =  256; 		 // сообщение проверено пользователем на спам
+     Общественного  статического  INT  МЕДИА  =  512;		 // сообщение содержит медиаконтент
+     Общественного  статического  INT  Беседа  =  8192;     // беседа
+
+     Общественного  статического  сообщение  разбора (JSONArray) бросает JSONException {  
+         Сообщение м =  новый  сообщение ();
+ М. В середине =. GetString (1);
+ М. UID =. GetLong (3);
+ М. Дата =. GetString (4);
+ М. Название =  Апи. Экранирования (а. GetString (5));
+ М. Тело =  Апи. Экранирования (а. GetString (6));
+         INT флаг =. GetInt (2);
+ М. Read_state = ((флаг и  UNREAD) =!  0)? "0": "1";
+ М. Is_out = (флаг &  Исходящие) =!  0;
+         Если ((флаг и  беседа)! =  0) {
+ М. Chat_id =. GetLong (3) и 63; // сократить 6 последних цифр 
+             JSONObject о =. GetJSONObject (7);
+ М. UID = O. GetLong ("от");
+}
+         //m.attachment = A.getJSONArray (7); ДЕЛАТЬ			 
+         Возврат м;
+}
+}
10      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / NameCases.java
@@-0,0 +1,10@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  NameCases {
+     Общественного  статический  финал  Строка  НОМ  =  "ном"; // по умолчанию
+     Общественного  статический  финал  Строка  GET  =  "ген";
+     Общественного  статический  финал  Строка  DAT  =  "DAT";
+     Общественного  статический  финал  Строка  АКК  =  "Точность";
+     Общественного  статический  финал  Строка  ИНС  =  "модули";
+     Общественного  статический  финал  Строка  ABL  =  "ABL";
+}
108      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / NewsItem.java
@@-0,0 1 108@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.util.ArrayList;
+
+ Импорт  org.json.JSONArray;
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  статьи новостей {
+     Общественного  Строка типа;
+     Общественного  долго source_id;
+     Общественного  долго from_id; // когда пост приходит в комментариях, то в source_id там стена, а в from_id автор сообщения.
+     Общественного  долго дата;
+     Общественного  долго post_id;
+     Общественного  долго copy_owner_id;
+     Общественного  долго copy_post_id;
+     Общественного  Строка текста;
+
+     // Понравилось
+     Общественного  INT like_count;
+     Общественного  логическое user_like;
+
+     // Комментарии
+     Общественного  INT comment_count;
+     Общественного  логическое comment_can_post;
+
+     Общественные  ArrayList <Приложение> вложения = новый  ArrayList <Приложение> ();
+     Общественного  Гео гео;
+     Общественные  ArrayList <Фотография> фото = новый  ArrayList <Фото> (); // исключением стены
+     Общественного  ArrayList <Фото> photo_tags = новый  ArrayList <Фото> (); // исключением стены
+     Общественного  ArrayList <Примечание> заметки; // исключением стены
+     Общественные  ArrayList <Строка> друзья; // UID // кроме стены
+
+     Общественного  Строка comments_json;
+
+     Общественного  статического  статьи новостей  разбора (JSONObject  JİTEM, логические  is_comments) бросает  JSONException {
+         Статьи новостей статьи новостей =  новый  статьи новостей ();
+ Статьи новостей. Тип = JİTEM. GetString ("тип");
+ Статьи новостей. Source_id =  Длинные. ParseLong (JİTEM. GetString ("source_id"));
+         Строка from_id = JİTEM. Строка_опций ("from_id");
+         Если (from_id! = NULL &&! From_id. Равно (""))  
+ Статьи новостей. From_id =  Длинные. ParseLong (from_id);
+ Статьи новостей. Дата = JİTEM. GetLong ("Дата");
+ Статьи новостей. Post_id = JİTEM. OptLong ("post_id");
+ Статьи новостей. Текст =  Апи. Экранирования (JİTEM. Строка_опций ("Текст"));
+ Статьи новостей. Copy_owner_id = JİTEM. OptLong ("copy_owner_id");
+         JSONArray вложения = JİTEM. OptJSONArray ("вложения");
+         Если (оборудование! = NULL)
+ Статьи новостей. Вложения = Вложений. ParseAttachments (оборудование, статьи новостей. Source_id, статьи новостей. Copy_owner_id);
+         Если (JİTEM. Имеет (NewsJTags. КОММЕНТАРИИ)) {
+             JSONObject JComments = JİTEM. GetJSONObject (NewsJTags. КОММЕНТАРИИ);
+ Статьи новостей. Comment_count = JComments. OptInt ("Количество", 0); // однажды была строка нулевой
+ Статьи новостей. Comment_can_post = JComments. GetInt ("can_post") == 1;
+             JSONArray х = JComments. OptJSONArray ("список");
+             Если (х! = NULL)
+ Статьи новостей. Comments_json = х. ToString ();
+}
+         Если (JİTEM. Имеет (NewsJTags. ЛЮБИТ)) {
+             JSONObject jlikes = JİTEM. GetJSONObject (NewsJTags. ЛЮБИТ);
+ Статьи новостей. Like_count = jlikes. GetInt ("рассчитывать");
+ Статьи новостей. User_like = jlikes. GetInt ("user_likes") == 1;
+}
+         Если (JİTEM. Имеет (NewsJTags. PHOTO_TAGS)) {
+             JSONArray jphoto_tags = JİTEM. GetJSONArray (NewsJTags. PHOTO_TAGS);
+ Статьи новостей. Photo_tags =  новый  ArrayList <Фото> ();
+             Для (INT J =  1, J <jphoto_tags. Длина (); J ++) {
+                 JSONObject jphoto_tag = (JSONObject) jphoto_tags. Получить (J);
+                 Фото фото =  фото. Разбора (jphoto_tag);
+ Статьи новостей. Photo_tags. Добавить (фото);
+}
+}
+         Если (JİTEM. Имеет (NewsJTags. ФОТО)) {
+             JSONArray jphotos = JİTEM. GetJSONArray (NewsJTags. ФОТО);
+ Статьи новостей. Фото =  новый  ArrayList <Фото> ();
+             Для (INT J =  1, J <jphotos. Длина (); J ++) {
+                 JSONObject jphoto = (JSONObject) jphotos. Получить (J);
+                 Фото фото =  фото. Разбора (jphoto);
+ Статьи новостей. Фото. Добавить (фото);
+}
+}
+         // В newsfeed.getComments фотка прямо в новости
+         Если (статьи новостей. Тип. Равно ("фото") && is_comments) {
+ Статьи новостей. Фото =  новый  ArrayList <Фото> ();
+             Фото фото =  фото. Разбора (JİTEM);
+ Статьи новостей. Фото. Добавить (фото);
+}
+         Если (JİTEM. Имеет (NewsJTags. ДРУЗЬЯ))
+ {
+             JSONArray jfriends = JİTEM. GetJSONArray (NewsJTags. ДРУЗЬЯ);
+ Статьи новостей. Друзья =  новый  ArrayList <Строка> ();
+             Для (INT J =  1, J <jfriends. Длина (); ++ J) {
+                 JSONObject jfriend = (JSONObject) jfriends. Получить (J);
+ Статьи новостей. Друзья. Добавить (jfriend. GetString ("UID"));
+}
+}
+         Если (JİTEM. Имеет (NewsJTags. ПРИМЕЧАНИЯ))
+ {
+             JSONArray jnotes = JİTEM. GetJSONArray (NewsJTags. ПРИМЕЧАНИЯ);
+ Статьи новостей. Примечания =  новый  ArrayList <Примечание> ();
+             Для (INT J =  1, J <jnotes. Длина (); ++ J) {
+                 JSONObject jnote = (JSONObject) jnotes. Получить (J);
+                 Примечание Примечание =  Примечание. Разбора (jnote, ложь);
+ Статьи новостей. Заметки. Добавить (примечание);
+}
+}
+         Возврат статьи новостей;
+}
+}
15      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / NewsJTags.java
@@-0,0 +1,15@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  NewsJTags {
+     Общественного  статический  финал  Строка  ФОТО  =  "фото";
+     Общественные  статические  окончательные  Струнные  ФОТО  =  "Фотографии";
+     Общественные  статические  окончательные  Струнные  PHOTO_TAGS  =  "photo_tags";
+     Общественные  статические  окончательные  Струнные  ДРУЗЬЯ  =  "друзья";
+     Общественного  статический  финал  Строка  ПРИМЕЧАНИЕ  =  "внимание";
+     Общественные  статические  окончательные  Струнные  ПРИМЕЧАНИЯ  =  "отмечает";
+     Общественного  статический  финал  Строка  ПРИЛОЖЕНИЕ  =  "привязанность";
+     Общественные  статические  окончательные  Струнные  КОММЕНТАРИИ  =  "комментариев";
+     Общественного  статический  финал  Строка  ЛЮБИТ  =  "любит";
+     Общественного  статический  финал  Строка  АУДИО  =  "аудио";
+     Общественного  статический  финал  Строка  ВИДЕО  =  "видео";
+}
11      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / NewsTypes.java
@@-0,0 +1,11@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  NewsTypes {
+     Общественного  статический  финал  Строка  POST  =  "Сообщение";
+     Общественного  статический  финал  Строка  ФОТО  =  "фото";
+     Общественного  статический  финал  Строка  PHOTO_TAG  =  "photo_tag";
+     Общественного  статический  финал  Строка  ДРУГ  =  "друг";
+     Общественного  статический  финал  Строка  ПРИМЕЧАНИЕ  =  "внимание";
+     Общественного  статический  финал  Строка  АУДИО  =  "аудио";
+     Общественного  статический  финал  Строка  ВИДЕО  =  "видео";
+}
40      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Newsfeed.java
@@-0,0 +1,40@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.util.ArrayList;
+ Импорт  org.json.JSONArray;
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Лента новостей {
+     Общественного  ArrayList <статьи новостей> предметы = новый  ArrayList <статьи новостей> ();
+     Общественного  ArrayList <Система> Профили;
+     Общественные  ArrayList <Группа> группы;
+
+     Общественного  статического  Лента новостей  разбора (JSONObject  корень, логические  is_comments) бросает  JSONException {
+         JSONObject response1 = корень. GetJSONObject ("ответ");
+         JSONArray jitems = response1. OptJSONArray ("элементы");
+         JSONArray jprofiles = response1. OptJSONArray ("Профили");
+         JSONArray JGroups = response1. OptJSONArray ("группы");
+         Лента новостей лента новостей =  новый  Лента новостей ();
+         Если (jitems! = NULL) { 
+ Лента новостей. Пункты =  новый  ArrayList <статьи новостей> ();
+             Для (INT я =  0; я <jitems. Длина (); я ++) {
+                 JSONObject JİTEM = (JSONObject) jitems. Получить (я);
+                 Статьи новостей статьи новостей =  статьи новостей. Разбора (JİTEM, is_comments);
+ Лента новостей. Пункты. Добавить (статьи новостей);
+}
+}
+        
+         Если (jprofiles! = NULL) { 
+ Лента новостей. Анкет =  новый  ArrayList <Пользователь> ();
+             Для (INT я =  0; я <jprofiles. Длина (); я ++) {
+                 JSONObject jprofile = (JSONObject) jprofiles. Получить (я);
+                 Пользователь м =  Пользователь. ParseFromNews (jprofile);
+ Лента новостей. Анкет. Добавить (м);
+}
+}
+         Если (JGroups! = NULL) 
+ Лента новостей. Группы =  Группа. ParseGroups (JGroups);
+         Возврат лента новостей;
+}
+} 
35      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Note.java
@@-0,0 +1,35@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Примечание {
+     Общественного  долго нидь;
+     Общественного  долго owner_id;
+     Общественного  Строка Название;
+     Общественного  Строка текста;
+     Общественного  долго дата = 0;
+     Общественного  долго NCOM = - 1;
+     // Общественного долго read_ncom = -1;
+
+     Общественного  статического  Примечание  разбора (JSONObject  о, логическое  is_get) бросает  NumberFormatException, JSONException {
+         Примечание Примечание =  новый  Примечание ();
+         Если (is_get)
+ Примечание. Нидь = O. GetLong ("NID");
+         Еще
+ Примечание. Нидь =  Длинные. ParseLong (о. Строка_опций ("NID"));
+         Если (is_get)
+ Примечание. Owner_id =  Длинные. ParseLong (о. GetString ("UID"));
+         Еще
+ Примечание. Owner_id = O. GetLong ("owner_id");
+ Примечание. Название =  Апи. Экранирования (о. GetString ("название"));
+         Если (is_get)
+ Примечание. NCOM =  Длинные. ParseLong (о. Строка_опций ("NCOM"));
+         Еще
+ Примечание. NCOM = O. OptLong ("NCOM");
+         //note.read_ncom = O.optLong ("read_ncom");
+ Примечание. Текст = O. Строка_опций ("Текст");
+ Примечание. Дата = о. OptLong ("Дата");
+         Возврат записка;
+}
+}
47      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Params.java
@@-0,0 +1,47@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.net.URLEncoder;
+ Импорт  java.util.TreeMap;
+ Импорт  java.util.Map.Entry;
+
+ Общественного  класса  Params {
+     TreeMap <Строка, Строка> аргументы =  новый  TreeMap <Строка, Строка> ();
+     Строка имя_метода;
+    
+     Общественные  Params (Строка  method_name) {
+         Это. Имя_метода = имя_метода;
+}
+
+     Общественного  недействительными  положить (Строка  param_name, Строка  param_value) {
+         Если (param_value == NULL)
+             Возвращения;
+ Аргументы. Положим (param_name, param_value);
+}
+    
+     Общественного  недействительными  положить (Строка  param_name, Лонг  param_value) {
+         Если (param_value == NULL)
+             Возвращения;
+ Аргументы. Положим (param_name, Лонг. ToString (param_value));
+}
+    
+     Общественного  недействительными  положить (Строка  param_name, целое  param_value) {
+         Если (param_value == NULL)
+             Возвращения;
+ Аргументы. Положим (param_name, целое. ToString (param_value));
+}
+    
+     Общественного  недействительными  putDouble (Строка  param_name, дважды  param_value) {
+ Аргументы. Положим (param_name, Двухместный. ToString (param_value));
+}
+    
+     Общественного  Строка  getParamsString () {
+         Строка ПАРАМЕТРЫ = "";
+         Для (запись <Струнные, строки> запись: аргументов. EntrySet ()) {
+             Если (ПАРАМЕТРЫ. Длина ()! = 0)
+ Титулы + = "&";
+ Титулы + = (запись. GetKey () + "=" + URLEncoder. Кодировать (запись. GetValue ()));
+}
+         Возврат Титулы;
+}
+
+}
53      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Photo.java
@@-0,0 +1,53@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.io.Serializable;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  фотография  реализует  Serializable {
+     Частный  статический  финал  долго serialVersionUID =  1L;
+     Общественного  долго ПИД-регулятора;
+     Общественного  долго помощи;
+     Общественного  Строка owner_id;
+     Общественного  Строка ДЗО;
+     Общественного  Струнный src_small; // не используется сейчас, потому что в ленте новостей он пуст
+     Общественного  Строка src_big;
+     Общественного  Строка src_xbig;
+     Общественного  Строка src_xxbig;
+     Общественного  Строка phototext;
+     Общественного  долго создано;
+     Общественного  Целое like_count;
+     Общественные  логические user_likes;
+
+     Общественного  статического  Фото  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Фото стр =  новый  Фото ();
+ Р. PID = O. GetLong ("ПИД");
+ Р. Помощь = O. OptLong ("помощь");
+ Р. Owner_id = O. GetString ("owner_id");
+ Р. SRC = о. GetString ("SRC");
+ Р. Src_small = O. Строка_опций ("src_small");
+ Р. Src_big = O. GetString ("src_big");
+ Р. Src_xbig = O. Строка_опций ("src_xbig");
+ Р. Src_xxbig = O. Строка_опций ("src_xxbig");
+ Р. Phototext =  Апи. Экранирования (о. Строка_опций ("Текст"));
+ Р. Создана = O. OptLong ("создана");
+        
+         Если (о. Имеет ("любит")) {
+             JSONObject jlikes = O. GetJSONObject ("Понравилось");
+ Р. Like_count = jlikes. GetInt ("Количество");
+ Р. User_likes = jlikes. GetInt ("user_likes") == 1;
+}
+         Возврат р;
+}
+
+     Общественного  Фото () {
+}
+
+     Общественного  Фото (Лонг  ID, Строка  owner_id, Строка  SRC, Строка  src_big) {
+         Это. PID = идентификатор;
+         Это. Owner_id = owner_id;
+         Это. SRC = SRC;
+         Это. Src_big = src_big;
+}
+}
6      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / PhotoComment.java
@@-0,0 +1,6@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  PhotoComment {
+     Общественного  фотография фото;
+     Общественного  Комментарий комментарий,
+}
50      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / PhotoTag.java
@@-0,0 +1,50@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  фотометка {
+    
+     Общественного  Длинные owner_id;
+     Общественного  долго ПИД-регулятора;
+    
+     Общественного  долго UID;
+     Общественного  долго tag_id;
+     Общественного  долго placer_id;
+     Общественного  Строка tagged_name;
+     Общественного  долго дата;
+     Общественные  двойные х;
+     Общественного  дважды у;
+     Общественного  дважды х2;
+     Общественного  дважды у2;
+     Общественного  INT рассматривается;
+    
+     Общественного  статического  фотометка  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Фотометка т =  новый  фотометка ();
+ T. UID = O. GetLong ("UID");
+ T. Tag_id = O. OptLong ("tag_id");
+ T. Placer_id = O. OptLong ("placer_id");
+ T. Tagged_name =  Апи. Экранирования (о. Строка_опций ("tagged_name"));
+ T. Дата = O. OptLong ("дата");
+ T. Х = O. OptDouble ("х");
+ T. X2 = O. OptDouble ("х2");
+ T. У = O. OptDouble ("у");
+ T. У2 = O. OptDouble ("у2");
+ T. Просматриваемые = O. OptInt ("рассматривается");
+         Возврат т;
+}
+    
+     Общественного  фотометка () {
+        
+}
+    
+     Общественного  фотометка (Лонг  owner_id, долго  PID, долго  UID, двойные  х, дважды  у, дважды  x2, дважды  у2) {
+         Это. Owner_id = owner_id;
+         Это. PID = ПИД-регулятора;
+         Это. UID = UID;
+         Это. Х = х;
+         Это. У = у;
+         Это. X2 = x2;
+         Это. У2 = у2;
+}
+}
10      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Place.java
@@-0,0 +1,10@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  Место {
+     Общественного  Строка place_id;
+     Общественного  Строка Название;
+     Общественного  Строка типа;
+     Общественного  Строка country_id;
+     Общественного  Строка CITY_ID;
+     Общественного  Строка адрес;
+}
126      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / User.java
@@-0,0 Один тысяча сто двадцать шесть@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONArray;
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ // Поля являются обязательными. Должно быть нулевым, если не заполняется
+ Общественного  класса  пользователя {
+     Общественного  долго UID;
+     Общественного  Строка first_name;
+     Общественного  Строка last_name;
+     Общественного  Строка прозвище;
+     Общественного  целое секс = NULL;
+     Общественного  Логическое онлайн = NULL;
+     Общественного  Строка Дата рождения; // bdate
+     Общественного  Строка фото; // то же самое, photo_rec
+     Общественного  Строка photo_big;
+     Общественного  Строка photo_medium;
+     Общественного  Целое город = NULL;
+     Общественного  Целое страна = NULL;
+     Общественного  Целое часовой пояс = NULL;
+     Общественного  Струнные списки;
+     Общественного  Строка домена;
+     Общественного  Целое ставка = NULL;
+     Общественного  Целое университет = NULL; // если образование
+     Общественного  Строка university_name; // если образование
+     Общественного  Целое факультет = NULL; // если образование
+     Общественного  Строка faculty_name; // если образование
+     Общественного  Целое окончания = NULL; // если образование
+     Общественного  Логическое has_mobile = NULL;
+     Общественного  Строка home_phone;
+     Общественного  Строка mobile_phone;
+     Общественного  Строка состояния;
+     Общественного  Целое отношение;
+     Общественного  Струнные friends_list_ids =  нулевые;
+     Общественного  долго last_seen;
+    
+     Общественного  статического  Пользователь  разбора (JSONObject  о) бросает  JSONException {
+         Пользователь U =  новый  пользователь ();
+ U. UID =  Длинные. ParseLong (о. GetString ("UID"));
+         Если (! О. IsNull ("first_name"))
+ U. First_name =  Апи. Экранирования (о. GetString ("first_name"));
+         Если (! О. IsNull ("last_name"))
+ U. Last_name =  Апи. Экранирования (о. GetString ("last_name"));
+         Если (! О. IsNull ("ник"))
+ U. Прозвище =  Апи. Экранирования (о. Строка_опций ("ник"));
+         Если (! О. IsNull ("домен"))
+ U. Доменов = O. Строка_опций ("домен");
+         Если (! О. IsNull ("онлайн"))
+ U. Онлайн = O. OptInt ("онлайн") == 1;
+         Если (! О. IsNull ("секс"))
+ U. Секс =  Целое. ParseInt (о. Строка_опций ("секс"));
+         Если (! О. IsNull ("bdate"))
+ U. Дата рождения = O. Строка_опций ("bdate");
+         Попытка {
+ U. Город =  Целое. ParseInt (о. Строка_опций ("город"));
+} Поймать (NumberFormatException экс) {}
+         Попытка {            
+ U. Страна =  Целое. ParseInt (о. Строка_опций ("страна"));
+} Поймать (NumberFormatException экс) {}
+         Если (! О. IsNull ("часовой пояс"))
+ U. Часовой пояс = O. OptInt ("часовой пояс");
+         Если (! О. IsNull ("фото"))
+ U. Фото = O. Строка_опций ("фото");
+         Если (! О. IsNull ("photo_medium"))
+ U. Photo_medium = O. Строка_опций ("photo_medium");
+         Если (! О. IsNull ("photo_big"))
+ U. Photo_big = O. Строка_опций ("photo_big");
+         Если (! О. IsNull ("has_mobile"))
+ U. Has_mobile = O. OptInt ("has_mobile") == 1;
+         Если (! О. IsNull ("home_phone"))
+ U. Home_phone = O. Строка_опций ("home_phone");
+         Если (! О. IsNull ("mobile_phone"))
+ U. Mobile_phone = O. Строка_опций ("mobile_phone");
+         Если (! О. IsNull ("Скорость"))
+ U. Скорость =  Целое. ParseInt (о. Строка_опций ("Скорость"));
+         Попытка {
+ U. Факультет =  Целое. ParseInt (о. Строка_опций ("Факультет"));
+} Поймать (NumberFormatException экс) {}
+         Если (! О. IsNull ("faculty_name"))
+ U. Faculty_name = O. Строка_опций ("faculty_name");
+         Попытка {
+ U. Университет =  Целое. ParseInt (о. Строка_опций ("Университет"));
+} Поймать (NumberFormatException экс) {}
+         Если (! О. IsNull ("university_name"))
+ U. University_name = O. Строка_опций ("university_name");
+         Попытка {
+ U. Выпуск =  Целое. ParseInt (о. Строка_опций ("градации"));
+} Поймать (NumberFormatException экс) {}
+         Если (! О. IsNull ("деятельность"))
+ U. Статус =  Апи. Экранирования (о. Строка_опций ("деятельность"));
+         Если (! О. IsNull ("отношение"))
+ U. Отношение = O. OptInt ("отношение");
+         Если (! О. IsNull ("списки")) {
+             JSONArray массив = O. OptJSONArray ("списки");
+             Если (массив! = NULL) { 
+                 Строка IDS =  "";
+                 Для (INT я = 0; я <массив. Длина () - 1; ++ я)
+ IDS + = массив. GetString (я) +  ",";
+ IDS + = массив. GetString (массив. Длина () - 1);
+ U. Friends_list_ids = идентификаторы;
+}
+}
+         Если (! О. IsNull ("last_seen")) {
+             JSONObject объект = O. OptJSONObject ("last_seen");
+             Если (объект! = NULL) 
+ U. Last_seen = объект. OptLong ("Время");
+}
+         Возвращения и;
+}
+    
+     Общественные  статические  Система  parseFromNews (JSONObject  jprofile) бросает  JSONException {
+         Пользователь м =  новый  пользователь ();
+ М. UID =  Длинные. ParseLong (jprofile. GetString ("UID"));
+ М. First_name =  Апи. Экранирования (jprofile. GetString ("first_name"));
+ М. Last_name =  Апи. Экранирования (jprofile. GetString ("last_name"));
+ М. Фото = jprofile. GetString ("фото");
+         Попытка {
+ М. Пола =  Целое. ParseInt (jprofile. Строка_опций ("секс"));
+} Поймать (NumberFormatException экс) {
+             // Если там мусор, то мы это пропускаем
+ Экс. PrintStackTrace ();
+}
+         Возврат м;
+}
+}
36      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / Video.java
@@-0,0 +1,36@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  Видео {
+     Общественного  долго VID;
+     Общественного  долго owner_id;
+     Общественного  Строка Название;
+     Общественного  Строка Описание;
+     Общественного  долго продолжительность;
+     Общественного  Строка ссылку;
+     Общественного  Строка изображения;
+     Общественного  долго дата;
+     Общественного  Строка проигрыватель;
+
+     Общественного  статического  Видео  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         Видео v =  новый  видео ();
+         Если (о. Имеет ("VID"))
+ V. VID = O. GetLong ("VID");
+         Если (о. Имеет ("ID")) //video.getUserVideos
+ V. VID =  Длинные. ParseLong (о. GetString ("ID"));
+ V. Owner_id = O. GetLong ("owner_id");
+ V. Название =  Апи. Экранирования (о. GetString ("название"));
+ V. Продолжительность = O. GetLong ("Продолжительность");
+ V. Описание =  Апи. Экранирования (о. Строка_опций ("Описание"));
+         Если (о. Имеет ("изображение"))
+ V. Изображение = O. Строка_опций ("изображение");
+         Если (о. Имеет ("палец")) //video.getUserVideos
+ V. Изображение = O. Строка_опций ("палец");
+ V. Ссылку = O. Строка_опций ("ссылка");
+ V. Дата = о. OptLong ("Дата");
+ V. Игрок = O. Строка_опций ("Игрок");
+         Возврат v;
+}
+}
8      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / VkApp.java
@@-0,0 +1,8@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  VkApp {
+     Общественного  Строка app_id;
+     Общественного  Строка app_name;
+     Общественного  Строка ДЗО;
+     Общественного  Строка src_big;
+}
55      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / VkPoll.java
@@-0,0 +1,55@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.util.ArrayList;
+
+ Импорт  org.json.JSONArray;
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  VkPoll {
+     Общественного  долго ID;
+     Общественного  Строка вопрос;
+     Общественного  долго owner_id;
+     Общественного  Лонг создал;
+     Общественные  Длинные голосов;
+     Общественного  Длинные answer_id;
+     Общественного  Строка answers_json;
+    
+     Общественного  статического  VkPoll  разбора (JSONObject  о) бросает  NumberFormatException, JSONException {
+         VkPoll v =  новый  VkPoll ();
+ V. ID = O. GetLong ("poll_id");
+ V. Вопрос =  Апи. Экранирования (о. GetString ("Вопрос"));
+         Если (о. Имеет ("owner_id"))
+ V. Owner_id = O. GetLong ("owner_id");
+         Если (о. Имеет ("создана"))
+ V. Создано = O. GetLong ("создана");
+         Если (о. Имеет ("голосов"))
+ V. Голосов = O. GetLong ("голосов");
+         Если (о. Имеет ("answer_id"))
+ V. Answer_id = O. GetLong ("answer_id");
+         Если (о. Имеет ("ответы"))
+ V. Answers_json = O. GetJSONArray ("ответы"). ToString ();
+         Возврат v;
+}
+
+     Общественные  статические  ArrayList <VkPollAnswer>  getPollAnswers (Строка  answers_json) {
+         ArrayList <VkPollAnswer> ответы =  новый  ArrayList <VkPollAnswer> ();
+         Попытка {
+             JSONArray массив =  новый  JSONArray (answers_json);
+             Для (INT я = 0, я <массив. Длину (); ++ я) {
+                 Если (массив. Получить (я) экземпляром  JSONObject  ==  ложь)
+                     Продолжить;
+                 JSONObject о = (JSONObject) массив. Получить (I);
+                 VkPollAnswer годовых =  новый  VkPollAnswer ();
+ Годовых. ID = O. GetLong ("ID");
+ Годовых. Голосов = O. GetInt ("голоса");
+ Годовых. Текст =  Апи. Экранирования (о. GetString ("Текст"));
+ Годовых. Скорость = O. GetInt ("Скорость");
+ Ответы. Добавить (PA);
+}
+} Поймать (JSONException е) {
+ Е. PrintStackTrace ();
+}
+         Возврат ответы;
+}
+}
8      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / VkPollAnswer.java
@@-0,0 +1,8@@
+ Пакет  com.perm.kate.api;
+
+ Общественного  класса  VkPollAnswer {
+     Общественного  долго ID;
+     Общественные  INT голосов;
+     Общественного  Строка текста;
+     Общественного  INT ставка;
+}
56      AndroidVkSdk / SRC / COM / Пермь / Кейт / API / WallMessage.java
@@-0,0 +1,56@@
+ Пакет  com.perm.kate.api;
+
+ Импорт  java.util.ArrayList;
+
+ Импорт  org.json.JSONArray;
+ Импорт  org.json.JSONException;
+ Импорт  org.json.JSONObject;
+
+ Общественного  класса  WallMessage {
+     Общественного  долго from_id;
+     Общественного  долго to_id;
+     Общественного  долго дата;
+     Общественного  Строка текста;
+     Общественного  долго ID;
+     Общественный  строки в режиме онлайн;
+     Общественные  ArrayList <Приложение> вложения;
+     Общественного  долго comment_count;
+     Общественного  логическое comment_can_post;
+
+     // Понравилось
+     Общественного  INT like_count;
+     Общественного  логическое user_like;
+     Общественного  логическое can_like;
+     Общественного  логическое like_can_publish;
+    
+     Общественного  долго copy_owner_id = 0;
+     Общественного  долго copy_post_id = 0;
+    
+     Общественного  статического  WallMessage  разбора (JSONObject  о) бросает  JSONException {
+         WallMessage WM =  новый  WallMessage ();
+ WM. ID = O. GetLong ("ID");
+ WM. From_id = O. GetLong ("from_id");
+ WM. To_id = O. GetLong ("to_id");
+ WM. Дата = о. GetLong ("Дата");
+ WM. Онлайн = O. GetString ("онлайн");
+ WM. Текст =  Апи. Экранирования (о. GetString ("Текст"));
+         Если (о. Имеет ("любит")) {
+             JSONObject jlikes = O. GetJSONObject (NewsJTags. ЛЮБИТ);
+ WM. Like_count = jlikes. GetInt ("рассчитывать");
+ WM. User_like = jlikes. GetInt ("user_likes") == 1;
+ WM. Can_like = jlikes. GetInt ("can_like") == 1;
+ WM. Like_can_publish = jlikes. GetInt ("can_publish") == 1;
+}
+ WM. Copy_owner_id = O. OptLong ("copy_owner_id");
+         JSONArray вложения = O. OptJSONArray ("вложения");
+         Если (оборудование! = NULL)
+             // Владельцем опроса является to_id. Даже если добавить опрос в группу от своего имени, то from_id буду я, но опрос всё-равно будет принадлежать группе.
+ WM. Вложения = Вложений. ParseAttachments (оборудование, WM. To_id, WM. Copy_owner_id);
+         Если (о. Имеет ("комментарии")) {
+             JSONObject JComments = O. GetJSONObject ("комментарии");
+ WM. Comment_count = JComments. GetInt ("Количество");
+ WM. Comment_can_post = JComments. GetInt ("can_post") == 1;
+}
+         Возврат WM;
+}
+}
37      AndroidVkSdk / SRC / COM / Пермь / утилиты / Utils.java
@@-0,0 +1,37@@
+ Пакет  com.perm.utils;
+
+ Импорт  java.io.IOException;
+ Импорт  java.io.InputStream;
+ Импорт  java.io.InputStreamReader;
+ Импорт  java.io.StringWriter;
+ Импорт  java.util.regex.Matcher;
+ Импорт  java.util.regex.Pattern;
+
+ Общественного  класса  утилиты {
+    
+     Общественного  статического  Строка  extractPattern (Строка  Строка, Строка  рисунок) {
+         Шаблон р =  шаблон. Компилировать (рисунок);
+         Сличитель м = р. Совпадений (строка);
+         Если (! М. Найти ())
+             Возврат  NULL;
+         Возврат м. ToMatchResult (). Группа (1);
+}
+    
+     Общественного  статического  Строка  convertStreamToString (InputStream  является) бросает  IOException {
+         InputStreamReader г =  новая  InputStreamReader (есть);
+         StringWriter SW =  новый  StringWriter ();
+         Обугливается [] буфера =  новый  символ [1024];
+         Попытка {
+             Для (INT п; (п = т. Читал (буфер)) =!  - 1;)
+ SW. Написать (буфер, 0, N);
+}
+         Наконец {
+             Попытка {
+ Является. Close ();
+} Поймать (IOException e1) {
+ Е1. PrintStackTrace ();
+}
+}
+         Возврат SW. ToString ();
+}
+}
12      AndroidVkSdk / SRC / COM / Пермь / утилиты / WrongResponseCodeException.java
@@-0,0 +1,12@@
+ Пакет  com.perm.utils;
+
+ Импорт  java.io.IOException;
+
+ Общественного  класса  WrongResponseCodeException  распространяется  IOException {
+     Частный  статический  финал  долго serialVersionUID =  1L;
+
+     Общественного  WrongResponseCodeException (Строка  сообщение) {
+         Супер (сообщение);
+}
+
+}
8      AndroidVkSdkSample / .classpath
@@-0,0 +1,8@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <Классам>
+ <Classpathentry  вид = "SRC" Путь = "SRC" /> 
+ <Classpathentry  вид = "SRC" Путь = "поколения" /> 
+ <Classpathentry  вид = "кон" Путь = "com.android.ide.eclipse.adt.ANDROID_FRAMEWORK" /> 
+ <Classpathentry  вид = "мошенники" путь = "com.android.ide.eclipse.adt.LIBRARIES" /> 
+ <Classpathentry  вид = "Выход" Путь = "Bin / классы" /> 
+ </ Классам>
33      AndroidVkSdkSample / .project
@@-0,0 +1,33@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <ProjectDescription>
+ <Имя> AndroidVkSdkSample </ имя>
+ <Комментарий> </ комментарий>
+ <Проекты>
+ </ Проекты>
+ <BuildSpec>
+ <BuildCommand>
+ <Имя> com.android.ide.eclipse.adt.ResourceManagerBuilder </ имя>
+ <Аргументы>
+ </ Аргументы>
+ </ BuildCommand>
+ <BuildCommand>
+ <Имя> com.android.ide.eclipse.adt.PreCompilerBuilder </ имя>
+ <Аргументы>
+ </ Аргументы>
+ </ BuildCommand>
+ <BuildCommand>
+ <Имя> org.eclipse.jdt.core.javabuilder </ имя>
+ <Аргументы>
+ </ Аргументы>
+ </ BuildCommand>
+ <BuildCommand>
+ <Имя> com.android.ide.eclipse.adt.ApkBuilder </ имя>
+ <Аргументы>
+ </ Аргументы>
+ </ BuildCommand>
+ </ BuildSpec>
+ <Натуры>
+ <Природа> com.android.ide.eclipse.adt.AndroidNature </ природа>
+ <Природа> org.eclipse.jdt.core.javanature </ природа>
+ </ Природа>
+ </ ProjectDescription>
31      AndroidVkSdkSample / AndroidManifest.xml
@@-0,0 +1,31@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <Проявляются  XMLNS: Android = "http://schemas.android.com/apk/res/android"
+     Пакет = "com.perm.kate.api.sample"
+     Андроид: versionCode = "1"
+     Андроид: versionName = "1.0"
+>
+
+ <Использования  SDK-андроид: minSdkVersion = "4" />
+    
+ <Использования-разрешение  Android: Название = "android.permission.INTERNET" />
+
+ <Приложение
+         Андроид: значок = "@ рисуем / ic_launcher"
+         Андроид: этикетка = "@ строка / app_name"
+>
+ <Деятельность
+             Андроид: имя = ".MainActivity"
+             Андроид: этикетка = "@ строка / app_name"
+>
+ <Намерения фильтр>
+ <Действие  андроид: имя = "android.intent.action.MAIN" />
+ <Категория  андроид: имя = "android.intent.category.LAUNCHER" />
+ </ Намерения фильтр>
+ </ Деятельность>
+ <Деятельность  андроид: имя = ".LoginActivity"
+             Андроид: configChanges = "keyboardHidden | ориентация"
+             Андроид: этикетка = "@ строка / app_name"
+ />
+ </ Приложение>
+
+ </ Проявляются> 
40      AndroidVkSdkSample / proguard.cfg
@@-0,0 +1,40@@
+ -optimizationpasses 5
+ -dontusemixedcaseclassnames
+ -dontskipnonpubliclibraryclasses
+ -dontpreverify
+ -verbose
+ -optimizations! Код / упрощение / арифметика, поля! / * ,! класс / слияния / *
+
+ -keep общественного класса * расширяет android.app.Activity
+ -keep общественного класса * расширяет android.app.Application
+ -keep общественного класса * расширяет android.app.Service
+ -keep общественного класса * расширяет android.content.BroadcastReceiver
+ -keep общественного класса * расширяет android.content.ContentProvider
+ -keep общественного класса * расширяет android.app.backup.BackupAgentHelper
+ -keep общественного класса * расширяет android.preference.Preference
+ -keep общественного класса com.android.vending.licensing.ILicensingService
+
+ -keepclasseswithmembernames класс * {
+ Родные <методы>;
+}
+
+ -keepclasseswithmembers класс * {
+ Общественного <инициализации> (android.content.Context, android.util.AttributeSet);
+}
+
+ -keepclasseswithmembers класс * {
+ Общественного <инициализации> (android.content.Context, android.util.AttributeSet, INT);
+}
+
+ -keepclassmembers класс * расширяет android.app.Activity {
+ Общественного недействительными * (android.view.View);
+}
+
+ -keepclassmembers перечисление * {
+ Общественности статической ** [] значения ();
+ Общественности статической ** valueOf (java.lang.String);
+}
+
+ -keep класс * реализует android.os.Parcelable {
+ Общественности статической окончательный android.os.Parcelable $ Творец *;
+}
12      AndroidVkSdkSample / project.properties
@@-0,0 +1,12@@
+ # Этот файл автоматически генерируется Android Tools.
+ # Не изменяйте этот файл - ваши изменения будут стерты!
+ #
+ # Этот файл должен быть проверен в системах контроля версий.
+ #
+ # Чтобы настроить свойства, используемые Ant использования системы сборки,
+ # "Ant.properties", и значения вручную, чтобы адаптировать сценарий к вашему
+ # Структура проекта.
+
+ # Цель проекта.
+ Цель = андроид-4
+ Android.library.reference.1 = .. / AndroidVkSdk
ОГРН  AndroidVkSdkSample / RES / рисуем-ИПЧР / ic_launcher.png

ОГРН  AndroidVkSdkSample / RES / рисуем-ldpi / ic_launcher.png

ОГРН  AndroidVkSdkSample / RES / рисуем-MDPI / ic_launcher.png

13      AndroidVkSdkSample / RES / макет / login.xml
@@-0,0 +1,13@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <LinearLayout 
+ XMLNS: Android = "http://schemas.android.com/apk/res/android"
+     Андроид: ориентация = "вертикали"
+     Андроид: layout_width = "fill_parent"
+     Андроид: layout_height = "fill_parent"
+>
+ <WebView 
+         Андроид: ID = "@ + ID / facebookview"
+         Андроид: layout_width = "fill_parent"
+         Андроид: layout_height = "fill_parent"
+ />
+ </ LinearLayout>
34      AndroidVkSdkSample / RES / макет / main.xml
@@-0,0 +1,34@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <LinearLayout  XMLNS: Android = "http://schemas.android.com/apk/res/android"
+     Андроид: layout_width = "fill_parent"
+     Андроид: layout_height = "fill_parent"
+     Андроид: ориентация = "вертикальной">
+
+ <Кнопка
+         Андроид: ID = "@ + ID / разрешать"
+         Андроид: layout_width = "fill_parent"
+         Андроид: layout_height = "wrap_content"
+         Андроид: текст = "Авторизация"
+ />
+    
+ <EditText
+         Андроид: ID = "@ + ID / сообщение"
+         Андроид: layout_width = "fill_parent"
+         Андроид: layout_height = "wrap_content"
+         Андроид: текст = "Тестовая запись на стене"
+ />
+ <Кнопка
+         Андроид: ID = "@ + ID / пост"
+         Андроид: layout_width = "fill_parent"
+         Андроид: layout_height = "wrap_content"
+         Андроид: текст = "Отправить запись на стену"
+ />
+    
+ <Кнопка
+         Андроид: ID = "@ + ID / выход"
+         Андроид: layout_width = "fill_parent"
+         Андроид: layout_height = "wrap_content"
+         Андроид: текст = "Выход"
+ />
+
+ </ LinearLayout> 
6      AndroidVkSdkSample / RES / значения / strings.xml
@@-0,0 +1,6@@
+ <? XML версия = "1.0" кодирования = "UTF-8"?>
+ <Ресурсы>
+
+ <Строка  имя = "app_name"> AndroidVkSdkSample </ строка>
+
+ </ Ресурсы> 
25      AndroidVkSdkSample / SRC / COM / Пермь / Кейт / API / образец / Account.java
@@-0,0 +1,25@@
+ Пакет  com.perm.kate.api.sample;
+
+ Импортные  android.content.Context;
+ Импортные  android.content.SharedPreferences;
+ Импорт  android.content.SharedPreferences.Editor;
+ Импорт  android.preference.PreferenceManager;
+
+ Общественного  класса  счета {
+     Общественного  Строка access_token;
+     Общественного  долго user_id;
+    
+     Общественного  недействительными  сохранить (Context  контекст) {
+         SharedPreferences привилегированные =  PreferenceManager. GetDefaultSharedPreferences (контекста);
+         Редактор редактор = префы. Редактировать ();
+ Редактор. PutString ("access_token", access_token);
+ Редактор. PutLong ("user_id", user_id);
+ Редактор. Совершению ();
+}
+    
+     Общественного  недействительными  восстановить (Context  контекст) {
+         SharedPreferences привилегированные =  PreferenceManager. GetDefaultSharedPreferences (контекста);
+ Access_token = префы. GetString ("access_token", NULL);
+ User_id = префы. GetLong ("user_id", 0);
+}
+}
7      AndroidVkSdkSample / SRC / COM / Пермь / Кейт / API / образец / Constants.java
@@-0,0 +1,7@@
+ Пакет  com.perm.kate.api.sample;
+
+ Общественного  класса  Константы {
+     // Этот ID предназначен только для примера. Пожалуйста замение его ID своего приложения.
+     Общественного  статического  Строка  api_id = "2904017";
+
+}
70      AndroidVkSdkSample / SRC / COM / Пермь / Кейт / API / образец / LoginActivity.java
@@-0,0 +1,70@@
+ Пакет  com.perm.kate.api.sample;
+
+ Импорт  com.perm.kate.api.Auth;
+ Импорт  android.app.Activity;
+ Импорт  android.content.Intent;
+ Импорт  android.graphics.Bitmap;
+ Импорт  android.os.Bundle;
+ Импорт  android.util.Log;
+ Импорт  android.webkit.CookieManager;
+ Импорт  android.webkit.CookieSyncManager;
+ Импорт  android.webkit.WebView;
+ Импорт  android.webkit.WebViewClient;
+ Импорт  com.perm.kate.api.sample.R;
+
+ Общественного  класса  LoginActivity  расширяет  активность {
+     Частный  статический  финал  Строка  TAG  =  "Kate.LoginActivity";
+
+     WebView WebView;
+    
    +Override
+     Общественного  недействительными  OnCreate (Bundle  savedInstanceState) {
+         Супер. OnCreate (savedInstanceState);
+ SetContentView (R. Макета. Войти);
+        
+ WebView = (WebView) findViewById (R. ID. Facebookview);
+ WebView. GetSettings (). SetJavaScriptEnabled (правда);
+ WebView. ClearCache (правда);
+        
+         // × òîáû Получить ÷ äöü óâåäîìëåíèÿ Ia îêîí ÷ AIEE çàãðóçêè ñòðàíèöû
+ WebView. SetWebViewClient (новый  FacebookWebViewClient ());
+                
+         // Иначе CookieManager упадет с java.lang.IllegalStateException: CookieSyncManager :: CreateInstance () должен быть вызван до CookieSyncManager :: GetInstance ()
+         CookieSyncManager. CreateInstance (это);
+        
+         CookieManager cookieManager =  CookieManager. ДеЫпзЬапсе ();
+ CookieManager. RemoveAllCookie ();
+        
+         Строка гиперссылка = Авт. GetURL (Константы. Api_id, Auth. GetSettings ());
+ WebView. LoadUrl (URL);
+}
+    
+     Класс  FacebookWebViewClient  распространяется  WebViewClient {
        +Override
+         Общественного  недействительными  onPageStarted (WebView  вид, Строка  гиперссылка, растровый  Favicon) {
+             Супер. OnPageStarted (вид, гиперссылка, Favicon);
+ ParseUrl (URL);
+}
+}
+    
+     Частного  недействительными  parseUrl (Строка  гиперссылка) {
+         Попытка {
+             Если (гиперссылка == NULL)
+                 Возвращения;
+             Авторизация. Я (TAG, "URL =" + URL);
+             Если (гиперссылка. StartsWith (Авт. REDIRECT_URL))
+ {
+                 Если (! Гиперссылка. Содержит ("Ошибка =")) {
+                     Строка [] авт = Авт. ParseRedirectUrl (URL);
+                     Намерение Намерение = новый  Намерение ();
+ Намерения. PutExtra ("маркер", авт [0]);
+ Намерения. PutExtra ("user_id", Лонг. ParseLong (авт [1]));
+ SetResult (активность. RESULT_OK, намерение);
+}
+ Отделка ();
+}
+} Поймать (Exception е) {
+ Е. PrintStackTrace ();
+}
+}
+} 
138      AndroidVkSdkSample / SRC / COM / Пермь / Кейт / API / образец / MainActivity.java
@@-0,0 Тысяча сто тридцать восемь@@
+ пакет com.perm.kate.api.sample;
+
+ com.perm.kate.api.Api импорта;
+ android.app.Activity импорта;
+ android.content.Intent импорта;
+ android.os.Bundle импорта;
+ android.view.View импорта;
+ android.view.View.OnClickListener импорта;
+ импорт android.widget.Button;
+ импортные android.widget.EditText;
+ импорт android.widget.Toast;
+
+ открытый класс MainActivity расширяет активность {
+    
+ Частный финал INT REQUEST_LOGIN = 1;
+    
+ Кнопка authorizeButton;
+ Кнопка logoutButton;
+ Кнопка postButton;
+ EditText messageEditText;
+    
+ Общий счет = новый аккаунт ();
+ API API;
+    
+Override
+ Общественного недействительными OnCreate (Bundle savedInstanceState) {
+ Super.onCreate (savedInstanceState);
+ SetContentView (R.layout.main);
+        
+ SetupUI ();
+        
+ //
+ Account.restore (это);
+        
+ // API
+, Если (account.access_token! = NULL)
+ API = Новый API (account.access_token, Constants.API_ID);
+        
+ ShowButtons ();
+}
+
+ Частного недействительными setupUI () {
+ AuthorizeButton = (кнопка) findViewById (R.id.authorize);
+ LogoutButton = (кнопка) findViewById (R.id.logout);
+ PostButton = (кнопка) findViewById (R.id.post);
+ MessageEditText = (EditText) findViewById (R.id.message);
+ AuthorizeButton.setOnClickListener (authorizeClick);
+ LogoutButton.setOnClickListener (logoutClick);
+ PostButton.setOnClickListener (postClick);
+}
+    
+ Частного OnClickListener authorizeClick = новый OnClickListener () {
+Override
+ Общественного недействительными OnClick (Посмотреть v) {
+ StartLoginActivity ();
+}
+};
+    
+ Частного OnClickListener logoutClick = новый OnClickListener () {
+Override
+ Общественного недействительными OnClick (Посмотреть v) {
+ Выход ();
+}
+};
+    
+ Частного OnClickListener postClick = новый OnClickListener () {
+Override
+ Общественного недействительными OnClick (Посмотреть v) {
+ PostToWall ();
+}
+};
+    
+ Частного недействительными startLoginActivity () {
+ Намерение Намерение = новый Намерение ();
+ Intent.setClass (это, LoginActivity.class);
+ StartActivityForResult (намерение, REQUEST_LOGIN);
+}
+    
+Override
+ Защищен недействительными onActivityResult (INT requestCode, INT ResultCode, Intent данных) {
+, Если (== requestCode REQUEST_LOGIN) {
+, Если (== ResultCode RESULT_OK) {
+ // 
+ Account.access_token = data.getStringExtra ("маркер");
+ Account.user_id = data.getLongExtra ("user_id", 0);
+ Account.save (MainActivity.this);
+ API = Новый API (account.access_token, Constants.API_ID);
+ ShowButtons ();
+}
+}
+}
+    
+ Частного недействительными postToWall () {
+ // Пользовательский интерфейс
+ Новое Автор () {
+Override
+ Общественного недействительными Run () {
+ Попробуйте {
+ Текст String = messageEditText.getText () ToString ().
+ Api.createWallPost (account.user_id, текст, NULL, NULL, ложь, ложь, NULL, NULL);
+ // Интерфейс 
+ RunOnUiThread (successRunnable);
+} Улов (Исключение е) {
+ E.printStackTrace ();
+}
+}
+} .start ();
+}
+    
+ Runnable successRunnable = новый Runnable () {
+Override
+ Общественного недействительными Run () {
+ Toast.makeText (getApplicationContext (), "", Toast.LENGTH_LONG) .show ();
+}
+};
+    
+ Частного недействительными Выход () {
+ API = NULL;
+ Account.access_token = NULL;
+ Account.user_id = 0;
+ Account.save (MainActivity.this);
+ ShowButtons ();
+}
+    
+ Недействительными showButtons () {
+, Если (API! = NULL) {
+ AuthorizeButton.setVisibility (View.GONE);
+ LogoutButton.setVisibility (View.VISIBLE);
+ PostButton.setVisibility (View.VISIBLE);
+ MessageEditText.setVisibility (View.VISIBLE);
+} Еще {
+ AuthorizeButton.setVisibility (View.VISIBLE);
+ LogoutButton.setVisibility (View.GONE);
+ PostButton.setVisibility (View.GONE);
+ MessageEditText.setVisibility (View.GONE);
+}
+}
+} 
