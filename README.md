# CS-360_InventoryApp

# Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?
InventoryApp allows a user to login and manage a list of items in a local SQLite database.  The application allows for multiple users to each manage their own list of items.  Users can add, edit, and delete items.  The application also requests for a user's permission to send and receive SMS messages. If granted, InventoryApp sends an SMS notification when an item's quantity reaches 0.

# What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?
InventoryApp consists of a login screen, a screen that displays a list of all items, a screen to edit item details, and a screen to adjust notification preferences.  One example of how InventoryApp keeps users in mind is the increment and decrement buttons included on the item list screen.  With these buttons a user can adjust the quantity of multiple items quickly without the need to navigate between screens.

# How did you approach the process of coding your app? What techniques or strategies did you use? How could those be applied in the future?
When developing InventoryApp I applied agile principles of frequent deliveries and functional code.  I broke the requirements up and only worked on the basic features and functionality first.  I then iteratively added functionality to the app.  In this way I was always able to submit functional code at the end of a work session which prevented the project from becoming overwhelming. This strategy becomes more and more important as the complexity of applications increases.

# How did you test to ensure your code was functional? Why is this process important and what did it reveal?
I tested the code manually usingthe emulator in Android Studio.  I tested it on multiple devices with different screen sizes to ensure the application would scale nicely.  I discovered many runtime errors during this testing as well as some issues that did not produce errors but affected the functionality of the application.  For example, I was originally handling notification preferences as a shared preference.  However, when I switched users in testing I realized that this tactic was causing all users to have the same notification preferences.  It seems obvious that shared preferences would be shared between users but it was not until testing that I caught this issue. I then moved notification preferences into the user table of the database.

# Considering the full app design and development process, from initial planning to finalization, where did you have to innovate to overcome a challenge?
My biggest challenge in the development of InventoryApp was to figure out how to display only the current user's data. I accomplished this by adding a user column to the item table in the database.  This allowed me to only display items that belonged to a particular user.

# In what specific component from your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?
I was particularly sucessful in my implementation of a RecyclerView to display all of the user's items.  As a user's item list grows large this will be much more efficient then a simple listView.  I was also able to successfully implement SMS notifications and adding images from the device to items.
