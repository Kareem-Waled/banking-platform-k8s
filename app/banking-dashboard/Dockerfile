
# ابدأ من nginx خفيفة
FROM nginx:1.25-alpine

# احذف الـ config الافتراضي
RUN rm /etc/nginx/conf.d/default.conf

# انسخ الـ config بتاعنا
COPY nginx.conf /etc/nginx/conf.d/default.conf

# انسخ الـ HTML للمجلد الصح
COPY index.html /usr/share/nginx/html/index.html

# افتح البورت
EXPOSE 80

# nginx بيشتغل أوتوماتيك
CMD ["nginx", "-g", "daemon off;"]
