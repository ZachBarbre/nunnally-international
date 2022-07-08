<script>
    export let reports;
</script>

<style>
.container {
    margin: 0 auto;
    width: 85%;
    max-width: 1200px;
    display: flex;
    justify-content: space-around;
    align-items: stretch;
    flex-flow: row wrap;
}

.card {
    flex: 0 1 300px;
    padding: 1.5rem 2rem;
    margin: 2% 0;
    border: 1px solid #034078;
    border-radius: 2px;
    display: flex;
    flex-flow: column nowrap;
    justify-content: space-between;
    align-items: start;
}

.top {
    font-style: italic;
    font-size: small;
}

.bold {
    font-weight: 500;
    margin-top: 0;
}

p {
    font-size: medium;
}

a {
    cursor: pointer;
    font-size: large;
    padding: .75rem 1rem;
    border: #000000 solid 1px;
    background-color: #2A2E45;
    color: #FFFFFF;
    text-decoration: none;
    border-radius: 5px;
}

a:hover {
    background-color: #FDFDFD;
    color: #000000;
}
</style>
<div class="container">
    {#each reports.reports as report}
        <div class="card">
            <p class="top">{report.superTitle}</p>
            {#if report.title}
                <h3>{report.title}</h3>
            {/if}
            {#if report.boldDescription}
                <p class="bold">{report.boldDescription}</p>
            {/if}
            {#if report.description}
                <p>{report.description}</p>
            {/if}
            <a href="{report.downloadURI}" target="_blank" >Download</a>
        </div>
    {/each}
</div>