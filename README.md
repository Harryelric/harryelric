.sidebar {
  width: 260px;
  background-color: var(--color-auto-blue-9);
  position: sticky;
  top: 0;
  padding-bottom: $spacer-5;
  overflow-y: auto;
  height: 100vh;
  flex-shrink: 0;

  @include breakpoint(xl) {
    width: 280px;
  }
}

.sidebar-background-color {
  background-color: var(--color-auto-blue-9);
}

.sidebar-products > li {
  margin: 4px 0;
}

.sidebar-products a,
.sidebar-products .arrow {
  text-decoration: none;
  color: var(--color-auto-white);
  display: block;
  line-height: 1.4;

  &:hover {
    color: var(--color-auto-blue-3);
  }
}

.sidebar-category,
.sidebar-product {
  > a,
  summary a {
    color: var(--color-auto-blue-2);
    opacity: 0.8;
  }
}

.sidebar-product,
.sidebar-category,
.sidebar-maptopic,
.sidebar-article {
  &.is-current-page > a {
    color: var(--color-auto-blue-3);
  }
}

.sidebar-category.active {
  background-color: var(--color-auto-blue-8);
}

.sidebar-maptopic {
  .sidebar-article {
    position: relative;

    &::before {
      content: "";
      position: absolute;
      left: $spacer-4;
      height: 100%;
      border-left: 1px solid var(--color-auto-blue-7);
      width: 1px;
      top: 0;
    }

    &.active {
      &::before {
        border-left: 3px solid var(--color-auto-blue-7);
      }
    }
  }
}

// only display child lists of active elements in sidebar
.sidebar-product.active > ul,
.sidebar-category.active > ul,
.sidebar-maptopic.active > ul {
  display: block;
}

.sidebar-category {
  > ul {
    display: none;
  }
}

.sidebar-maptopic > ul {
  display: none;
}
