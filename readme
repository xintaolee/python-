from flask import Flask, render_template, request, escape
app = Flask(__name__)

@app.route('/pick_a_color', methods=['POST'])
def pick_a_color() -> "html":
    user_color = request.form['user_color']
    print("user_color:", user_color)
    return render_template('results.html',
                           the_title = '以下是您选的颜色',
                           the_color = user_color,)

@app.route('/')
@app.route('/entry')
def entry_page() -> 'html':
    return render_template('entry.html',
                           the_title='欢迎来到网上选色')

if __name__ == '__main__':
    app.run(debug=True)
