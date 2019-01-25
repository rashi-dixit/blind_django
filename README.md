# blind_django
Web based Email Portal for the Blind 
It aims at providing a voice based email service to blind people enabling the blind users to control their gmail accounts only through voice commands and mouse clicks to perform functions like composing an email, sending attachments with it, reading, replying, forwarding, deleting mails and other operations.


The mysite/homepage/urls.py  contains the urls of all webpages.

The mysite/homepage/views.py   contains the functions to be executed when the urls are loaded.

The mysite/homepage/templates/homepage contains the html files of the webpages

The url of the 'Homepage'(first page) invokes the function 'login_view'

def login_view() : asks for email id and password from user in speech, and upon successfully logging in, loads the url of the next page (options page)

The url of the 'Options Page' invokes the function 'options_view'

def options_view() : provides 4 options to user, namely, Compose, Inbox, Sent Mails, Logout. The selected option loads the corresponding page.

The url of the 'Compose Page' invokes the function 'compose_view'

def compose_view() : for composing and sending an email ( multiple recipients, attachments, an option to record an audio and send as .mp3 file as attachment)

The url of the 'Inbox Page' invokes the function 'inbox_view'

def inbox_view() : read out to user the number of unread mails(with senders emailids), options for reading unread emails, all emails, mails from a specific person etc; audio attachments automatically downloaded and played; option of replying to every email, and forwarding it to others, and deleting it.

The url of the 'Sent Mails Page' invokes the function 'sent_view'

def sent_view() : reads mails in sent folder by first reading out email numbers with coresponding email ids of receivers, then asking the user which mails he/she wants to read as a whole.

The url of the 'Trash Page' invokes the function 'trash_view'

def trash_view() : reads mails in trash folder by first reading out email numbers with coresponding email ids of receivers/senders, then asking the user which mails he/she wants to read as a whole; option of restoring mails from Trash folder.


The above major functions call other functions from within themselves like:

def texttospeech(text):  google APIs used to convert text to speech

def speechtotext() : take input from user as speech and convert it into text

def read_mails():

def get_body():

def get_attachments():

def reply_mail():

def forward_mail()

def search_specific_mail():

def convert_special_chars():


 
