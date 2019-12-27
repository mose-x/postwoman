<template>
  <div class="wrapper">
    <div class="content">
      <div class="columns">
        <aside class="nav-first">
          <nav class="primary-nav">
            <!--
              We're using manual checks for linkActive because the query string
              seems to mess up the nuxt-link active class.
            -->
            <nuxt-link
              :to="localePath('index')"
              :class="linkActive('/')"
              v-tooltip.right="$t('home')"
              aria-label="Home"
            >
              <logo alt class="material-icons" style="height: 24px;"></logo>
            </nuxt-link>
            <nuxt-link
              :to="localePath('realtime')"
              :class="linkActive('/realtime')"
              v-tooltip.right="$t('realtime')"
            >
              <i class="material-icons">settings_input_hdmi</i>
            </nuxt-link>
            <nuxt-link
              :to="localePath('graphql')"
              :class="linkActive('/graphql')"
              v-tooltip.right="$t('graphql')"
              aria-label="GraphQL"
            >
              <svg
                class="material-icons"
                version="1.1"
                xmlns="http://www.w3.org/2000/svg"
                x="0px"
                y="0px"
                viewBox="0 0 400 400"
              >
                <g>
                  <g>
                    <g>
                      <rect
                        x="122"
                        y="-0.4"
                        transform="matrix(-0.866 -0.5 0.5 -0.866 163.3196 363.3136)"
                        width="16.6"
                        height="320.3"
                      />
                    </g>
                  </g>
                  <g>
                    <g>
                      <rect x="39.8" y="272.2" width="320.3" height="16.6" />
                    </g>
                  </g>
                  <g>
                    <g>
                      <rect
                        x="37.9"
                        y="312.2"
                        transform="matrix(-0.866 -0.5 0.5 -0.866 83.0693 663.3409)"
                        width="185"
                        height="16.6"
                      />
                    </g>
                  </g>
                  <g>
                    <g>
                      <rect
                        x="177.1"
                        y="71.1"
                        transform="matrix(-0.866 -0.5 0.5 -0.866 463.3409 283.0693)"
                        width="185"
                        height="16.6"
                      />
                    </g>
                  </g>
                  <g>
                    <g>
                      <rect
                        x="122.1"
                        y="-13"
                        transform="matrix(-0.5 -0.866 0.866 -0.5 126.7903 232.1221)"
                        width="16.6"
                        height="185"
                      />
                    </g>
                  </g>
                  <g>
                    <g>
                      <rect
                        x="109.6"
                        y="151.6"
                        transform="matrix(-0.5 -0.866 0.866 -0.5 266.0828 473.3766)"
                        width="320.3"
                        height="16.6"
                      />
                    </g>
                  </g>
                  <g>
                    <g><rect x="52.5" y="107.5" width="16.6" height="185" /></g>
                  </g>
                  <g>
                    <g>
                      <rect x="330.9" y="107.5" width="16.6" height="185" />
                    </g>
                  </g>
                  <g>
                    <g>
                      <rect
                        x="262.4"
                        y="240.1"
                        transform="matrix(-0.5 -0.866 0.866 -0.5 126.7953 714.2875)"
                        width="14.5"
                        height="160.9"
                      />
                    </g>
                  </g>
                  <path
                    d="M369.5,297.9c-9.6,16.7-31,22.4-47.7,12.8c-16.7-9.6-22.4-31-12.8-47.7c9.6-16.7,31-22.4,47.7-12.8C373.5,259.9,379.2,281.2,369.5,297.9"
                  />
                  <path
                    d="M90.9,137c-9.6,16.7-31,22.4-47.7,12.8c-16.7-9.6-22.4-31-12.8-47.7c9.6-16.7,31-22.4,47.7-12.8C94.8,99,100.5,120.3,90.9,137"
                  />
                  <path
                    d="M30.5,297.9c-9.6-16.7-3.9-38,12.8-47.7c16.7-9.6,38-3.9,47.7,12.8c9.6,16.7,3.9,38-12.8,47.7C61.4,320.3,40.1,314.6,30.5,297.9"
                  />
                  <path
                    d="M309.1,137c-9.6-16.7-3.9-38,12.8-47.7c16.7-9.6,38-3.9,47.7,12.8c9.6,16.7,3.9,38-12.8,47.7C340.1,159.4,318.7,153.7,309.1,137"
                  />
                  <path
                    d="M200,395.8c-19.3,0-34.9-15.6-34.9-34.9c0-19.3,15.6-34.9,34.9-34.9c19.3,0,34.9,15.6,34.9,34.9C234.9,380.1,219.3,395.8,200,395.8"
                  />
                  <path
                    d="M200,74c-19.3,0-34.9-15.6-34.9-34.9c0-19.3,15.6-34.9,34.9-34.9c19.3,0,34.9,15.6,34.9,34.9C234.9,58.4,219.3,74,200,74"
                  />
                </g>
              </svg>
            </nuxt-link>
            <nuxt-link
              :to="localePath('doc')"
              :class="linkActive('/doc')"
              v-tooltip.right="'Documentation'"
              aria-label="Documentation"
            >
              <i class="material-icons">books</i>
            </nuxt-link>
            <nuxt-link
              :to="localePath('settings')"
              :class="linkActive('/settings')"
              v-tooltip.right="$t('settings')"
              aria-label="Settings"
            >
              <i class="material-icons">settings</i>
            </nuxt-link>
          </nav>
          <div v-if="$route.path === '/'">
            <nav class="secondary-nav">
              <ul>
                <li>
                  <a href="#request" v-tooltip.right="$t('request')">
                    <i class="material-icons">cloud_upload</i>
                  </a>
                </li>
                <li>
                  <a href="#options" v-tooltip.right="$t('options')">
                    <i class="material-icons">toc</i>
                  </a>
                </li>
                <li>
                  <a href="#response" v-tooltip.right="$t('response')">
                    <i class="material-icons">cloud_download</i>
                  </a>
                </li>
              </ul>
            </nav>
          </div>
          <div v-else-if="$route.path === '/realtime'">
            <nav class="secondary-nav">
              <ul>
                <li>
                  <a href="#request" v-tooltip.right="$t('request')">
                    <i class="material-icons">cloud_upload</i>
                  </a>
                </li>
                <li>
                  <a href="#response" v-tooltip.right="$t('communication')">
                    <i class="material-icons">cloud_download</i>
                  </a>
                </li>
              </ul>
            </nav>
          </div>
          <div v-else-if="$route.path === '/graphql'">
            <nav class="secondary-nav">
              <ul>
                <li>
                  <a href="#endpoint" v-tooltip.right="$t('endpoint')">
                    <i class="material-icons">cloud</i>
                  </a>
                </li>
                <li>
                  <a href="#schema" v-tooltip.right="$t('schema')">
                    <i class="material-icons">assignment_returned</i>
                  </a>
                </li>
                <li>
                  <a href="#query" v-tooltip.right="$t('query')">
                    <i class="material-icons">cloud_upload</i>
                  </a>
                </li>
                <li>
                  <a href="#response" v-tooltip.right="$t('response')">
                    <i class="material-icons">cloud_download</i>
                  </a>
                </li>
              </ul>
            </nav>
          </div>
          <div v-else-if="$route.path === '/doc'">
            <nav class="secondary-nav">
              <ul>
                <li>
                  <a href="#collections" v-tooltip.right="$t('collections')">
                    <i class="material-icons">folder</i>
                  </a>
                </li>
                <li>
                  <a href="#documentation" v-tooltip.right="'Documentation'">
                    <i class="material-icons">insert_drive_file</i>
                  </a>
                </li>
              </ul>
            </nav>
          </div>
          <div v-else-if="$route.path === '/settings'">
            <nav class="secondary-nav">
              <ul>
                <li>
                  <a href="#theme" v-tooltip.right="$t('theme')">
                    <i class="material-icons">brush</i>
                  </a>
                </li>
                <li>
                  <a href="#proxy" v-tooltip.right="$t('proxy')">
                    <i class="material-icons">public</i>
                  </a>
                </li>
              </ul>
            </nav>
          </div>

          <div class="flex-wrap">
            <span>
                <v-popover>
                  <button class="icon" v-tooltip="$t('choose_language')">
                    <i class="material-icons">translate</i>
                  </button>
                  <template slot="popover">
                    <div v-for="locale in availableLocales" :key="locale.code">
                      <nuxt-link :to="switchLocalePath(locale.code)">
                        <button class="icon" v-close-popover>
                          {{ locale.name }}
                        </button>
                      </nuxt-link>
                    </div>
                  </template>
                </v-popover>
              </span>
          </div>

        </aside>
        <div class="main" id="main">
          <nuxt />
        </div>
        <aside class="nav-second"></aside>
      </div>
    </div>
    <modal v-if="showShortcuts" @close="showShortcuts = false">
      <div slot="header">
        <ul>
          <li>
            <div class="flex-wrap">
              <h3 class="title">{{ $t("shortcuts") }}</h3>
              <div>
                <button class="icon" @click="showShortcuts = false">
                  <i class="material-icons">close</i>
                </button>
              </div>
            </div>
          </li>
        </ul>
      </div>
      <div slot="body">
        <br />
        <div>
          <label>{{ $t("send_request") }}</label>
          <kbd>⌘ G</kbd>
        </div>
        <br />
        <div>
          <label>{{ $t("save_to_collections") }}</label>
          <kbd>⌘ S</kbd>
        </div>
        <br />
        <div>
          <label>{{ $t("copy_request_link") }}</label>
          <kbd>⌘ K</kbd>
        </div>
        <br />
        <div>
          <label>{{ $t("reset_request") }}</label>
          <kbd>⌘ L</kbd>
        </div>
        <br />
      </div>
      <div slot="footer"></div>
    </modal>
    <modal v-if="showSupport" @close="showSupport = false">
      <div slot="header">
        <ul>
          <li>
            <div class="flex-wrap">
              <h3 class="title">{{ $t("support_us_on") }}</h3>
              <div>
                <button class="icon" @click="showSupport = false">
                  <i class="material-icons">close</i>
                </button>
              </div>
            </div>
          </li>
        </ul>
      </div>
      <div slot="body">
        <div>
          <a
            href="https://opencollective.com/postwoman"
            target="_blank"
            rel="noopener"
          >
            <button class="icon">
              <i class="material-icons">donut_large</i>
              <span>{{ $t("open_collective") }}</span>
            </button>
          </a>
        </div>
        <div>
          <a
            href="https://www.paypal.me/liyascthomas"
            target="_blank"
            rel="noopener"
          >
            <button class="icon">
              <i class="material-icons">payment</i>
              <span>{{ $t("paypal") }}</span>
            </button>
          </a>
        </div>
        <div>
          <a
            href="https://www.patreon.com/liyasthomas"
            target="_blank"
            rel="noopener"
          >
            <button class="icon">
              <i class="material-icons">local_parking</i>
              <span>{{ $t("patreon") }}</span>
            </button>
          </a>
        </div>
      </div>
      <div slot="footer"></div>
    </modal>
  </div>
