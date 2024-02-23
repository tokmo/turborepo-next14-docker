# Utilisez l'image node comme base
FROM node:20.11.1-alpine as base

RUN apk add --no-cache libc6-compat
RUN apk update

WORKDIR /app

EXPOSE 3000
EXPOSE 3001

RUN corepack enable
RUN yarn global add turbo

COPY . .

RUN pnpm i --frozen-lockfile

ARG PROJECT
ENV PROJECT=$PROJECT

RUN echo $PROJECT

CMD if [ -z "$PROJECT" ]; then \
      echo "No project specified. Starting default server."; \
      pnpm run dev; \
    else \
      pnpm run dev:"$PROJECT"; \
    fi

