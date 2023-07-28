FROM debian:latest

LABEL "maintainer"="Aiden Vigue <aiden@vigue.me>"
LABEL "repository"="https://github.com/acvigue/resume"
LABEL "homepage"="https://github.com/acvigue/resume"

LABEL "com.github.actions.name"="Convert to PDF"
LABEL "com.github.actions.description"="Convert documents to PDF using xelatex."
LABEL "com.github.actions.icon"="code"
LABEL "com.github.actions.color"="blue"

# Install all xelatex and LaTeX dependencies

RUN apt-get update && \
    apt-get install --yes --no-install-recommends \
    texlive-full \
    texlive-xetex && \

ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]