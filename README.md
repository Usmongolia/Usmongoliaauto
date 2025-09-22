from pptx import Presentation


# PowerPoint файл үүсгэх
file_path = 'github_mobile_app_steps.pptx'
prs = Presentation()


# Слайдны хэв маяг
title_slide_layout = prs.slide_layouts[0]
content_slide_layout = prs.slide_layouts[1]


# Title slide
slide = prs.slides.add_slide(title_slide_layout)
title = slide.shapes.title
subtitle = slide.placeholders[1]


title.text = "📱 GitHub мобайл апп ашиглах алхам алхмаар"
subtitle.text = "Flowchart маягийн танилцуулга"


# Алхамууд
steps = [
"1. Open App",
"2. Sign In",
"3. Repositories",
"4. Edit File → Commit changes",
"5. Add New File → Commit changes"
]


for i, step in enumerate(steps, start=1):
slide = prs.slides.add_slide(content_slide_layout)
slide.shapes.title.text = f"Алхам {i}"
slide.placeholders[1].text = step


# Файлыг хадгалах
prs.save(file_path)
print(f"PowerPoint файл үүссэн: {file_path}") 1