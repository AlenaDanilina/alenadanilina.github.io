# alen.photography

Сайт-портфолио Alen Danilina. Статический React + Vite, хостится на GitHub Pages.

Перенесён с Manus AI: все фотографии лежат в репозитории (`public/photos/`),
внешних зависимостей от Manus (хранилище, OAuth, бэкенд) больше нет.

## Локальный запуск

```bash
npm install
npm run dev
```

## Деплой

Любой push в `main` автоматически собирает и публикует сайт
(`.github/workflows/deploy.yml`). Вручную ничего загружать не нужно.

## Как добавить или заменить фотографии

1. Положить файлы в `public/photos/`.
2. Прописать их в нужной секции:
   - портфолио — массив `IMAGES` в `src/components/PortfolioSection.tsx`
     (поля `src`, `alt`, `category`, `aspect`, `span`, `isPreview`);
   - первый экран — `src/components/HeroSection.tsx`;
   - «обо мне» — `src/components/AboutSection.tsx`;
   - цены — `src/components/PricingSection.tsx`;
   - галереи — `src/components/ClientGallerySection.tsx`.
3. `git push` — сайт обновится сам за пару минут.

## Тексты и цены

Двуязычные строки (EN/RU) лежат прямо в компонентах секций,
переключатель языка — `src/contexts/LanguageContext.tsx`.
