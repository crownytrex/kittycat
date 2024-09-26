import tkinter as tk
from PIL import Image, ImageTk

class CatFollower:
    def __init__(self, master):
        self.master = master
        self.master.title("Cat Follower")
        
        # Load cat image
        self.cat_image = Image.open("cat.png")
        self.cat_photo = ImageTk.PhotoImage(self.cat_image)
        
        # Create a label to display the cat image
        self.cat_label = tk.Label(master, image=self.cat_photo, bd=0)
        self.cat_label.place(x=0, y=0)

        # Bind mouse movement
        self.master.bind('<Motion>', self.mouse_move)

    def mouse_move(self, event):
        # Update cat's position to follow the mouse
        x, y = event.x, event.y
        self.cat_label.place(x=x, y=y)

if __name__ == "__main__":
    root = tk.Tk()
    app = CatFollower(root)
    root.geometry("800x600")  # Set window size
    root.mainloop()
