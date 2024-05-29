## Flask Application Design for Creating Slides from a Sheet

### HTML Files
- **create_slide.html**: This HTML file will serve as the main interface for the user to create a slide. It will have a form with inputs for the slide title, content, and any additional attributes required.

### Routes
- **@app.route('/create_slide', methods=['POST'])**: This route will handle the POST request from the create_slide.html form. It will receive the slide data, process it, and store it in a database or other persistent storage.
- **@app.route('/view_slides', methods=['GET'])**: This route will display a list of all the created slides. It will render an HTML file with a table or list showing the slide titles and content.
- **@app.route('/view_slide/<slide_id>', methods=['GET'])**: This route will allow the user to view a specific slide. It will receive the slide ID as a parameter and render an HTML file displaying the slide's details.
- **@app.route('/edit_slide/<slide_id>', methods=['GET', 'POST'])**: This route will enable the user to edit an existing slide. It will render an HTML file with a form pre-filled with the current slide data. When the form is submitted, the route will update the slide data in the database.