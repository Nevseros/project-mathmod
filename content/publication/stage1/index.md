---
title: 'Модель колебания цепочек атомов'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - yana
  - misha

# Author notes (optional)
author_notes:
  - 'Общий вклад'
  - 'Общий вклад'
  - 'Общий вклад'

date: '2025-03-22T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2025-03-05T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: Колебания цепочек

# Summary. An optional shortened abstract.
summary: Обозначили актуальности, цель и задачи. Описали модель.

tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_video: 'https://plvideo.ru/watch?v=UbNmImnvGdzX'
url_pdf: 'https://nevseros.github.io/publication/stage1/conference-paper.pdf'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---

# Введение

## Актуальность

Все вещества состоят из атомов, которые постоянно колеблются. Изучение этих колебаний помогает нам понять, как материалы ведут себя при разных температурах. Особенно важно понимать, как колебания приводят к тепловому равновесию. Исследование цепочек атомов, связанных пружинками, это простая модель, чтобы понять, как возникают колебания в кристаллах. Эта модель помогает объяснить, почему некоторые классические законы физики работают только при высоких температурах. Понимание колебаний важно для создания новых материалов с нужными свойствами, например, для электроники или термоизоляции.

## Объект и предмет исследования

1. Изучение условий для установления равновесия.
2. Изучение условий для приближения к равновесию.
3. Изучение явлений в простейшем одномерном случае.

## Цель работы

Исследовать закономерности колебаний в простейшей одномерной цепочке атомов, связанных между собой.

## Задачи

- построить модель цепочки из N частиц;
- задать начальные условия в виде гармоники и измерить собственную частоту. Сравнить результаты с теоретическими;
- проверить, используя преобразования Фурье координат и скоростей частиц, что энергия каждой гармоники не меняется;
- рассмотреть цепочку с чередующимися частицами.

# Модель

## Колебания цепочек

Все тела состоят из атомов. Представим движение атомов, связанных вместе пружинами. Эти колебания, называемые фононами, переносят энергию и импульс через материал, определяя его тепловые и оптические свойства. Колебания цепочек позволяют понять, как тепло распространяется в твёрдых телах, почему закон cV = 3R Дюлонга и Пти хорошо выполняется при не слишком низких температурах, пока влияние квантовых эффектов невелико. Модели колебаний цепочек варьируются от простых одномерных моделей до сложных трёхмерных расчётов, учитывающих взаимодействие между атомами и дефекты решётки.

## Гармоническая цепочка

Рассмотрим простейшую модель, используемую для описания колебаний атомов в твёрдом теле. Она состоит из $N$ идентичных точечных частиц, каждая массой $m$, расположенных вдоль прямой линии и соединённых между собой идеальными пружинками с одинаковой жёсткостью $k$. Крайние частицы прикреплены к неподвижным стенкам при помощи пружин. Таким образом, всего в системе $N+1$ пружин, каждая из которых имеет длину $d$.

## Уравнение движения

Если начально пружины не деформированы, то положение равновесия $i$-й частицы — это $x_i = id$. Вводятся малые смещения $y_i$ от положения равновесия. Тогда силы, действующие на $i$-ю частицу, записываются как:

$$
F_i = k(y_{i+1} - y_i) - k(y_i - y_{i-1}) = k(y_{i+1} - 2y_i + y_{i-1}).
$$

Соответственно, уравнение движения имеет вид:

$$
m \frac{d^2 y_i}{dt^2} = k(y_{i+1} - 2y_i + y_{i-1}), \quad i = 1, \dots, N.
$$

## Полная энергия системы

Полная энергия системы учитывает как кинетическую, так и потенциальную энергию:

$$
U = \frac{m}{2} \sum_{i=1}^{N} \left( \frac{d y_i}{dt} \right)^2 + \frac{k}{2} \sum_{i=1}^{N+1} (y_i - y_{i-1})^2.
$$

## Решение уравнения

Физически обоснованным решением является форма стоячей волны:

$$
y_i = \left( A \cos (p x_i) + B \sin (p x_i) \right) \cos (\omega t).
$$

Граничные условия \(y_0 = 0\) и \(y_{N+1} = 0\) приводят к ограничению на \(p\):

$$
\sin (p (N+1)d) = 0.
$$

Это выполняется при значениях:

$$
p_l = \frac{l \pi}{(N+1)d}, \quad l = 1, \dots, N.
$$

## Дисперсионное соотношение

Подставляя $p_l$ в уравнение движения, получаем:

$$
\omega_l = 2\omega_0 \sin \left( \frac{l \pi}{2(N+1)} \right), \quad l = 1, \dots, N,
$$

где $\omega_0 = \sqrt{k/m}$.

## Собственные моды

В системе существуют различные моды колебаний, соответствующие различным $p_l$. Эти моды не взаимодействуют между собой и называются гармониками. В музыке волна с волновым числом $p_1$ называется основным тоном, а остальные — обертонами.

{{% callout note %}}
Полный текст публикации можно найти по [этой](https://nevseros.github.io/publication/conference-paper/conference-paper.pdf) ссылке.
{{% /callout %}}

{{% callout note %}}
Защиту работы можно найти по [этой](https://plvideo.ru/watch?v=UbNmImnvGdzX) ссылке.
{{% /callout %}}
