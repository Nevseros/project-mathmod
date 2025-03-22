---
# Leave the homepage title empty to use the site title
title: Колебания цепочек
date: 2025-03-22
type: landing

sections:
  - block: hero
    content:
      title: |
        Проект
        Колебания цепочек
      image:
        filename: welcome.jpg
      text: |
        <br>
        
        Этот сайт создан для освещения работы над проектом по изучению и моделированию колебания цепочек. Это применимо к цепочкам атомов в кристалле.
  
  - block: collection
    content:
      title: Последние новости
      subtitle:
      text:
      count: 5
      filters:
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: card
      columns: '1'

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./people/" cta_text="Познакомьтесь с нами →" %}}
    design:
      columns: '1'
      
---
