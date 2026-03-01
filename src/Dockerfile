FROM archlinux AS builder

COPY bash-5.3.tar.gz /opt 
RUN cd /opt && tar xzf /opt/bash-5.3.tar.gz 

WORKDIR /opt/bash-5.3

RUN yes | pacman -Syu gcc mandoc make groff
RUN ./configure 
RUN make 
RUN mv bash /bin/bash

RUN head -1 /etc/passwd | sed 's;/usr/bin;;' >> /tmp/passwd


FROM scratch
COPY --from=builder /tmp/passwd /etc/passwd 
COPY --from=builder /bin/bash /bash 
CMD ["/bash"]

