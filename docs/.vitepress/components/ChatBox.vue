<template>
  <div class="chat-box">
    <template v-for="message of props.messages" :key="message.username + message.content">
      <div v-if="!message.send" class="chat-message-left">
        <div class="chat-avatar">
          <img :src="getAvatar(message)" alt="头像" width="40" height="40"/>
        </div>
        <div class="chat-info-left">
          <span class="chat-title">
            <span class="name">{{ getUsername(message) }}</span>
          </span>
          <div class="bubble-left">
            <span v-if="message.html" v-html="message.content"/>
            <span v-else style="white-space: pre-wrap;">{{ message.content }}</span>
          </div>
        </div>
      </div>
      <div v-else class="chat-message-right">
        <div class="chat-info-right">
          <span class="chat-title">
            <span class="name">{{ getUsername(message) }}</span>
          </span>
          <div class="bubble-right">
            <span v-if="message.html" v-html="message.content"/>
            <span v-else style="white-space: pre-wrap;">{{ message.content }}</span>
          </div>
        </div>
        <div class="chat-avatar">
          <img :src="getAvatar(message)" alt="头像" width="40" height="40"/>
        </div>
      </div>
    </template>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { withBase } from 'vitepress'

interface ChatMessage {
  username: string,
  content: string,
  avatar?: 'dice' | 'user1' | 'user2' | 'user3',
  send: boolean,
  html: boolean,
}

const props = defineProps<{
  title?: string,
  messages?: ChatMessage[],
  noShadow?: boolean,
  lType?: 'info' | 'tip' | 'warning' | 'danger'
  rType?: 'info' | 'tip' | 'warning' | 'danger'
}>()

const getColorVar = (type) => {
  switch (type) {
    case 'tip':
      return 'var(--vp-c-tip-soft)'
    case 'warning':
      return 'var(--vp-c-warning-soft)'
    case 'danger':
      return 'var(--vp-c-danger-soft)'
    case 'info':
    default:
      return 'var(--vp-c-default-soft)'
  }
}

const getAvatar = (message: ChatMessage) => {
  if (message.avatar) {
    if (message.avatar === 'dice') {
      return withBase("/images/avatar/dice.svg")
    } else {
      return withBase(`/images/avatar/${message.avatar}.jpg`)
    }
  }
  if (message.send) {
    return withBase("/images/avatar/user1.jpg")
  } else {
    return withBase("/images/avatar/dice.svg")
  }
}

const getUsername = (message: ChatMessage) => {
  if (message.username && message.username !== '') {
    return message.username
  }
  if (message.send) {
    return '木落'
  } else {
    return '海豹核心'
  }
}

const leftColorVar = computed(() => {
  return getColorVar(props.rType ?? 'info')
})

const rightColorVar = computed(() => {
  return getColorVar(props.lType ?? 'tip')
})

const saturation = computed(() => {
  return props.noShadow ? 0.99 : 0.95
})
</script>

<style scoped lang="scss">
.chat-box {
  display: flex;
  flex-direction: column;
}

.chat-message-left, .chat-message-right {
  display: flex;
  margin: 0.5rem 0;
}

.chat-message-right {
  justify-content: right;
}

.chat-avatar {
  display: flex;
  justify-content: center;
  margin: 1px;
  border-radius: 0.25rem;

  img {
    width: 40px;
    height: 40px;
    border-radius: 0.25rem;
  }
}

.chat-info-left, .chat-info-right {
  width: 70%;
  display: flex;
  flex-direction: column;

  .chat-title {
    margin: 0 0.5rem;
  }
}

.chat-info-right {
  align-items: flex-end;
}

.bubble-left, .bubble-right {
  width: fit-content;
  max-width: 80%;
  margin: 0.1rem 0;
  padding: 0.5rem 1rem;
  filter: brightness(v-bind(saturation));
  position: relative;
  word-break: break-all;

  span {
    line-height: 1.5;
  }
}

.bubble-left::before, .bubble-right::after {
  position: absolute;
  content: '';
  width: 0;
  height: 0;
}

.bubble-left {
  background-color: v-bind(leftColorVar);
  border-radius: 0 0.5rem 0.5rem 0.5rem;
  margin-left: 0.5rem;

  &:before {
    top: 0;
    left: -1rem;
    border-top: 0;
    border-right: 0.5rem solid v-bind(leftColorVar);
    border-bottom: 1rem solid transparent;
    border-left: 0.5rem solid transparent;
  }
}

.bubble-right {
  background-color: v-bind(rightColorVar);
  border-radius: 0.5rem 0 0.5rem 0.5rem;
  margin-right: 0.5rem;

  &:after {
    top: 0;
    right: -1rem;
    border-top: 0;
    border-right: 0.5rem solid transparent;
    border-bottom: 1rem solid transparent;
    border-left: 0.5rem solid v-bind(rightColorVar);
  }
}
</style>

