# project.py

from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
    return render_template('home.html')

@app.route('/solar')
def solar():
    return 'Energi matahari dapat dihasilkan dengan menggunakan panel surya.'

@app.route('/wind')
def wind():
    return 'Energi angin dapat dihasilkan dengan menggunakan turbin angin.'

@app.route('/hydro')
def hydro():
    return 'Energi air dapat dihasilkan dengan menggunakan turbin air.'

if __name__ == '__main__':
    app.run(debug=True)
