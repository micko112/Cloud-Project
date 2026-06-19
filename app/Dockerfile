# Jednostavan Dockerfile - jedan stepen, sa keširanjem slojeva
FROM node:20-alpine

WORKDIR /app

# Prvo kopiramo samo package.json da Docker keširao "npm install" sloj
COPY package.json .
RUN npm install --omit=dev --no-audit

# Tek sad kopiramo ostatak kôda aplikacije
COPY . .

EXPOSE 3000

CMD ["npm", "start"]
