<template>
  <main id="main">
    <!-- ======= Blog Header ======= -->
    <div class="header-bg page-area">
      <div class="container position-relative">
        <div class="row">
          <div class="col-md-12 col-sm-12 col-xs-12">
            <div class="slider-content text-center">
              <div class="header-bottom">
                <div class="layer2">
                  <h1 class="title2">My Blog</h1>
                </div>
                <div class="layer3">
                  <h2 class="title3">Profesional Blog Page</h2>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End Blog Header -->

    <!-- ======= Blog Page ======= -->
    <div class="blog-page area-padding">
      <div class="container">
        <div class="row">
          <div class="col-lg-4 col-md-4">
            <div class="page-head-blog">
              <div class="single-blog-page">
                <!-- search option start -->
                <form action="#">
                  <div class="search-option">
                    <input type="text" placeholder="Search..." />
                    <button class="button" type="submit">
                      <i class="bi bi-search"></i>
                    </button>
                  </div>
                </form>
                <!-- search option end -->
              </div>
              <div class="single-blog-page">
                <!-- recent start -->
                <div class="left-blog">
                  <h4>recent post</h4>
                  <div class="recent-post">
                    <!-- start single post -->
                    <div class="recent-single-post">
                      <div class="post-img">
                        <a href="#">
                          <img src="@/assets/images/blog/1.jpg" alt="" />
                        </a>
                      </div>
                      <div class="pst-content">
                        <p><a href="#"> Redug Lerse dolor sit amet consect adipis elit.</a></p>
                      </div>
                    </div>
                    <!-- End single post -->
                    <!-- start single post -->
                    <div class="recent-single-post">
                      <div class="post-img">
                        <a href="#">
                          <img src="@/assets/images/blog/2.jpg" alt="" />
                        </a>
                      </div>
                      <div class="pst-content">
                        <p><a href="#"> Redug Lerse dolor sit amet consect adipis elit.</a></p>
                      </div>
                    </div>
                    <!-- End single post -->
                    <!-- start single post -->
                    <div class="recent-single-post">
                      <div class="post-img">
                        <a href="#">
                          <img src="@/assets/images/blog/3.jpg" alt="" />
                        </a>
                      </div>
                      <div class="pst-content">
                        <p><a href="#"> Redug Lerse dolor sit amet consect adipis elit.</a></p>
                      </div>
                    </div>
                    <!-- End single post -->
                    <!-- start single post -->
                    <div class="recent-single-post">
                      <div class="post-img">
                        <a href="#">
                          <img src="@/assets/images/blog/4.jpg" alt="" />
                        </a>
                      </div>
                      <div class="pst-content">
                        <p><a href="#"> Redug Lerse dolor sit amet consect adipis elit.</a></p>
                      </div>
                    </div>
                    <!-- End single post -->
                  </div>
                </div>
                <!-- recent end -->
              </div>
              <div class="single-blog-page">
                <div class="left-blog">
                  <h4>categories</h4>
                  <ul>
                    <li>
                      <a href="#">Portfolio</a>
                    </li>
                    <li>
                      <a href="#">Project</a>
                    </li>
                    <li>
                      <a href="#">Design</a>
                    </li>
                    <li>
                      <a href="#">wordpress</a>
                    </li>
                    <li>
                      <a href="#">Joomla</a>
                    </li>
                    <li>
                      <a href="#">Html</a>
                    </li>
                    <li>
                      <a href="#">Website</a>
                    </li>
                  </ul>
                </div>
              </div>
              <div class="single-blog-page">
                <div class="left-blog">
                  <h4>archive</h4>
                  <ul>
                    <li>
                      <a href="#">07 July 2016</a>
                    </li>
                    <li>
                      <a href="#">29 June 2016</a>
                    </li>
                    <li>
                      <a href="#">13 May 2016</a>
                    </li>
                    <li>
                      <a href="#">20 March 2016</a>
                    </li>
                    <li>
                      <a href="#">09 Fabruary 2016</a>
                    </li>
                  </ul>
                </div>
              </div>
              <div class="single-blog-page">
                <div class="left-tags blog-tags">
                  <div class="popular-tag left-side-tags left-blog">
                    <h4>popular tags</h4>
                    <ul>
                      <li>
                        <a href="#">Portfolio</a>
                      </li>
                      <li>
                        <a href="#">Project</a>
                      </li>
                      <li>
                        <a href="#">Design</a>
                      </li>
                      <li>
                        <a href="#">Website</a>
                      </li>
                      <li>
                        <a href="#">Joomla</a>
                      </li>
                      <li>
                        <a href="#">Html</a>
                      </li>
                      <li>
                        <a href="#">wordpress</a>
                      </li>
                      <li>
                        <a href="#">Masonry</a>
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <!-- End left sidebar -->
          <!-- Start single blog -->
          <div class="col-md-8 col-sm-8 col-xs-12">
            <div class="row" v-for="post in currentPosts" :key="post.id">
              <div class="col-md-12 col-sm-12 col-xs-12">
                <div class="single-blog">
                  <div class="single-blog-img">
                    <img
                      v-if="post.image.endsWith('.jpg')"
                      :src="`${post.image}`"
                      class="card-img-top"
                      alt="..."
                    />
                    <img v-else class="card-mg-top" src="@/assets/images/404.jpg" />
                  </div>
                  <div class="blog-meta">
                    <span class="date-type">
                      <i class="bi bi-calendar"></i>{{ post.createdAt.slice(0, 10) }} /
                      {{ post.createdAt.slice(11, 19) }}
                    </span>
                  </div>
                  <div class="blog-text">
                    <h4>
                      <a href="#">{{ post.title }}</a>
                    </h4>
                    <p>{{ post.preview }}</p>
                  </div>
                  <span>
                    <NuxtLink :to="`/post/${post.id}`" class="ready-btn">Read more</NuxtLink>
                  </span>
                </div>
              </div>
            </div>
            <div class="blog-pagination">
              <ul class="pagination">
                <li class="page-item">
                  <NuxtLink v-if="pageId > 1" :to="`/page/${+pageId - 1}`" class="page-link"
                    >&lt;</NuxtLink
                  >
                  <button v-else class="page-link disabled" disabled>&lt;</button>
                </li>
                <li class="page-item" v-show="pageId > 1">
                  <NuxtLink :to="`/page/${+pageId - 1}`" class="page-link">{{
                    +pageId - 1
                  }}</NuxtLink>
                </li>
                <li class="page-item active">
                  <a href="#" class="page-link">{{ pageId }}</a>
                </li>
                <li class="page-item" v-show="pageId < postLength">
                  <NuxtLink :to="`/page/${+pageId + 1}`" class="page-link">{{
                    +pageId + 1
                  }}</NuxtLink>
                </li>
                <li class="page-item">
                  <NuxtLink
                    v-if="pageId < postLength"
                    :to="`/page/${+pageId + 1}`"
                    class="page-link"
                    >&gt;</NuxtLink
                  >
                  <button v-else class="page-link disabled" disabled>&gt;</button>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End Blog Page -->
  </main>
</template>

<script setup>
const props = defineProps({
  pageId: Number,
});
const { data: posts } = await useFetch(
  "https://6082e3545dbd2c001757abf5.mockapi.io/qtim-test-work/posts/"
);
const postLength = Math.ceil(posts._rawValue.length / 4);
const currentPosts = posts._rawValue.slice(props.pageId * 4 - 4, props.pageId * 4);
if (props.pageId < 1 || props.pageId > postLength) {
  throw createError({ statusCode: 404, statusMessage: 'Post not Found' })
}
</script>
