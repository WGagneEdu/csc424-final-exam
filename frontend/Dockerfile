FROM node:22-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install --no-fund --no-audit

#Build for prod
COPY . .
RUN npm run build

#Serve via nginx
FROM nginx:1.27-alpine
COPY --from=builder /app/dist /usr/share/nginx/html

#Expose to port 80
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
