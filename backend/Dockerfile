 # Use the official Node.js image.
FROM node:20

# Set the working directory.
WORKDIR /app

# Copy package.json and pnpm-lock.yaml to the working directory.
COPY package.json pnpm-lock.yaml ./

# Install pnpm and dependencies.
RUN npm install -g pnpm && pnpm install

# Copy the rest of the application code.
COPY . .

# Build the application.
RUN pnpm build

# Expose the port the app runs on.
EXPOSE 3000

# Start the application.
CMD ["pnpm", "start"]