FROM debian:bullseye

RUN --mount=type=secret,id=sec_name echo "Sekretny tekst:" $(cat /run/secrets/sec_name) > /secret.txt