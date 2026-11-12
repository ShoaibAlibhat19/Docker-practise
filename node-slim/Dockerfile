
FROM node:22-slim

WORKDIR /app

# Copy only package.json first (for caching)
COPY package*.json ./

# Install dependencies (skip devDependencies)
RUN npm install --omit=dev

# Now copy the rest of the code
COPY . .

# Port documentation
EXPOSE 3000

# Start the app in exec form
CMD ["node", "server.js"]