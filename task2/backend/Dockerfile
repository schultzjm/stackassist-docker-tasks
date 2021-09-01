FROM node
COPY . /backend
WORKDIR /backend
RUN npm install
# Node creates user uid 1000, need a different uid (or to rename node to 1000)
RUN useradd -u 1001 -g 1000 rootless
USER rootless