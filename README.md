# pythonproject16
rom flask import Flask, render_template, url_for, request
app = Flask(__name__)
print(__name__)

@app.route('/')
def hello():
    return render_template('index.html')

@app.route('/<string:page_name>')
def html_function(page_name):
    return render_template(page_name)

@app.route('/submit_form', methods=['POST', 'GET'])
def submit_form():
    return render_template('/thankyou.html')

app.run(host='127.0.0.1', threaded=True)
