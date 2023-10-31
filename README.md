def login():
    username = input("请输入用户名: ")
    password = input("请输入密码: ")

    if username == "admin" and password == "password":
        print("登录成功！")
    else:
        print("用户名或密码错误！")

def generate_captcha():
    import random
    captcha = ""
    for _ in range(6):
        captcha += str(random.randint(0, 9))
    return captcha
def verify_captcha():
    captcha = generate_captcha()
    print("验证码:", captcha)
    user_captcha = input("请输入验证码: ")
    
