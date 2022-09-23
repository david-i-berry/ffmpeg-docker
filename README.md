# Running docker
docker build -t ffmpeg .
docker run -it -v ${pwd}:/local ffmpeg

# Running ffmpeg
cd /local
ffmpeg -r 18 -i frames/frame_%04d.png -c:v libx264 -pix_fmt yuv420p anim.mp4

# Assumptions
Working directory contains ./frames and associated pngs. If not update {pwd} accordingly.