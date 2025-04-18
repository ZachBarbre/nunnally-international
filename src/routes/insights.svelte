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
                superTitle: "In The News",
                title: "Press Release - ",
                boldDescription:
                    "Nunnally International serves as M&A Advisor in sale of Fiduciary Wealth Advisors to Waverly Advisors",
                description: "",
                downloadURI:
                    "/Waverly Advisors Acquires Fiduciary Wealth Advisors.pdf",
            },
            {
                superTitle: "In The News",
                title: "Press Release - ",
                boldDescription:
                    "Nunnally International serves as M&A Advisor in Poplar Forest Capital merger with Tocqueville Asset Management",
                description: "",
                downloadURI:
                    "/Tocqueville Asset Management Welcomes Poplar Forest Capital Team.pdf",
            },
            {
                superTitle: "RIA M&A Advice Series (Part I of II)",
                title: "BEHAVIORAL FINANCE IN M&A",
                description: "Beware of Biases That Cost Millions",
                downloadURI:
                    "/RIA M&A Advice Series - Beware of Biases That Cost Millions.pdf",
            },
            {
                superTitle: "RIA M&A Advice Series",
                title: "HOW MUCH IS YOUR RIA WORTH?",
                description: "HOW MUCH IS YOUR RIA WORTH?",
                downloadURI:
                    "/RIA M&A Advice Series - How Much Is Your RIA Worth.pdf",
            },
            {
                superTitle: "In The News",
                title: "PR Newswire - ",
                boldDescription:
                    "Nunnally International serves as M&A Advisor in acquisition of C2C Wealth Management",
                description: "",
                downloadURI:
                    "/Dakota-Wealth-Management-Acquires-C2C-Wealth.pdf",
            },
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
                downloadURI:
                    "/RIA M&A Advice Series - Firm Culture (Part 3 of 3).pdf",
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
                downloadURI:
                    "/RIA M&A Market Report - How Much is My RIA Worth.pdf",
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
                acquiredLogo: "/fiduciary-logo.png",
                acquiredAlt: "Fiduciary Wealth Advisors Logo",
                acquiredByLogo: "/waverly-logo.png",
                acquiredByAlt: "Waverly Advisors Logo",
                acquiredByTextOveride: "has been acquired by",
                acquiredText:
                    "Nunnally International served as M&A Advisor in the transaction",
            },
            {
                acquiredLogo: "/poplar-logo.png",
                acquiredAlt: "Poplar Forest Capital Logo",
                acquiredByLogo: "/tocqueville-logo.png",
                acquiredByAlt: "Tocqueville Logo",
                acquiredByTextOveride: "has merged with",
                acquiredText:
                    "Nunnally International served as M&A Advisor in the transaction",
            },
            {
                acquiredLogo: "/c2d-logo.png",
                acquiredAlt: "C2C Wealth Management LLC Logo",
                acquiredByLogo: "/dakota-logo.png",
                acquiredByAlt: "Dakota Wealth Management Logo",
                acquiredText:
                    "Nunnally International served as M&A Advisor in the transaction",
            },
            {
                acquiredLogo: "/loveless-logo.png",
                acquiredAlt: "Loveless Wealth Management LLC Logo",
                acquiredByLogo: "/dakota-logo.png",
                acquiredByAlt: "Dakota Wealth Management Logo",
                acquiredText:
                    "Nunnally International served as M&A Advisor in the transaction",
            },
            {
                acquiredLogo: "/pfa-logo.png",
                acquiredAlt: "Personal Financial Advisors Logo",
                acquiredByLogo: "/mercer-logo.png",
                acquiredByAlt: "Mercer Advisors Logo",
                acquiredText:
                    "Nunnally International served as M&A Advisor in the transaction",
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
