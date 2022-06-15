FROM  odoo:14.0

# change to the root user
USER root
RUN apt-get update && apt-get -y upgrade
RUN apt-get install git git-gui gitk -y


RUN apt-get install -y pkg-config libxml2-dev libldap2-dev libffi-dev libsasl2-dev libxslt1-dev libxmlsec1-dev libxmlsec1-openssl python3-pip python3-qrcode git
RUN apt-get install -y gcc
RUN apt-get install -y python3-dev
RUN pip3 install xmlsec
RUN pip3 install git+https://github.com/pysimplesoap/pysimplesoap.git@master

#RUN python3 -m pip install /mnt/extra-addons/odoo-argentina/requirements.txt

# Instalo las dependencias de odoo-argentina desde el archivo requirements

#RUN pip3 install git+https://github.com/pysimplesoap/pysimplesoap@a330d9c4af1b007fe1436f979ff0b9f66613136e
#RUN pip3 install git+https://github.com/ingadhoc/pyafipws@py3k


# Instalo las dependencias de odoo-argentina-ce desde el archivo requirements
#RUN cd mnt && cd extra-addons && cd odoo-argentina && pip3 install -r requirements.txt
#RUN pip3 install -r ~/mnt/extra-addons/odoo-argentina/requirements.txt
#RUN pip3 install -r mnt/extra-addons/odoo-argentina/requirements.txt
#RUN apt-get install python3-m2crypto

#RUN apt-get install -y libssl-dev
RUN pip3 install --upgrade pip
RUN pip3 install pyOpenSSL
#RUN apt-get install -y g++
#RUN apt-get install -y libpcre3 libpcre3-dev
#RUN pip3 install wheel
#RUN apt-get -y install swig

#RUN pip3 install M2Crypto
RUN pip3 install httplib2>=0.7
RUN pip3 install git+https://github.com/pysimplesoap/pysimplesoap@e1453f385cee119bf8cfb53c763ef212652359f5
RUN pip3 install  fpdf>=1.7.2
RUN pip3 install  dbf>=0.88.019
RUN pip3 install  Pillow>=2.0.0

RUN apt-get install -y swig libssl-dev
RUN apt-get install python3-dev 

RUN apt-get install -y python-httplib2 python-m2crypto

RUN git clone https://github.com/pyar/pyafipws.git -b py3k && cd pyafipws && pip3 install -r requirements.txt && cd .. && rm -rf pyafipws


RUN pip3 install  git+https://github.com/OCA/openupgradelib/@master

RUN pip3 install  git+https://github.com/ingadhoc/pyafipws@py3k
#RUN cd pyafipws && pip3 install -r requirements.txt && python setup.py install && mkdir cache && chmod -R 777 cache && cd ..

#RUN pip3 install git+https://github.com/filoquin/pyafipws.git@py3k




#RUN  apt-get remove libpq5 -y
#RUN  apt-get install libpq-dev -y


#website
RUN pip3 install html2text
RUN pip3 install suds-jurko
RUN pip3 install requests
# change to the odoo user
USER odoo
