<script>
  import { fade } from 'svelte/transition'

  import Transition from '../components/Transition'
  import Typewriter from '../components/Typewriter'
</script>

<style>
  article {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    min-height: 100%;
    height: 900px;
    overflow: auto;
    background: var(--bg-color);
    z-index: 4;
    width: 100%;
  }

  article .o-content {
    max-width: 100%;
    width: 800px;
    margin: auto;
    padding: 2rem 0.5rem;
    margin-bottom: 10rem;
  }

  p {
    line-height: 2rem;
    margin-bottom: 2.5rem;
    font-size: 1.2rem;
    word-break: break-word;
  }

  hr {
    border: 1px dashed var(--primary-color);
    margin-bottom: 1.5rem;
  }

  h2 {
    color: var(--primary-color);
    font-family: var(--serif-font);
    font-size: 3rem;
    text-align: center;
    margin-bottom: 2rem;
  }

  h3 {
    color: var(--primary-color);
    font-family: var(--serif-font);
    font-size: 2.5rem;
    padding-top: 2rem;
    margin-bottom: 1rem;
  }

  h4 {
    font-size: 1.3rem;
    text-align: center;
  }

  sup {
    font-size: 14px;
    margin-left: -2px;
    color: var(--primary-color);
  }

  .o-cover {
    height: 100vh;
    background: linear-gradient(rgba(0, 0, 0, 0.9), rgba(0, 0, 0, 0.9)),
      url('/story.jpg');
    background-size: cover;
    background-attachment: fixed;
    background-position: center center;
    padding: 2rem;
  }

  .o-cover__container {
    display: table;
    height: 100vh;
    width: 100%;
  }

  .o-cover__content {
    display: table-cell;
    vertical-align: middle;
  }

  .o-footnotes p {
    font-size: 1rem;
    margin-bottom: 0;
    text-align: left;
  }

  @media screen and (min-width: 60em) {
    h2 {
      font-size: 4rem;
      line-height: 0;
      margin-bottom: 4rem;
    }

    p {
      font-size: 1.3rem;
    }

    h3 {
      font-size: 3rem;
    }

    article .o-content {
      text-align: justify;
      margin-bottom: 0;
    }
  }
</style>

<svelte:head>
  <title>evilfactorylabs.org - Cerita</title>
</svelte:head>

