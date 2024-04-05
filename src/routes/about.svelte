<script>
  import Hero from "../components/Hero.svelte";
  import Card from "../components/Card.svelte";
  import Info from "../components/Info.svelte";
  import BulletPoints from "../components/BulletPoints.svelte";
  import { slide } from "svelte/transition";

  const heroText = "Perspective. Transparency. Perseverance.";
  const background = `background: url(/cheers.jpg) top 25% center no-repeat;`;
  const infoTextTop = `"Firm culture defines how you and your team relate to one another. It is also defined by how you treat your clients."`;

  const firstCardContent = {
    imgUrl: "/TylerNunnally.jpg",
    imgAlt: "Tyler D. Nunnally",
    text: ``,
    header: "",
    background: "background: #FEFCFB;",
    sideStyle: "align-self: start; display: block;",
  };
  const secondCardContent = {
    imgUrl: "/Prague.jpg",
    imgAlt: "Prague at sunset.",
    text: "My career path took some interesting twists and turns before I joined the wealth management industry and eventually moved into M&A. I did not start-out as an analyst at an investment bank or work for a Wall Street firm.",
    header: "OUR APPROACH",
    background: "background: #D6DDD9;",
    isFipped: true,
  };

  const bulletPointContent = {
    title: "",
    points: [
      {
        img: "/learn-more-global.svg",
        imgAlt: "the earth over the palm of a hand",
        header: "Perspective",
        text: [
          "Investment advisory is a people business. RIAs are relatively small, and you have to work closely with the people around you. Firm culture defines how you and your team relate to one another. It is also defined by how you treat your clients.",
          "Nunnally International puts a great deal of emphasis on compatible firm cultures because it is often the difference between a successful M&A partnership and one that fails.",
        ],
      },
      {
        img: "/learn-more-shield.svg",
        imgAlt: "a shield with a checkmark coat of arms",
        header: "Transparency",
        text: [
          "The payoff for M&A deals is very rewarding and so the incentives are strong for M&A advisors, as well as buyers and sellers. The desire to win can often bring-out the worst in people. Broken promises, half-truths and flat-out lies - whatever it takes.",
          "You have to choose your partners wisely which requires rigorous due diligence. We are firm believers in the Reagan era Cold War adage: Trust, but verify.",
        ],
      },
      {
        img: "/learn-more-heart.svg",
        imgAlt: "a heart lamp",
        header: "Perseverance",
        text: [
          "The M&A process can be long and tedious. It can be emotionally draining and takes internal fortitude, a strong will to succeed and the ability to adapt.",
          "We advise clients to be mentally prepared from the onset of talks and stick with the process despite the inevitable turmoil along the way. You have to persevere in order to achieve your objectives and never lose sight of the ultimate goal.",
        ],
      },
    ],
    background: "background: #D6DDD9;",
    width: "flex: 0 1 320px;",
  };
  const location = "about";
</script>

<svelte:head>
  <title>About | Nunnally International</title>
</svelte:head>

<Hero {heroText} {background} />
<Info infoText={infoTextTop} {location} />

<Card content={firstCardContent}>
  <div slot="side">
    <h3>Tyler D. Nunnally</h3>
    <p class="title">Founder & CEO</p>
    <p>
      Tyler founded Nunnally International, Inc. to focus exclusively on the RIA
      mergers and acquisitions market after serving as the Head of FinTech at
      M&A advisory EGL Holdings. Prior to entering M&A, Tyler served as a
      strategist to leading advisor technology companies – including investor
      risk profiling provider FinaMetrica, which was acquired by Morningstar. He
      began his wealth management career in England as an executive at Oxford
      Risk, a spin-off behavioral finance consultancy of Oxford University.
    </p>
    <p>
      Tyler has consulted hundreds of RIAs on mergers, acquisitions and matters
      of risk as a frequent speaker at industry conferences, host of countless
      webinars and key relationship manager to strategic partners at Schwab, TD
      Ameritrade, Fidelity, Redtail, Orion Advisor Services, MoneyGuidePro and
      Fi360. As an industry thought leader, he has been published widely and
      interviewed extensively by The Wall Street Journal, Bloomberg, CNBC, Smart
      Money, Kiplinger and InvestmentNews.
    </p>
    <p>
      He currently resides in his hometown Atlanta with his wife Eva. Tyler and
      Eva met during the 1992 Summer Olympics in Barcelona and have two sons.
      Max plays football at Tufts University and studies International
      Relations. Dylan is a Doctoral Fellow at the Centre for Research in
      Agricultural Genomics in Barcelona, Spain and graduated from University
      College Dublin in Ireland with a degree in biochemistry.
    </p>
  </div>
  <article slot="under">
    <p>
      Tyler began his career as a budding entrepreneur in Prague following the
      collapse of communism. He has lived in the Czech Republic, Scotland,
      England and Spain. He holds a B.A. from the University of Georgia and a
      Master’s in International Business with Distinction from the University of
      St Andrews in Scotland.
    </p>
    <a href="/Tyler Nunnally Professional Biography.pdf" nore target="_blank"
      >Professional Biography</a
    >
  </article>
</Card>
<div class="background-fill">
  <Card content={secondCardContent}>
    <div slot="side">
      <p>
        I began my career as a 24-year old entrepreneur in Prague, Czech
        Republic following the collapse of communism in Eastern Europe. I
        started an international trade business there in 1993 and worked in the
        country throughout the transition from communism to capitalism. To
        survive and thrive in that environment you had to navigate risks that
        went beyond the numbers. You had to understand the motivations and
        incentives that strike at the core human nature.
      </p>
    </div>
    <article slot="under">
      <p>
        I sold the business after a successful 10-year run and later joined an
        Oxford University spin-off consultancy where I worked alongside a
        prominent team of academics to bring the company’s investor risk
        profiling research to market. It proved to be an excellent training
        ground in the study of behavioral finance and the psychology of risk
        taking. The knowledge that I gained in Oxford was especially rewarding
        because it linked the behavioral sciences with aspects of human nature I
        witnessed in Prague.
      </p>
      <p>
        As Founder & CEO of Nunnally International, we apply these lessons in
        our approach to M&A. It explains the importance we attach to personal
        relationships and the emphasis we place on risk management.
      </p>
    </article>
  </Card>
</div>
<BulletPoints content={bulletPointContent}></BulletPoints>

<style>
  p {
    font-size: large;
    /* text-align: center; */
  }

  h3 {
    margin: 0 auto;
    text-align: center;
  }

  .title {
    margin: 0 0 10% 0;
    text-align: center;
  }

  a {
    display: block;
    cursor: pointer;
    font-size: large;
    padding: 1rem 2rem;
    margin-top: 1.5rem;
    background-color: #fdfdfd;
    border: #000000 solid 1px;
    color: #000000;
    text-decoration: none;
    border-radius: 5px;
    max-width: 200px;
    text-align: center;
  }

  a:hover {
    background-color: #2a2e45;
    color: #ffffff;
  }

  .background-fill {
    background-color: #d6ddd9;
  }

  article p {
    font-size: 18px;
    text-align: left;
  }
  @media (max-width: 430px) {
    a {
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>
