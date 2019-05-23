#!/usr/bin/env python
# -*- coding: utf-8 -*-
from selenium import webdriver
import time
from pyvirtualdisplay import Display

with Display() as display:

	browser = webdriver.Firefox()
	browser.get('https://twitter.com/login')

	username = raw_input('Usuario: ')
	password = raw_input('Clave: ')
	mensaje = raw_input('Mensaje: ')

	usuario = browser.find_element_by_class_name("js-username-field")
	clave = browser.find_element_by_class_name("js-password-field")

	usuario.send_keys(username)
	browser.implicitly_wait(1)
	clave.send_keys(password)
	browser.implicitly_wait(1)

	browser.find_element_by_class_name("EdgeButtom--medium").click()

	time.sleep(5)

	tweetbox = browser.find_element_by_id("tweet-box-home-timeline")
	browser.execute_script("arguments[0].click();", tweetbox)

	tweetbox.send_keys(mensaje)
	browser.implicitly_wait(1)

	time.sleep(5)

	browser.find_element_by_class_name("tweet-action").click()

	print "Tu tweet ha sido enviado con éxito.!!"

respuesta = raw_input('Quieres ver tu tweet?: y/n ')

if respuesta == "y":
  browser = webdriver.Firefox()
  browser.get('https://twitter.com/login')
  usuario = browser.find_element_by_class_name("js-username-field")
  clave = browser.find_element_by_class_name("js-password-field")
  usuario.send_keys(username)
  browser.implicitly_wait(1)
  clave.send_keys(password)
  browser.implicitly_wait(1)
  browser.find_element_by_class_name("EdgeButtom--medium").click()
  browser.get("https://twitter.com/" + username)

elif respuesta == "n":
  print("Gracias.!!")
