<template>
  <footer class="footer">
    <div class="wrapper">
      <div class="main">
        <div class="logo">
          <a href="/">
            <img
              class="footer-logo"
              :src="$withBase('/logotype-white.svg')"
              alt="logo-icon-white"
            />
          </a>
        </div>
        <div class="navLinks">
          <div class="column">
            <h3>Developers</h3>
            <div class="link">
              <a href="https://explorer.erialos.me" target="_blank">
                Explorers
              </a>
            </div>
            <div class="link">
              <a href="/getting-started"> Documentation </a>
            </div>
            <div class="link">
              <a href="https://getbze.com/testnet-faucet" target="_blank">
                Faucet
              </a>
            </div>
          </div>
          <div class="column">
            <h3>Wallets</h3>
            <div class="link">
              <a
                href="https://play.google.com/store/apps/details?id=com.vidulumwallet.app"
                target="_blank"
              >
                Android
              </a>
            </div>
            <div class="link">
              <a
                href="https://apps.apple.com/us/app/id1505859171"
                target="_blank"
              >
                iOS
              </a>
            </div>
          </div>
        </div>
        <div class="socials">
          <a
            target="_blank"
            rel="noopener noreferrer"
            href="https://twitter.com/VidulumApp"
          >
            <img :src="$withBase('/social/twitter.svg')" alt="twitter" />
          </a>
          <a
            target="_blank"
            rel="noopener noreferrer"
            href="https://www.youtube.com/channel/UCNd92ZViZweu6zz5ydt_wrQ"
          >
            <img :src="$withBase('/social/youtube.svg')" alt="youtube" />
          </a>
          <a
            target="_blank"
            rel="noopener noreferrer"
            href="https://www.reddit.com/r/VidulumOfficial/"
          >
            <img :src="$withBase('/social/reddit.svg')" alt="reddit" />
          </a>
          <a
            target="_blank"
            rel="noopener noreferrer"
            href="https://discord.gg/hne7Ccq"
          >
            <img :src="$withBase('/social/discord.svg')" alt="discord" />
          </a>
        </div>
      </div>
      <p class="copyright">
        Copyright © {{ currentYear }} Beezee. All rights reserved.
      </p>
    </div>
  </footer>
</template>

<script>
export default {
  components: {},

  data() {
    return {
      linksWrapMaxWidth: null,
    };
  },

  computed: {
    currentYear() {
      return new Date().getFullYear();
    },
  },
};
</script>

<style lang="stylus">
@require '../styles/config'
$light-color = rgba(255, 255, 255, 50%)
.footer {
  min-height: $footerHeight;
  // width: 100%;
  padding: 28px 15px;
  background-color: #0b1426;

  .wrapper {
    max-width $MQWide
    margin 0 auto
  }

  .main {
    display flex
    justify-content space-between
    margin-bottom 3rem
    .navLinks {
      display flex
      .column {
        margin 0 2.5rem
        h3 {
          margin: 0;
          margin-bottom: 16px;
          font-size 16px;
          color: white;
          font-weight: 600;
        }
        .link {
          margin-bottom: 12px;
          font-size 14px;
          a {
            color: $light-color;
            font-weight: 500;
          }
          a:hover {
            color: white;
          }
        }
      }
    }

    .socials {
      max-width: 420px;
      margin-bottom: 32px;
      text-align: left;
      & > a {
        display: inline-block;
        margin: 0 20px 16px;
        font-size: 16px;
        opacity: 0.6;
      }
    }
  }

  .copyright {
    width: inherit;
    margin: 0;
    color: $light-color;
    font-weight: 600;
    font-size: 12px;
  }
}
@media (max-width: $MQMobile) {
  .footer {
    .main {
      flex-direction column
      margin-bottom 2rem

      .navLinks {
        flex-direction column
      }

      .navLinks {
        margin 2rem 1rem
        .column {
          margin 0
        }
      }

      .socials {
        margin-bottom 0
      }
    }
  }
}
</style>
