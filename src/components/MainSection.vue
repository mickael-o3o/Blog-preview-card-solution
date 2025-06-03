<template>
  <main class="card-container">
    <div class="card">
      <img
        src="/images/illustration-article.svg"
        alt="illustration-article"
        class="illustration-article"
      />
      <div class="content">
        <div class="category">Learning</div>
        <date class="publish-date"> Published 21 Dec 2023</date>
        <h1 class="title">HTML & CSS foundations</h1>
        <p class="description">
          These languages are the backbone of every website, defining structure, content, and
          presentation.
        </p>
      </div>
      <div class="author">
        <img src="/images/image-avatar.webp" class="image-avatar" alt="author picture" />
        <h2 class="author-name">Greg Hooper</h2>
      </div>
    </div>
  </main>
</template>

<style lang="scss">
.card-container {
  min-height: 100vh;
  width: 100%;
  max-width: var(--mobile-width);
  margin: 0 auto;
  background-color: var(--color-yellow);
  display: flex;
  justify-content: center;
  align-items: center;
}

.card {
  width: 100%;
  max-width: var(--card-width-mobile);
  background-color: var(--color-white);
  border: 1px solid rgba($color: #000000, $alpha: 1);
  border-radius: calc(20 / var(--font-size-paragraph) * 1rem);
  padding: var(--space-200);
  display: flex;
  flex-direction: column;
  gap: var(--space-200);
  box-shadow: 0.5rem 0.5rem 0 rgb(0, 0, 0);

  .illustration-article {
    max-width: calc(var(--card-width) - (var(--space-200) * 2));
    border-radius: calc(10 / var(--font-size-paragraph) * 1rem);
  }

  .content {
    display: flex;
    flex-direction: column;
    gap: var(--space-150);
  }

  .author {
    display: flex;
    align-items: center;
    gap: var(--space-150);
  }
}

.content {
  .category {
    background-color: var(--color-yellow);
    width: fit-content;
    padding: var(--space-50) var(--space-150);
    border-radius: calc(4 / var(--font-size-paragraph) * 1rem);
    font: {
      weight: var(--font-weight-bold);
      size: var(--text-preset-3);
    }
  }

  .publish-date {
    font-size: var(--text-preset-3);
  }

  .title {
    font: {
      size: var(--text-preset-1);
      weight: var(--font-weight-bold);
    }
    &:hover {
      color: var(--color-yellow);
    }
    cursor: pointer;
  }

  .description {
    font-size: var(--text-preset-2);
    color: var(--color-gray-500);
  }
}

.author {
  .image-avatar {
    width: 2rem;
    height: 2rem;
  }

  .author-name {
    font-size: var(--text-preset-2);
  }
}

@media (min-width: 375px) {
  .card-container {
    max-width: var(--desktop-width);

    .card {
      max-width: var(--card-width-desktop);
    }
  }
}
</style>
