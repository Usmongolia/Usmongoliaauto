car1from pptx import Presentation

# PowerPoint файл үүсгэх
file_path = 'github_mobile_app_steps.pptx'
prs = Presentation()

# Title slide
slide = prs.slides.add_slide(prs.slide_layouts[0])
slide.shapes.title.text = "📱 GitHub мобайл апп ашиглах алхам алхмаар"
slide.placeholders[1].text = "Flowchart маягийн танилцуулга"

# Алхамууд
steps = [
    "1. Open App",
    "2. Sign In",
    "3. Repositories",
    "4. Edit File → Commit changes",
    "5. Add New File → Commit changes"
]

for i, step in enumerate(steps, start=1):
    slide = prs.slides.add_slide(prs.slide_layouts[1])
    slide.shapes.title.text = f"Алхам {i}"
    slide.placeholders[1].text = step

# Файлыг хадгалах
prs.save(file_path)
print(f"PowerPoint файл үүссэн: {file_path}")
