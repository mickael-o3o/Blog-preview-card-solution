<template>
  <main class="p-main">
    <article class="c-card">
      <header>
        <img
          src="/images/illustration-article.svg"
          alt="illustration of the article"
          class="c-card__illustration-article"
          width="336px"
          height="201px"
        />
      </header>

      <div class="c-card__content">
        <p class="c-card__category">Learning</p>
        <div class="c-card__publish-date">Published 21 Dec 2023</div>
        <h1 class="c-card__title">HTML & CSS foundations</h1>
        <p class="c-card__description">
          These languages are the backbone of every website, defining structure, content, and
          presentation.
        </p>
      </div>
      <footer class="c-card__footer">
        <img
          src="/images/image-avatar.webp"
          class="c-card__image-avatar"
          alt="author picture"
          width="64px"
          height="65px"
        />
        <h2 class="c-card__author-name">Greg Hooper</h2>
      </footer>
    </article>
  </main>
</template>

<style lang="scss">
.p-main {
  min-block-size: 100vh;
  inline-size: 100%;
  max-inline-size: var(--desktop-width);
  display: flex;
  justify-content: center;
  align-items: center;
  padding-inline: 1.5rem;
}

.c-card {
  inline-size: 100%;
  max-inline-size: var(--card-width-desktop);
  background-color: var(--color-white);
  border: 0.0625rem solid rgba($color: #000000, $alpha: 1);
  border-radius: 1.25rem;
  padding: var(--space-200);
  display: flex;
  flex-direction: column;
  gap: var(--space-200);
  box-shadow: 0.5rem 0.5rem 0 rgb(0, 0, 0);

  &__illustration-article {
    inline-size: 100%;
    block-size: auto;
    border-radius: calc(10 / var(--font-size-paragraph) * 1rem);
  }

  &__content {
    display: flex;
    flex-direction: column;
    gap: var(--space-150);
  }

  &__category {
    background-color: var(--color-yellow);
    inline-size: fit-content;
    padding: var(--space-50) var(--space-150);
    border-radius: calc(4 / var(--font-size-paragraph) * 1rem);
    font: {
      weight: var(--font-weight-bold);
      size: var(--text-preset-3);
    }
  }

  &__publish-date {
    font-size: var(--text-preset-3);
  }

  &__title {
    font: {
      size: var(--text-preset-1);
      weight: var(--font-weight-bold);
    }
    &:hover {
      color: var(--color-yellow);
    }
    cursor: pointer;
  }

  &__description {
    font-size: var(--text-preset-2);
    color: var(--color-gray-500);
  }

  &__footer {
    display: flex;
    align-items: center;
    gap: var(--space-150);
  }

  &__image-avatar {
    inline-size: 2rem;
    block-size: 2rem;
  }

  &__author-name {
    font-size: var(--text-preset-2);
  }
}
</style>
