FROM tusproject/tusd:v1.8

ARG container_user=mosip
ARG container_user_group=mosip
ARG container_user_uid=1001
ARG container_user_gid=1001

WORKDIR /home/${container_user}

RUN chown -R ${container_user}:${container_user} /home/${container_user}

USER ${container_user_uid}:${container_user_gid}

ENTRYPOINT ["tusd", "-behind-proxy"]
CMD [ "--hooks-dir", "/srv/tusd-hooks" ]
