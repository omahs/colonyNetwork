FROM node:14-bullseye
COPY ./packages ./packages
COPY ./package.json ./
COPY ./package-lock.json ./
COPY ./build ./build
RUN npm install
EXPOSE 3000
CMD node $NODE_ARGS packages/reputation-miner/bin/index.js --dbPath $REPUTATION_JSON_PATH --colonyNetworkAddress $COLONYNETWORK_ADDRESS --privateKey $PRIVATE_KEY --syncFrom $SYNC_FROM_BLOCK $ARGS
