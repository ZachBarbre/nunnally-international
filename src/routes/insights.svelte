<script>
  import Hero from "../components/Hero.svelte";
  import Info from "../components/Info.svelte";
  import Reports from "../components/Reports.svelte";
  import Deals from "../components/Deals.svelte";

  const heroText = "Perspective. Transparency. Perseverance.";
  const background = `background: url(/high-five.jpg) top 25% center no-repeat;`;

  const reportsInfoText =
    "Market Intelligence: Access our latest market analysis and research on the RIA M&A market";
  const reports = {
    reports: [
      {
        superTitle: "RIA M&A Advice Series (Part II of II)",
        title: "EXTERNAL SUCCESSION",
        description: "The Stark Reality of Succession Planning",
        downloadURI:
          "/RIA M&A Advice Series - External Succession (Part II of II).pdf",
      },
      {
        superTitle: "RIA M&A Advice Series (Part I of II)",
        title: "INTERNAL SUCCESSION",
        description: "The Stark Reality of Succession Planning",
        downloadURI:
          "/RIA M&A Advice Series - Internal Succession (Part I of II).pdf",
      },
      {
        superTitle: "RIA M&A Advice Series (Part III of III)",
        title: "Firm culture",
        description:
          "3 factors that are key to your RIA M&A partnership success.",
        downloadURI: "/RIA M&A Advice Series - Firm Culture (Part 3 of 3).pdf",
      },
      {
        superTitle: "In The News",
        title: "CITYWIRE RIA -",
        boldDescription:
          "Nunnally International represented Loveless Wealth Management in sale to Dakota Wealth Management",
        description: "",
        downloadURI:
          "/CityWire-Nunnally-International-represented-Loveless-Wealth-Management-in-sale-to-Dakota-Wealth-Management.pdf",
      },
      {
        superTitle: "RIA M&A Advice Series (Part II of III)",
        title: "PARTNERSHIP CRITERIA",
        description:
          "3 factors that are key to your RIA M&A partnership success.",
        downloadURI:
          "/RIA M&A Advice Series - Partnership Criteria (Part II of III).pdf",
      },
      {
        superTitle: "RIA M&A Advice Series (Part I of III)",
        title: "STRATEGIC OBJECTIVES",
        description:
          "3 factors that are key to your RIA M&A partnership success.",
        downloadURI:
          "/RIA M&A Advice Series - Strategic Objectives (Part I of III).pdf",
      },
      {
        superTitle: "RIA M&A Market Report",
        title: "How Much is My RIA Worth?",
        boldDescription: "",
        description:
          "Evaluation of the impact of Covid-19 and subsequent market volatility on valuations.",
        downloadURI: "/RIA M&A Market Report - How Much is My RIA Worth.pdf",
      },
      {
        superTitle: "RIA M&A Market Report",
        title: "Is It the Right Time to Sell?",
        description:
          "Analysis of the 3 primary factors that are driving RIA M&A deals to record highs.",
        downloadURI:
          "/RIA M&A MARKET REPORT - Is it the Right Time to Sell.pdf",
      },
    ],
  };

  const dealsInfoText = "M&A Deals: Our most recently completed transactions";
  const deals = {
    deals: [
      {
        acquiredLogo: "/loveless-logo.png",
        acquiredAlt: "Loveless Wealth Management LLC Logo",
        acquiredByLogo: "/dakota-logo.png",
        acquiredByAlt: "Dakota Wealth Management Logo",
        acquiredText:
          "Nunnally International served as financial advisors to Loveless Wealth Management LLC",
      },
      {
        acquiredLogo: "/pfa-logo.png",
        acquiredAlt: "Personal Financial Advisors Logo",
        acquiredByLogo: "/mercer-logo.png",
        acquiredByAlt: "Mercer Advisors Logo",
        acquiredText:
          "Nunnally International served as a referral partner in the transaction",
      },
    ],
  };
</script>

<svelte:head>
  <title>Our Services | Nunnally International</title>
</svelte:head>

<Hero {heroText} {background} />

<Info infoText={reportsInfoText} />

<Reports {reports} />

<Info infoText={dealsInfoText} />

<Deals {deals} />
