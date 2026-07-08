from PIL import Image

try:
    image = Image.open("input.jpg")
    image = image.resize((512, 512))
    image.save("processed.png")
    print("Image is ready for AI 3D conversion.")
except FileNotFoundError:
    print("Error: input.jpg not found.")
except Exception as e:
    print("Error:", e)
