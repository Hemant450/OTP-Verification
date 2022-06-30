# OTP-Verification
import random
import smtplib

server= smtplib.SMTP('smtp.gmail.com',587)
server.starttls()
server.login('hemanty00011@gmail.com','adocvvxezyvhsevo')
otp=''.join([str(random.randint(0,9)) for i in range(4)])
MSG='Respected Sir/Mam, Your OTP is- '+str(otp)
server.sendmail('hemanty00011@gmail.com','gagandeep.e12617@cumail.in',MSG)
print('Your OTP has been generated')
server.quit()
