###
#
#   Version 1.2.0
#	Yves Vindevogel (vindevoy)
#	2021-02-17
#
#	Features: added dialog
#
###
 
FROM debian:10-slim

LABEL maintainer="Yves Vindevogel (vindevoy) - yves.vindevogel@asynchrone.com"

ARG TZ_REGION=Europe
ARG TZ_CITY=Brussels

RUN apt-get update -y
RUN apt-get upgrade -y

RUN apt-get install apt-utils --no-install-recommends -y
RUN apt-get install dialog --no-install-recommends -y

RUN apt-get autoremove
RUN apt-get clean all

RUN rm -f /etc/localtime
RUN ln -s /usr/share/zoneinfo/$TZ_REGION/$TZ_CITY /etc/localtime

CMD ["/bin/sh"]


###
#
#   Version history
#
#   Version 1.1.0
#	Yves Vindevogel (vindevoy)
#	2021-02-17
#
#	Features: added apt-utils
#
#   Version 1.0.0
#	Yves Vindevogel (vindevoy)
#	2019-10-25
#
#	Basic Debian 10 (slim version) image with possibility to change the timezone
#
###
