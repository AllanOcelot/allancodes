<template>
    <div class="page-wrapper">
        <headerComponent />
        <div class="intro-unit">
            <div class="into-text">
                <h1>My name is Allan</h1>
                <p>I’m a full stack web developer and frontend designer. </br>
                   I have a passion for Open Source projects and all things <b>Space Related</b>.</p>
                <a href="https://www.github.com/allanocelot" class="button github" title="Find me on Github"><i class="fab fa-github-square"></i>Find me on Github</a>
                <a href="https://www.twitch.tv/allancodes" class="button twitch" title="Find me on Twitch"><i class="fab fa-twitch"></i> Find me on Twitch</a>
            </div>
        </div>

        <div class="about-me">
            <div class="container">
                <div class="row">
                    <div class="col-md-12 col-lg-4">
                        <h1>About me:</h1>
                        <p>I've been coding since I was 13 - now 25 with 8 years of commercial experience behind me, I like to think I have only scratched the surface of whats possible on the web.</p>
                        <p>I've been incredibly lucky in my career to work with some amazingly talented developers who I consider close friends.</p>
                        <p>I also spent a year and a half of my life being a <a href="https://en.wikipedia.org/wiki/Digital_nomad" alt="A digital nomad, Wikipedia definition">digital nomad</a>, traveling the world whilst doing what I love, coding!</p>
                        <p>I have no formal training, nor college or university qualifications and I hope this encourages people of all backgrounds to get involved with web development.</p>
                    </div>
                    <div class="col-md-8 d-none d-lg-block d-xs-block d-sm-none d-xs-none">
                        <img src="/assets/images/about.png"  alt="Me, at the most Westerly point in Europe.">
                    </div>
                </div>

                <div class="row">
                    <div class="col-sm-12 d-none d-lg-block d-xs-block d-sm-none d-xs-none">
                        <div class="calendar">
                            <!-- Loading stuff -->
                            Loading my github data... please wait...
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="projects">
            <div class="container">
                <div class="row">
                    <div class="col-sm-12">
                        <h2>Current projects:</h2>
                        <p>Find out more information about what I'm currently involved with:</p>
                    </div>
                </div>
                <div class="row">
                    <div class="col-md-4 col-sm-12">
                        <div class="project-block">
                            <p class="title">Runescape Goals</p>
                            <p>A fun VUE JS tool for generating tasks for Runescape players! </br> The aim is to intergrate the backend with RuneLite in future!</p>
                            <a href="https://github.com/AllanOcelot/Runescape-Goals" target="_blank"><i class="fab fa-github-square"></i>View on Github</a>
                        </div>
                    </div>
                    <div class="col-md-4 col-sm-12">
                        <div class="project-block">
                            <p class="title">Find My Nomads</p>
                            <p>A hobby project - aimed at encouraging more companies to hire developers as remote workers. This tool tracks tasks, locations and timezones in realtime.</p>
                            <a href="https://github.com/AllanOcelot/findmynomads" target="_blank"><i class="fab fa-github-square"></i>View on Github</a>
                        </div>
                    </div>
                    <div class="col-md-4 col-sm-12">
                        <div class="project-block">
                            <p class="title">Kiwi IRC</p>
                            <p>Most of my time is currently spent doing contract work for Kiwi IRC and it's parent companies. I love this job and the work we are able to do!</p>
                            <a href="https://github.com/kiwiirc/kiwiirc" target="_blank"><i class="fab fa-github-square"></i>View on Github</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <footerComponent />
    </div>
</template>
<script>
import headerComponent from '../components/includes/header.vue';
import footerComponent from '../components/includes/footer.vue';
import GitHubCalendar from 'github-calendar';

export default {
    name: 'homePage',
    components: {
        headerComponent,
        footerComponent
    },
    mounted: function() {
        new GitHubCalendar(".calendar", "allanOcelot", {responsive: true});
    }
}
</script>
