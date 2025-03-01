# استفاده از نسخه رسمی Drupal 9
FROM drupal:9

# نصب پکیج‌های لازم
RUN apt-get update && \
    apt-get install -y git && \
    rm -rf /var/lib/apt/lists/*

# تغییر دایرکتوری به محل قالب‌ها
WORKDIR /var/www/html/themes

# کلون کردن شاخه 5.0.x قالب Bootstrap از مخزن Git
RUN git clone --branch 5.0.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

# برگشت به دایرکتوری پیش‌فرض در Drupal
WORKDIR /var/www/html
