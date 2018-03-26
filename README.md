# flask-validation
A decorator for request parameters validation in Flask.

## Installation

    pip install flask-validation


## Usage

Import the package

    from flaskvalidation import validate

Add the decorator after the Flask router decorator.
    
    @app.route('/api/login', methods=['POST'])
    @validate(form.username=(str, '3<len(x)<20'), form.passowrd=(str, 'x.match(r"\d{6,20}")'))
    def login():
       //...
       return
