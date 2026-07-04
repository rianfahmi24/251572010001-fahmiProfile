# Menggunakan nginx versi alpine yang ringan sebagai base image
FROM nginx:alpine

# Mendefinisikan ARG yang akan menerima nilai dari docker-compose.yml
ARG NAMA
ARG NIM
ARG PRODI
ARG KAMPUS
ARG MINAT
ARG ALASAN
ARG CITA

# Menyalin folder html (berisi index.html & style.css) ke direktori default Nginx
COPY html/ /usr/share/nginx/html/

# Menggunakan perintah 'sed' untuk me-replace (mengganti) teks PLACEHOLDER dengan variabel ARG saat proses build
RUN sed -i "s/NAMA_PLACEHOLDER/${NAMA}/g" /usr/share/nginx/html/index.html && \
    sed -i "s/NIM_PLACEHOLDER/${NIM}/g" /usr/share/nginx/html/index.html && \
    sed -i "s/PRODI_PLACEHOLDER/${PRODI}/g" /usr/share/nginx/html/index.html && \
    sed -i "s/KAMPUS_PLACEHOLDER/${KAMPUS}/g" /usr/share/nginx/html/index.html && \
    sed -i "s/MINAT_PLACEHOLDER/${MINAT}/g" /usr/share/nginx/html/index.html && \
    sed -i "s/ALASAN_PLACEHOLDER/${ALASAN}/g" /usr/share/nginx/html/index.html && \
    sed -i "s/CITA_PLACEHOLDER/${CITA}/g" /usr/share/nginx/html/index.html
