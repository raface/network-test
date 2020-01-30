FROM alpine:latest
RUN apk update
RUN apk upgrade

# Add ooniprobe and cronjobs
RUN wget https://github.com/ooni/probe-cli/releases/download/v3.0.0-rc.7/ooniprobe_v3.0.0-rc.7_linux_amd64.tar.gz -O temp.zip; tar xvzf temp.zip -C /usr/bin/; rm temp.zip
#ADD cronjob.sh /
#ADD entrypoint.sh /
#ADD sample_cron.txt /
#ADD sample_xteve.txt /

# Set executable permissions
#RUN chmod +x /entrypoint.sh
#RUN chmod +x /cronjob.sh
#RUN chmod +x /usr/bin/xteve
#RUN chmod +x /usr/bin/ooniprobe

#Check installation
RUN which ooniprobe

# Add user
RUN adduser -S appuser -G adm --uid 1000
USER appuser
CMD "ooniprobe help"

# Entrypoint
#ENTRYPOINT ["./entrypoint.sh"]
