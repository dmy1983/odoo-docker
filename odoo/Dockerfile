FROM  odoo:14.0

# change to the root user
USER root
RUN apt-get update && apt-get -y upgrade
RUN apt-get install git git-gui gitk -y
RUN apt-get install -y python3-dev
RUN apt-get install -y swig libssl-dev python-dev build-essential 




RUN apt-get install -y pkg-config libxml2-dev libldap2-dev zlib1g-dev libffi-dev libsasl2-dev libxslt1-dev libxmlsec1-dev libxmlsec1-openssl python3-pip python3-qrcode git
RUN apt-get install -y gcc

RUN apt-get install -y python-pypdf2 python-dateutil python-feedparser python-ldap python-libxslt1 python-lxml python-mako python-openid python-psycopg2 python-babel python-pychart python-pydot python-pyparsing python-reportlab python-simplejson python-tz python-vatnumber python-vobject
RUN apt-get install -y python-webdav python-werkzeug python-xlwt python-yaml python-zsi python-docutils python-psutil python-mock python-unittest2 python-jinja2 python-decorator python-requests python-passlib python-pil

RUN pip3 install --upgrade pip
RUN pip3 install PyPDF2 Werkzeug==0.11.15 python-dateutil reportlab psycopg2-binary

RUN pip3 install xmlsec
RUN pip3 install git+https://github.com/pysimplesoap/pysimplesoap.git@master



RUN pip3 install pyOpenSSL

RUN pip3 install httplib2>=0.7
RUN pip3 install git+https://github.com/pysimplesoap/pysimplesoap@e1453f385cee119bf8cfb53c763ef212652359f5
RUN pip3 install  fpdf>=1.7.2
RUN pip3 install  dbf>=0.88.019
RUN pip3 install  Pillow>=2.0.0


RUN apt-get install -y npm
RUN npm install -g less less-plugin-clean-css
RUN apt-get install -y node-less
# Descargo WHTMLTOPDF
RUN curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb \
        && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c - \
        && apt-get install -y --no-install-recommends ./wkhtmltox.deb \
        && rm -rf /var/lib/apt/lists/* wkhtmltox.deb

RUN git clone https://github.com/pyar/pyafipws.git -b py3k && cd pyafipws && pip3 install -r requirements.txt && cd .. && rm -rf pyafipws


RUN pip3 install  git+https://github.com/OCA/openupgradelib/@master

RUN pip3 install  git+https://github.com/ingadhoc/pyafipws@py3k

#website
RUN pip3 install html2text
RUN pip3 install suds-jurko
RUN pip3 install requests
# change to the odoo user
USER odoo