<article>
  <Transition>
    <div class="o-cover">
      <div class="o-cover__container">
        <div class="o-cover__content">
          <Typewriter cursor={false} interval={100}>
            <h2>Welcome to the 21st century</h2>
          </Typewriter>
          <h4 in:fade={{ delay: 3000, duration: 666 }}>
            Written by
            <a href="mailto:fariz@evilfactory.id">Fariz</a>
            — 14 Jan 2020, 13:37 WIB
          </h4>
        </div>
      </div>

      <div class="o-content" in:fade={{ duration: 666, delay: 3500 }}>
        <p>Welcome to this century, where software is eating the world.</p>

        <p>
          On 20 August 2011 Marc Andreessen wrote about
          <a
            href="https://a16z.com/2011/08/20/why-software-is-eating-the-world/">
            "Why Software Is Eating the world".
          </a>
          Long story short, there are significant increasement in major business
          and industries on being run on software and delivered as online
          services.
        </p>

        <p>
          Internet was came to Indonesia since 24 June 1988. The first IP
          Address from Indonesia was registered by UI-NETLAB for address range
          192.41.206/24 at that time
          <sup>1</sup>
          .
        </p>

        <p>
          In 1994, the first (commercial) ISP was born under IndoNet name lead
          by Sanjaya. At that time, internet users are relative small and can
          only be used to browse the internet via shell-based browser (Lynx) and
          email exchange
          <sup>2</sup>
          .
        </p>

        <p>
          Long story short, in 2017 internet penetration in Indonesia was about
          143,26 million users, it's 54,68% from total population of Indonesia
          at that time (262 million people). The biggest users are from Java &
          Bali island
          <sup>3</sup>
          .
        </p>

        <p>
          According to
          <a
            href="https://www.statista.com/statistics/254460/internet-penetration-rate-in-indonesia/">
            Statista,
          </a>
          internet user penetration in 2019 was about 40% from total population
          of Indonesia. This is a bright future since internet today was faster,
          cheaper, and more accessible than 2017.
        </p>

        <p>
          Software we are talking about here is the "online service". Or
          specifically the software that run on internet and accessible via
          internet browser: The Web Application.
        </p>

        <h3>The digital transformation</h3>

        <p>
          Software is eating both at Enterprise & Government in Indonesia. For
          example, in 2014, Direktorat Jenderal Pajak
          <a href="https://www.online-pajak.com/e-filing-pajakgoid">
            combining
          </a>
          all report & payment tax services under 1 system and lives on official
          Indonesia government internet domain (djponline.pajak.go.id). And
          until today, for example, Indonesia citizen can register NPWP via the
          official website, with no "offline action" required.
        </p>

        <p>
          As well as E-government implementation on several cities like DKI
          Jakarta, Bandung, and Pandeglang
          <sup>4</sup>
          .
        </p>

        <p>
          On Enterprise world itself, there are so many new technology companies
          (well known as startup company) born with their own mission.
        </p>

        <p>
          There are E-Commerce to empower Small-Medium Business (UKM) throughout
          Indonesia, Payment Processor to increase the GDP of Internet (in
          Indonesia), and other niche category to help "the digital
          transformation" easier & effective.
        </p>

        <p>
          Also don't forget about all the new buzzwords like Fintech,
          Blockchain, Digital Wallet, and AI that are gaining in popularity
          among us.
        </p>

        <h3>Are we ready yet?</h3>

        <p>
          There are 5
          <a href="https://en.wikipedia.org/wiki/Unicorn_(finance)">unicorn</a>
          startups in Indonesia: Go-Jek (On-demand multi-services), Tokopedia
          (E-commerce), Bukalapak (E-commerce), Traveloka (Online Ticket Agent),
          and OVO (Digital Wallet). It means there are a big hopes on this
          "digital transformation" era from (experienced) investor perspectives.
        </p>

        <p>
          According to
          <a
            href="https://katadata.co.id/berita/2019/01/10/transaksi-bukalapak-naik-tiga-kali-lipat-selama-2018">
            KataData
          </a>
          total gross merchandise value from Bukalapak in 2018 are tripled
          compared with 2017, although I don't have the exact number for that
          (there is an issue it's up to 4 tio/month).
        </p>

        <p>
          Tokopedia itself has 90+ million monthly active users. It means, we
          can say that majority of internet users in Indonesia is ready with
          this digital transformation in buying and selling goods category. And
          yes, Tokopedia has more users (assumed from their MAU) than Bukalapak.
          You got the point.
        </p>

        <h3>Seriously are we ready yet?</h3>

        <p>
          Since software is eating majority industries in Indonesia, we need to
          see from labour perspectives as well.
        </p>

        <p>Let's use E-commerce as an example.</p>

        <p>
          E-commerce was the throughput of digital transformation from
          traditional, physical market. In physical market, buyers are come to
          the "place" where the sellers are gather in the same place.
        </p>

        <p>
          Transactions are done directly, and basically with almost zero
          additional costs (like for shipment). Sellers doesn't need to pay
          anything for their activities (except for things related to thugs) on
          that place. Also, no maintenance cost. Usually it's done by the
          government.
        </p>

        <p>
          In E-commerce, there are so many costs. E-commerce is "owning" the
          "place" or well known as Marketplace, so they need to pay maintenance
          cost of that. Maintenance cost are including infrastructures,
          securities, legals, etc.
        </p>

        <p>Also, they need to pay the maintainers.</p>

        <p>
          Besides, they want to innovate more to make their marketplace better,
          more reliable, and safer. Yes, the R&D things. So people can continue
          to use their product/platform and doesn't move to competitiors or look
          back to the traditional ones.
        </p>

        <p>
          The question:
          <em>
            "Does labour market ready to fulfil the industries demand, for this
            century?"
          </em>
        </p>

        <h3>The vicious circle</h3>

        <p>
          Some people are looking for job and the company are looking for the
          candidates. This vicious circle was a classic™ problem on the job
          market. The problem is simple: Candidates are not fit enough with
          company needs, on their scale.
        </p>

        <p>
          As known as
          <a href="https://en.wikipedia.org/wiki/Structural_unemployment">
            Structural Unemployment.
          </a>
          Yes, the Skills Gap.
        </p>

        <p>
          Company can lower their expectation towards the candidates without
          reducing standard needs by investing more on training to the
          candidates. So they can pursue what company actually needs on company
          scale while they are helping the company at the time.
        </p>

        <h3>Our effort(s)</h3>

        <p>
          <a href="/">We are</a>
          group of people who have same interest for gathering in one "place".
          Yes, the community definition. We (not referring to us) are all
          basically learn & grow with the IT communities around the world. And
          our existence is our effort to "giving back" to the community.
        </p>

        <p>
          Our main focus is on
          <strike>solving</strike>
          bridging the skills gap towards the developers.
        </p>

        <p>
          As you might understand, our main audiences are
          newcomers/less-experienced developers who still getting started,
          including us (yes we are the audience itself).
        </p>

        <p>Our actions vary and depend on the level of experiences.</p>

        <p>
          Some are by sharing what they have learned (learning by
          <strike>teaching</strike>
          sharing), some are by building real world application, and some are
          building some toy project related with existing project (practical
          learning), etc.
        </p>

        <p>
          Everyone are welcome to come, yes, the truly everyone. Regardless with
          their level of experience, age, or even gender. We provide supportive
          (and fun) environment, help, and infrastructure.
        </p>

        <p>
          We don't have any goals yet, but we have
          <a href="/etos">Ethos</a>
          to make sure we don't get lost.
        </p>

        <p>
          We are just getting started, and the thousand step starts from the
          first step. Thank you for reading my story, now you can go back to the
          <a href="/tentang">About page</a>
          or to the
          <a href="/">Homepage.</a>
        </p>

        <p>High five!</p>

        <p>
          <em>
            — warm welcome from
            <a href="https://twitter.com/evilfactorylabs">evilfactorylabs.</a>
          </em>
        </p>

        <p>
          <em>
            Thanks to Adrin for reading drafts (and fixing grammar mistakes) of
            this.
          </em>
        </p>

        <hr />

        <div class="o-footnotes">
          <p>
            [1]:
            <a href="https://id.wikipedia.org/wiki/Sejarah_Internet_Indonesia">
              https://id.wikipedia.org/wiki/Sejarah_Internet_Indonesia
            </a>
          </p>
          <p>
            [2]:
            <a
              href="https://stei.itb.ac.id/id/blog/2017/06/19/sejak-kapan-masyarakat-indonesia-nikmati-internet/">
              https://stei.itb.ac.id/id/blog/2017/06/19/sejak-kapan-masyarakat-indonesia-nikmati-internet/
            </a>
          </p>
          <p>
            [3]:
            <a
              href="https://web.kominfo.go.id/sites/default/files/Laporan%20Survei%20APJII_2017_v1.3.pdf">
              https://web.kominfo.go.id/sites/default/files/Laporan%20Survei%20APJII_2017_v1.3.pdf
            </a>
          </p>
          <p>
            [4]:
            <a
              href="https://www.goodnewsfromindonesia.id/2018/01/23/penerapan-sistem-e-government-di-indonesia">
              https://www.goodnewsfromindonesia.id/2018/01/23/penerapan-sistem-e-government-di-indonesia
            </a>
          </p>
        </div>
      </div>
    </div>
  </Transition>
</article>
