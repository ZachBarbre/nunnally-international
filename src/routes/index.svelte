<script>
    import Card from "../components/Card.svelte";
    import Hero from "../components/Hero.svelte";
    import Info from "../components/Info.svelte";
    import BulletPoints from "../components/BulletPoints.svelte";
    import Testimonials from "../components/Testimonials.svelte";

    const heroText = "Perspective. Transparency. Perseverance.";
    const background = `background: url(/thumbs-up.jpg) top 46% center no-repeat;`;
    const infoText =
        "Nunnally International provides strategic M&A services to RIA firms that are looking to buy, sell or merge their business.";

    const firstCardContent = {
        imgUrl: "/financial-advice.jpg",
        imgAlt: "A man and woman receiving financial advice.",
        text: "We've spent years in the investment management industry in multiple capacities and understand the risks, opportunities and challenges that advisors face on a daily basis. We understand that every RIA is uniquely different and we tailor our  M&A guidance to your specific goals and circumstances.",
        background: "background: #D6DDD9;",
        header: "MARKET KNOWLEDGE",
        isFipped: true,
    };

    const secondCardContent = {
        imgUrl: "/buisness-handshake.jpg",
        imgAlt: "Two men shaking hands with a third standing behind.",
        text: "We act in your best interest by adhering to the same fiduciary principles and standard of care that you do. Our incentives are always aligned with yours and we're only compensated if your M&A deal successfully closes.",
        header: "UNCONFLICTED ADVICE",
        background: "background: #fefcfb;",
        // isFipped: true
    };

    const bulletPointContent = {
        title: "How We're Different",
        points: [
            {
                img: "/bullet-1-target.svg",
                imgAlt: "An arrow hitting a bullseye",
                header: "Strategic Objectives",
                text: [
                    "What are your goals and how can M&A help you achieve them? Is your intent to grow, diversify, adapt or create a succession plan?",
                ],
            },
            {
                img: "/bullet-2-handshake.svg",
                imgAlt: "Handshake",
                header: "Partnership Criteria",
                text: [
                    "Who can help you achieve your objectives? What characteristics define an ideal strategic partner? What's that's profile look like?",
                ],
            },
            {
                img: "/bullet-3-puzzle.svg",
                imgAlt: "Interlocking puzzle pieces",
                header: "Firm Culture",
                text: [
                    "Do you share the same worldview, investment philosophy and ambitions? What synergies exists professionally and personally between firm principles?",
                ],
            },
        ],
        background: "background: #D6DDD9;",
        width: "",
    };

    const testimonialContent = {
        title: "What our clients say",
        testimonials: [
            {
                text: `It has been a real pleasure working with Nunnally International. Tyler Nunnally is a true professional. He moved the M&A process forward at a good pace, and he helped me identify the perfect fit for my practice and my clients. I would highly recommend Nunnally International to any RIA who is interested in M&A.  `,
                name: "Scott Collins",
                title1: "President",
                title2: "Fiduciary Wealth Advisors",
            },
            {
                text: `It was a pleasure working with Tyler and Nunnally International. Tyler's ability to identify high caliber firms that fit our culture and goals is a rare and prized skill. We look forward to a continuously fruitful relationship with Nunnally international.`,
                name: "Paul Kleinschmidt",
                title1: "President & CEO ",
                title2: "Tocqueville Asset Management",
            },
            {
                text: `We could not be happier with Nunnally International's representation of Loveless Wealth Management in our M&A transaction. Their attention to detail and organization were second to none. Tyler introduced us to just the right firm and negotiated a great deal on our behalf.`,
                name: "Don Loveless",
                title1: "Founder and CEO",
                title2: "Loveless Wealth Management",
            },
            {
                text: `After searching and speaking with a number of firms for a couple years I was about to hit pause. Tyler came along and was able to very accurately identify the type of firm that would fit my needs. He knew the landscape, the deals, and how to narrow down possible partners. It was refreshing to have someone of his experience filter through and eventually identify my partner firm.`,
                name: "Lou Della Valle",
                title1: "Principal",
                title2: "C2C Wealth Management",
            },
            {
                text: `Tyler's personal interaction with each of our team members helped solidify what we were all looking for with a potential merger.  His ability to formalize the process of meeting with potential suitors was extremely valuable.  Most importantly, he helped our team stay on the same page as a cohesive unit with a tangible goal in sight.`,
                name: "Brian Suskevitch",
                title1: "Director, Senior Wealth Advisor",
                title2: "Partner and Shareholder",
            },
            {
                text: `I could not imagine navigating the M&A process on our own without Nunnally International. There is an overwhelming amount of detail and care needed throughout the entire process that was foreign to us, and Tyler was able to offer insight and guidance in our quest to find the best possible partner. He took the time to get to know us and we could not be happier with the final result.`,
                name: "Betsy Rector",
                title1: "Director, Senior Wealth Advisor",
                title2: "Partner and Shareholder",
            },
            {
                text: `Always a pleasure working with Tyler and Nunnally International.  Thank you!  Appreciate your ability to identify high caliber firms, clearly articulate needs and priorities for both parties, and helpfully contribute to making the transaction happen.`,
                name: "Bryan Keller",
                title1: "Chief Strategic Officer",
                title2: "Dakota Wealth Management",
            },
        ],
    };
</script>

<svelte:head>
    <title>Nunnally International</title>
</svelte:head>

<Hero {heroText} {background} />

<Info {infoText} />

<Card content={firstCardContent} />

<Card content={secondCardContent} />

<BulletPoints content={bulletPointContent}>
    <p>
        Nunnally International employs investor profiling expertise to help you
        find the best fit. We get to know you and your firm personally in order
        to gain a clear understanding of the factors that are key to your
        strategic partnership success.
    </p>
</BulletPoints>

<Testimonials content={testimonialContent} />

<style>
    p {
        width: 75%;
        text-align: center;
        font-size: 1.2rem;
        max-width: 1200px;
        margin-bottom: 5%;
    }
</style>
