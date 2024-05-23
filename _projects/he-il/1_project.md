---
lang: he-il
page_id: project_1
layout: page
title: פרויקט 1
description: עם תמונת רקע
img: /assets/img/12.jpg
importance: 1
category: work
related_publications: true
---
<div dir=rtl markdown=1>
    לכל פרויקט יש דף תצוגה יפהפה.
    ניתן בפשטות להוסיף תמונות בגריד גמיש של 3 עמודות.
    מקמו את תמונותכם ברוחב 1/3, 2/3 או רוחב מלא.

    כדי להוסיף תמונת רקע סדף הפורטפוליו, פשוט הוסיפו את התגית `img` ל-`front matter` בצורה הבאה:

        ---
        layout: page
        title: project
        description: a project with a background image
        img: /assets/img/12.jpg
        ---

    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="caption">
        הוסף תיאור לתמונות בפשטות. משמאל, דרך שעוברת בתוך מנהרה. באמצע, עלים נושרים בצורה אומנותית בצילום היפסטרי. מימין, עוד צילום היפסטרי, חוטב עצים מחזיק חופן של מחטי אורן. 
    </div>
    <div class="row">
        <div class="col-sm mt-3 mt-md-0">
            {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="caption">
        גם התמונה הזאת יכולה לקבל תיאור. זה כמו קסם.
    </div>

    אפשר גם פשוט לשים טקסט רגיל בין שורות של תמונות, אפילו ציטוטים {% cite einstein1950meaning %}.
    נניח שרציתם לכתוב קצת על הפרויקט שלכם לפני שפרסמתם את שאר התמונות.
    שתאם איך עמלתם, הזעתם, _דיממתם_ למען הפרויקט, ואז... אתם חושפים את מלוא הדרו בשורת התמונות הבאה.

    <div class="row justify-content-sm-center">
        <div class="col-sm-8 mt-3 mt-md-0">
            {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
        <div class="col-sm-4 mt-3 mt-md-0">
            {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        </div>
    </div>
    <div class="caption">
        אפשר גם סגנון אומנותי של תמונות מחולקות 2/3 + 1/3 כמו אלו.
    </div>

    הקוד הזה פשוט.
    פשוט עטפו את התמונות עם `<div class="col-sm">` ושימו אותם בתוך `<div class="row">` (קראו עוד על ה<a href="https://getbootstrap.com/docs/4.4/layout/grid/">גריד של Bootstrap</a> system).
    כדי שתמונות יהיו דינמיות, הוסיפו את מחלקת `img-fluid` לכל אחת מהן; לפינות מעוגלות וצללים השתמשו במחלקות `rounded` ו-`z-depth-1`.
    הנה הקוד עבור שורת התמונות האחרונה שמעל:

    {% raw %}

    ```html
    <div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    </div>
    ```

    {% endraw %}
</div>