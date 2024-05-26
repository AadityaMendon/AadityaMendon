from PIL import Image, ImageDraw, ImageFont

# Create an image with white background
image_width, image_height = 800, 600
background_color = (255, 255, 255)
image = Image.new('RGB', (image_width, image_height), background_color)
draw = ImageDraw.Draw(image)

# Define the text properties
text = "NAME"
font_size = 36
font_color = (0, 0, 0)
font_path = "arial.ttf"  # Path to a font file

# Load the font
font = ImageFont.truetype(font_path, font_size)

# Calculate the position to place the text
text_x, text_y = 10, 10  # Top-left corner

# Draw the text on the image
draw.text((text_x, text_y), text, font=font, fill=font_color)

# Save the image
image_path = "/mnt/data/profile_name.png"
image.save(image_path)

image.show()


