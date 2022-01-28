<template>
  <div class="card">
    <div class="card__category" :class="`${color}`">
      CATEGORY {{ category }}
    </div>
    <div class="card__img">
      <slot></slot>
    </div>
    <div class="card__text">
      <span class="card__author" :class="`${color}`">{{ author }}</span>
      <h2 class="card__header">{{ header }}</h2>
      <span class="card__description">{{ text }}</span>
    </div>
    <button class="card__action" :class="`${color}`">Call to action</button>
  </div>
</template>

<script>
export default {
  name: "x-card",
  props: {
    color: {
      type: String,
      default: "blue",
    },

    category: {
      type: String,
      default: "",
    },

    author: {
      type: String,
      default: "Adam Sendler",
    },

    header: {
      type: String,
      default: "Solution for people like you",
    },

    text: {
      type: String,
      default:
        "How can we help your technology and services business develop a revenue engine based",
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.card {
  border: 1px solid #d3d8e4;
  position: relative;
  padding: 29px;

  &__category {
    position: absolute;
    background: $blue;
    color: white;
    top: 11px;
    left: -1px;
    padding: 6px 16px 8px;
    text-align: center;
    font-size: 13px;
    text-transform: uppercase;
    letter-spacing: 1.2px;
    line-height: 22px;
  }

  &__img {
    height: 170px;
  }

  &__text {
    margin-top: 20px;
    margin-bottom: 30px;
  }

  &__author {
    font-size: 13px;
    line-height: 20px;
    letter-spacing: 0.8px;
    color: $blue;
    margin-bottom: 6px;
  }

  &__header {
    font-size: 22px;
    line-height: 30px;
    letter-spacing: 1.2px;
    color: $blackText;
    font-weight: normal;
    margin-bottom: 16px;
  }

  &__description {
    font-size: 16px;
    line-height: 26px;
    letter-spacing: 0.8px;
    color: $blackText;
  }

  &__action {
    width: 160px;
    height: 40px;
    padding-top: 9px;
    padding-bottom: 11px;
    text-align: center;
    border: none;
    font-family: "Noto Sans";
    color: white;
    letter-spacing: 0.8px;
    line-height: 20px;
    font-size: 13px;
    background-color: $blue;

    &:hover {
      opacity: 0.6;
      cursor: pointer;
    }
  }
}

@media screen {
  @media (max-width: 1200px) {
    .card {
      &__header {
        font-size: 20px;
        line-height: 28px;
      }

      &__action {
        width: 150px;
      }
    }
  }

  @media (max-width: 992px) {
    .card {
      padding: 27px;

      &__img {
        height: 150px;
      }

      &__author {
        font-size: 12px;
        line-height: 18px;
      }

      &__header {
        font-size: 18px;
        line-height: 26px;
        letter-spacing: 1px;
      }

      &__description {
        font-size: 14px;
        line-height: 22px;
        letter-spacing: 0.6px;
      }

      &__action {
        font-size: 12px;
        line-height: 18px;
        letter-spacing: 0.8px;
        width: 140px;
        height: 36px;
      }
    }
  }

  @media (max-width: 768px) {
    .card {
      &__category {
        font-size: 12px;
        line-height: 20px;
        letter-spacing: 1px;
      }
    }
  }

  @media (max-width: 576px) {
    .card {
      padding: 15px;

      &__category {
        top: 0;
        font-size: 12px;
        line-height: 20px;
        letter-spacing: 1px;
      }

      &__img {
        height: 140px;
      }
    }
  }

  div.blue,
  button.blue {
    background-color: $blue;
  }

  span.blue {
    color: $blue;
  }

  div.dark,
  button.dark {
    background-color: $darkBlue;
  }

  span.dark {
    color: $darkBlue;
  }
}
</style>
