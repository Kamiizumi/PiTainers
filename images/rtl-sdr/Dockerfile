FROM arm32v6/alpine
RUN apk add rtl-sdr --update-cache --repository http://dl-cdn.alpinelinux.org/alpine/edge/testing/ --allow-untrusted

# Install Python and heatmap.py so rtl_power output can be converted to heatmap images
RUN apk update
RUN apk add py-pip
RUN apk add py-pillow
RUN pip install image
ADD https://raw.githubusercontent.com/keenerd/rtl-sdr-misc/master/heatmap/heatmap.py /
ADD https://github.com/keenerd/rtl-sdr-misc/raw/master/heatmap/Vera.ttf /
RUN chmod +x /heatmap.py
