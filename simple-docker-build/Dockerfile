FROM nginx:stable-alpine
# support running as arbitrary user which belogs to the root group
RUN chmod g+rwx /var/cache/nginx /var/run /var/log/nginx 
EXPOSE 8080
# comment user directive as master process is run as user in OpenShift anyhow
RUN sed -i.bak 's/^user/#user/' /etc/nginx/nginx.conf
RUN sed -i.bak 's/^user/#user/' /etc/nginx/conf.d/default.conf
COPY --from=build build /usr/share/nginx/html
RUN echo "$nginx_config" > /etc/nginx/conf.d/default.conf
RUN cat  /etc/nginx/conf.d/default.conf
