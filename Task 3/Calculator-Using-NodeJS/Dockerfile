# 1. Use an official Node image as the base
FROM node:18-alpine

# 2. Set the working directory inside the container
WORKDIR /app

# 3. Copy package.json & package-lock.json first (for caching)
COPY package*.json ./

# 4. Install dependencies
RUN npm install --production

# 5. Copy the rest of your app’s code
COPY . .

# 6. Expose the port your app uses
EXPOSE 3000

# 7. Command to run your app
CMD ["npm", "start"]