</template>

<style scoped lang="scss"></style>

<script>
import intializePwa from "../assets/js/pwa";
import * as version from "../.postwoman/version.json";

export default {
  components: {
    logo: () => import("../components/logo"),
    modal: () => import("../components/modal")
  },

  methods: {
    linkActive(path) {
      return {
        "nuxt-link-exact-active": this.$route.path === path,
        "nuxt-link-active": this.$route.path === path
      };
    }
  },

  data() {
    return {
      // Once the PWA code is initialized, this holds a method
      // that can be called to show the user the installation
      // prompt.
      showInstallPrompt: null,
      version: {},
      showShortcuts: false,
      showSupport: false
    };
  },

  beforeMount() {
    // Set version data
    this.version = version.default;

    // Load theme settings
    (() => {
      // Apply theme from settings.
      document.documentElement.className =
        this.$store.state.postwoman.settings.THEME_CLASS || "";
      // Load theme color data from settings, or use default color.
      let color = this.$store.state.postwoman.settings.THEME_COLOR || "#50fa7b";
      let vibrant = this.$store.state.postwoman.settings.THEME_COLOR_VIBRANT;
      if (vibrant == null) vibrant = true;
      document.documentElement.style.setProperty("--ac-color", color);
      document.documentElement.style.setProperty(
        "--act-color",
        vibrant ? "rgba(32, 33, 36, 1)" : "rgba(255, 255, 255, 1)"
      );
    })();
  },

  mounted() {
    if (process.client) {
      document.body.classList.add("afterLoad");
    }

    document
      .querySelector("meta[name=theme-color]")
      .setAttribute(
        "content",
        this.$store.state.postwoman.settings.THEME_TAB_COLOR || "#202124"
      );

    // Initializes the PWA code - checks if the app is installed,
    // etc.
    (async () => {
      this.showInstallPrompt = await intializePwa();
      let cookiesAllowed = localStorage.getItem("cookiesAllowed") === "yes";
      if (!cookiesAllowed) {
        this.$toast.show("We use cookies", {
          icon: "info",
          duration: 5000,
          theme: "toasted-primary",
          action: [
            {
              text: "Dismiss",
              onClick: (e, toastObject) => {
                localStorage.setItem("cookiesAllowed", "yes");
                toastObject.goAway(0);
              }
            }
          ]
        });
      }
    })();

    window.addEventListener("scroll", event => {
      let mainNavLinks = document.querySelectorAll("nav ul li a");
      let fromTop = window.scrollY;
      mainNavLinks.forEach(link => {
        let section = document.querySelector(link.hash);

        if (
          section &&
          section.offsetTop <= fromTop &&
          section.offsetTop + section.offsetHeight > fromTop
        ) {
          link.classList.add("current");
        } else {
          link.classList.remove("current");
        }
      });
    });

    console.log("%cWe ❤︎ open source!", "background-color:white;padding:8px 16px;border-radius:8px;font-size:32px;color:red;")
    console.log("%cContribute: https://github.com/liyasthomas/postwoman", "background-color:black;padding:4px 8px;border-radius:8px;font-size:16px;color:white;")
  },

  watch: {
    $route() {
      this.$toast.clear();
    }
  },

  computed: {
    availableLocales() {
      return this.$i18n.locales.filter(i => i.code !== this.$i18n.locale);
    }
  }
};
</script>
