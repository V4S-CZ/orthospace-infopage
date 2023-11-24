# We'll base our dev container image on Alpine Linux.
FROM nginx

# Then we'll add the dependencies we need:
# - git and gnupg are useful for remote development so that we
#   can commit and sign commits from within the container
RUN apt update
RUN apt install -y git

# Finally, we'll remove nginx's default content and replace it
# with a symlink to our source code.

RUN rm -rf /var/www/html
RUN rm -rf /usr/share/nginx/html
RUN mkdir -p /var/www /usr/nginx/
RUN ln -s /workspaces/orthospace-infopage /var/www/html
RUN ln -s /workspaces/orthospace-infopage /usr/share/nginx/html

EXPOSE 80
