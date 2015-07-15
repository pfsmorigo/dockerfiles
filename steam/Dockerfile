FROM tianon/steamos

RUN echo 'deb [arch=amd64,i386] http://repo.steampowered.com/steam precise steam' > /etc/apt/sources.list.d/steam.list && \
	dpkg --add-architecture i386

RUN apt-get update
RUN apt-get install -yq \
	iproute \
	libc6:i386 \
	libgl1-mesa-dri:i386 \
	libgl1-mesa-glx:i386 \
	pulseaudio \
	steam-launcher \
	sudo

# steam itself needs to be able to install things, and it uses "sudo" for that
RUN echo 'steam ALL = NOPASSWD: ALL' > /etc/sudoers.d/steam && chmod 0440 /etc/sudoers.d/steam

RUN adduser --disabled-password --gecos 'Steam' --uid 3000 steam && \
	adduser steam video
USER steam
ENV HOME /home/steam
VOLUME /home/steam

CMD ["steam"]
