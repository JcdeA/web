<script>
    import Footer from "../components/Footer.svelte";
    import Title from "../components/Title/Title.svelte";
    import Navbar from "../components/Navbar/Navbar.svelte";
    import Email from "../components/Email.svelte";

    let infrastructureSponsors = [
        {link: "https://fosshost.org/", name: "Fosshost", tagline: "The Fosshost project is a non-profit organisation that exists to serve the hosting needs of the global open source community."},
        {link: "https://heficed.com/", name: "Heficed", tagline: "Heficed provides full-range infrastructure services. Heficed serves around 60 multi-billion industries starting from hosting to automotive or healthcare. With more than a decade of industry experience and operations globally, Heficed can meet any demand needs."},
        {link: "https://terrahost.no/", name: "Terrahost", tagline: "Our vision is to offer solutions of high quality at an affordable price. Our services are delivered from our own datacenter in Sandefjord. In that way we can ensure high stability and safety. We work around the clock to give you the best price and service on the market."},
        {link: "https://hostus.us/", name: "HostUS", tagline: "We offer cPanel Web Hosting, Reseller Hosting, OpenVZ VPS, KVM VPS and Managed VPS in 10 datacenter locations across 4 continents. All backed by our amazing 24/7 support team."},
        {link: "https://mythic-beasts.com/", name: "Mythic Beasts", tagline: "Mythic Beasts is a privately owned hosting ISP with a focus on a no-nonsense service backed by excellent technical support."},
        {link: "https://combahton.net/", name: "Combahton", tagline: "We offer highly available dedicated servers, colocation, DDoS protection and managed services based on fail-safe and certified infrastructure in Germany. We are also your reliable partner for server and network management."},
        {link: "https://ifog.ch/", name: "iFog", tagline: "iFog GmbH offers IT services. This includes Web Hosting, vServers, IXP Access as well as IP Transit and LIR Services."},
        {link: "https://spartanhost.org/", name: "SpartanHost", tagline: "The main goal of the company has always been to provide the best possible service and product at a price that is good value for money. We will continue to strive to meet this goal in the future as we expand our services and locations."},
        {link: "https://garanntor.com", name: "Garanntor", tagline: "Garanntor is a privately owned company hosting and infrastructure-as-a-service company. Since our founding in 2016, Garanntor has continually innovated new ways to deliver on our mission: Making it Easy So You Can Focus on Growing Your Business. Based in Lagos, Nigeria. we pride ourselves in providing high quality services and support for each and every one of our clients."},
        {link: "https://xenspec.com/", name: "XenSpec", tagline: "Chicago based VPS and Web Hosting provider. Offering custom infrastructure solutions with exceptional support"},
        {link: "https://www.hivane.net", name: "Hivane", tagline: "Hivane offers DNS / MX / WWW services to non-for-profit projects. Check out https://www.hivane.net/ for more information."},
        {link: "https://misaka.io/", name: "Misaka Network", tagline: "Superb cloud infrastructure with low latency. All our services are carefully designed to provide high performance, reliable and scalable at a reasonably price."},
        {link: "https://www.virtua.cloud/", name: "Virtua Systems", tagline: "Virtua.Cloud is a cloud hosting company, providing affordable Linux VPS and Windows VPS in Europe with instant setup and hourly billing."},
        {link: "https://ginernet.com", name: "GINERNET", tagline: "Hosting powerful servers in Spain. Service stability, high availability network and priority technical support."}
    ]

    let serviceSponsors = [
        {link: "https://browserstack.com/", name: "BrowserStack", tagline: "BrowserStack is a cloud web and mobile testing platform that provides developers the ability to test their websites and mobile applications across on-demand browsers, operating systems, and real mobile devices. They have four primary products- Live, App Live, Automate, and App Automate"},
        {link: "https://saucelabs.com/", name: "Sauce Labs", tagline: "Continuous testing is a key enabler of digital confidence—the knowledge that you’re delivering the best possible user experience to your customers. Digitally confident organizations know that their web and mobile applications look, function and perform exactly as intended, every single time they’re used. That’s the value of Sauce Labs."},
    ]
</script>

<main>
    <Navbar homepage={true}/>

    <div class="centered">
        <Title>
            <div slot="header">Community</div>
        </Title>

        <div class="content">
            <p>Packetframe is fueled by the community. If you're interested in helping out or supporting the project in any way, contact <Email/>. The sponsors below have been instrumental in providing infrastructure or other services to the project - huge thanks to all of the amazing supporters!</p>

            <h2>Infrastructure Sponsors</h2>
            {#each infrastructureSponsors as sponsor}
            <h3><a href={sponsor.link}>{sponsor.name}</a></h3>
            <p>{sponsor.tagline}</p>
            {/each}

            <h2>Service Sponsors</h2>
            {#each serviceSponsors as sponsor}
            <h3><a href={sponsor.link}>{sponsor.name}</a></h3>
            <p>{sponsor.tagline}</p>
            {/each}
        </div>
    </div>

    <Footer/>
</main>

<style lang="scss">
  .centered {
    width: 100%;
    max-width: 800px;
    margin: 0 auto;
    color: white;
    display: flex;
    flex-direction: column;
  }

  .content {
    margin-left: 4px;
    margin-right: 4px;
  }
</style>
