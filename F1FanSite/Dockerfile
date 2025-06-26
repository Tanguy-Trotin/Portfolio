# ----------- FRONTEND (Angular) -----------
FROM node:20 AS frontend-builder
WORKDIR /app/frontend
COPY f1-fan-frontend/package*.json ./
RUN npm install
COPY f1-fan-frontend/ ./
RUN npm run build -- --output-path=dist

# ----------- BACKEND (NestJS) -----------
FROM node:20 AS backend-builder
WORKDIR /app/backend
COPY f1-fan-backend/package*.json ./
RUN npm install
COPY f1-fan-backend/ ./
RUN npm run build

# ----------- FINAL IMAGE -----------
FROM node:20 AS runner
WORKDIR /app

# Copy built frontend
COPY --from=frontend-builder /app/frontend/dist ./public

# Copy backend build and node_modules
COPY --from=backend-builder /app/backend/dist ./dist
COPY --from=backend-builder /app/backend/node_modules ./node_modules
COPY f1-fan-backend/package*.json ./

EXPOSE 3000
CMD ["node", "dist/main.js"] 