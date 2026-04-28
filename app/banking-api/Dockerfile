# الخطوة 1: ابدأ من Node.js version 18 (خفيفة - alpine)
FROM node:18-alpine

# الخطوة 2: اعمل مجلد للتطبيق جوه الـ container
WORKDIR /app

# الخطوة 3: انسخ ملفات الـ dependencies الأول (للـ caching)
COPY package.json .

# الخطوة 4: ثبّت الـ dependencies
RUN npm install --production

# الخطوة 5: انسخ باقي الكود
COPY app.js .

# الخطوة 6: شغّل بـ user مش root (أمان)
RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser

# الخطوة 7: افتح البورت
EXPOSE 3000

# الخطوة 8: الأمر اللي بيشغّل التطبيق
CMD ["node", "app.js"]
