<!doctype html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <link
      rel="icon"
      href="images/logo-al-safha-al-portofolio.png"
      type="image/png"
    />
    <style>body {
  color: #fff;
  font-family: var(--main-font);
  text-decoration: none;
  min-height: 100vh;
  height: auto;
  background:
    linear-gradient(
      to right top,
      rgba(216, 58, 58, 0.4) 0%,
      rgba(216, 58, 58, 0.2) 10%,
      rgba(216, 58, 58, 0.1) 35%,
      transparent 60%
    ),
    linear-gradient(
      to left bottom,
      rgba(216, 58, 58, 0.4) 0%,
      rgba(216, 58, 58, 0.2) 10%,
      rgba(216, 58, 58, 0.1) 35%,
      transparent 50%
    );
  background-color: #030202;
  background-attachment: fixed;
}

html {
  scroll-behavior: smooth;
  overflow-x: hidden;
  scroll-padding-top: 70px;
  height: 100%;
  scrollbar-color: var(--main-color) #111;
}

* {
  margin: 0;
  padding: 0;
  /* overflow-x: hidden; */
  max-width: 100%;
  box-sizing: border-box;
}
:root {
  --main-color: #e23b3b;
  /* --section-background-1: #000;
  --section-background-2: rgba(42, 39, 39, 0.3); */
  --section-background-1: transparent;
  --section-background-2: transparent;
  --main-transition: 0.3s;
  --main-font: "Exo 2", sans-serif;
}
a {
  text-decoration: none;
  color: var(--main-color);
}

.stop {
  display: none;
  clear: both;
}

img {
  width: 100%;
}

h1 {
  text-align: center;
}

::selection {
  background-color: rgba(255, 0, 8, 0.4);
}

.title-section {
  color: rgba(255, 255, 255, 0.1);
  font-size: 100px;
  text-align: center;
  /* backdrop-filter: blur(10px); */
  font-weight: 850;
  letter-spacing: -3px;
  opacity: 0.7;
  margin: 0 0 70px 0;
}
.title-section + p {
  margin: -100px 0 0;
  font-size: 20px;
  text-align: center;
  color: #797979;
}

.typewriter {
  overflow: hidden;
  white-space: nowrap;
  border-right: 2px solid var(--main-color);
  width: 0;
  animation:
    typing 3s steps(50) forwards,
    blink 0.7s step-end infinite;
  margin: 0 auto;
}
::-webkit-scrollbar {
  width: 9px;
  transition: var(--main-transition);
}
::-webkit-scrollbar-track {
  background: #111;
}
::-webkit-scrollbar-thumb {
  background: var(--main-color);
  border-radius: 5px;
}
::-webkit-scrollbar-thumb:hover {
  background: #b71c1c;
}
@-moz-document url-prefix() {
  html {
    scrollbar-width: thin;
  }
}

/* ///////////////////////////    navbar 🔴    ////////////////////*/

.navbar {
  /* background: rgba(4, 4, 4, 0.8); */
  /* backdrop-filter: blur(10px); */
  animation-name: lettel-top-nav;
  animation-timing-function: linear;
  animation-fill-mode: both;
  animation-duration: auto;
  animation-timeline: scroll();
  animation-range: 0px 80px;
  height: 70px;
  width: 100%;
  position: fixed;
  top: 10px;
  border-radius: 20px;
  box-sizing: border-box;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999999999;
  border-bottom: 1px solid transparent;
}
.nav-container {
  max-width: 1400px;
  background: rgba(4, 4, 4, 0.5);
  width: 90%;
  animation-name: show-border;
  animation-timing-function: linear;
  animation-fill-mode: both;
  animation-duration: auto;
  animation-timeline: scroll();
  animation-range: 0px 80px;
  margin: 0 auto;
  border-radius: 25px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  box-sizing: border-box;
}
.sun,
.moon {
  font-size: large;
  color: #fff;
  transition: var(--main-transition);
  margin-right: 0;
  border-radius: 8px;
  padding: 7px;
  margin-top: 3px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.moon {
  display: none;
  text-align: center;
  margin-top: 6px;
}

.sun:hover,
.moon:hover {
  background-color: rgba(43, 43, 43, 0.5);
  color: var(--main-color);
  cursor: pointer;
}

.hamburger {
  display: none;
}

/* ---- logo (name and image) ----- */

.logo {
  display: flex;
  align-items: center;
  white-space: nowrap;
  font-size: 24px;
  font-family: var(--main-font);
  font-weight: bold;
}

.logo a {
  color: #fff;
  display: flex;
  align-items: center;
  text-decoration: none;
  transition: var(--main-transition);
}

.img-logo {
  width: 120px;
  margin: 0;
  margin-right: -25px;
  align-self: center;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr;
  align-items: center;
  justify-items: center;
}

.image-logo {
  grid-area: 1 / 1 / 2 / 2;
  width: 100%;
  max-height: 70px;
  object-fit: contain;
  transition: var(--main-transition);
  animation-name: logonav;
  animation-timing-function: linear;
  animation-fill-mode: both;
  animation-duration: auto;
  animation-timeline: scroll();
  animation-range: 0px 80px;
}

.image-logo-2 {
  grid-area: 1 / 1 / 2 / 2;
  width: 45px;
  max-height: 50px;
  margin: 0;
  object-fit: contain;
  transition: var(--main-transition);
  animation-name: logonavtwo;
  animation-timing-function: linear;
  animation-fill-mode: both;
  animation-duration: auto;
  animation-timeline: scroll();
  animation-range: 0px 80px;
}

.logo:hover a {
  color: var(--main-color);
}
.logo:hover .image-logo {
  transform: scale(1.05);
  filter: brightness(0) saturate(100%) invert(35%) sepia(86%) saturate(4619%)
    hue-rotate(345deg) brightness(113%) contrast(80%);
}

/* ---- links ---- */
.nav-phone {
  display: none;
  position: relative;
}

.nav-links-phone {
  margin: 0;
  padding: 0;
  background-color: #181818;
  position: absolute;
  list-style: none;
  right: 0;
  top: calc(100% + 15px);
  min-width: 200px;
  display: none;
}

.nav-links-phone li a {
  display: block;
  padding: 15px;
  color: #fff;
  transition: var(--main-transition);
}

.nav-links-phone li a:hover {
  color: var(--main-color);
  padding-left: 25px;
}

.nav-links-phone li {
  border-bottom: 1px solid rgb(61, 55, 55);
}

.sun-phone {
  padding: 15px;
  color: #fff;
  transition: var(--main-transition);
  text-align: center;
}

.sun-phone-child {
  border-radius: 7px;
  padding: 5px;
  border: solid 1px #2c2c2c;
  background-color: #131313;
}

.sun-phone span {
  padding-left: 5px;
}

.sun-phone-child:hover {
  color: var(--main-color);
  background-color: #2c2c2c;
}

.nav-links-phone::before {
  content: "";
  border-width: 10px;
  border-style: solid;
  border-color: transparent transparent #181818 transparent;
  position: absolute;
  right: 5px;
  top: -20px;
}

.nav-phone:hover .nav-links-phone {
  display: block;
}

.icon-nav {
  width: 30px;
  display: flex;
  flex-wrap: wrap;
  margin-right: 10px;
  gap: 5px;
  justify-content: flex-end;
}

.icon-nav span:first-child {
  height: 2px;
  width: 100%;
  background-color: #fff;
}

.icon-nav span:nth-child(2) {
  height: 2px;
  transition: var(--main-transition);
  width: 60%;
  background-color: #fff;
}

.icon-nav span:last-child {
  height: 2px;
  background-color: #fff;
  width: 100%;
}

.nav-phone:hover span:nth-child(2) {
  width: 100%;
}

.nav-links {
  list-style: none;
  display: flex;
  align-items: center;
  gap: 30px;
  margin: 0;
  padding: 0;
}

.nav-links li {
  margin: 0;
  padding: 0;
}

.nav-links a {
  color: #fff;
  text-decoration: none;
  font-size: 20px;
  transition: var(--main-transition);
}

.nav-links a:hover {
  color: var(--main-color);
}

/* ///////////////////     hero 🔴    ////////////////*/
.hero {
  height: auto;
  min-height: 100vh;
  margin-top: 50px;
  color: #fff;
  text-align: center;
  background-color: var(--section-background-1);
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 40px 0;
  text-align: center;
  color: #fff;
}

.hero-content {
  display: block;
}

.hero h1 {
  font-size: 80px;
  font-family: "Exo 2";
  margin: 10px 0;
}

.hero p {
  font-size: 24px;
  font-family: "Dancing Script";
  color: var(--main-color);
  margin-bottom: 22px;
}

.text-hero {
  margin-top: 9vh;
}

.hero img {
  margin: auto;
  margin-top: 20px;
}

.image {
  animation: Pulse 2s infinite;
  width: 200px;
  filter: contrast(115%) brightness(110%) saturate(150%);
  height: 200px;
  border-radius: 50%;
  border: #141414 solid;
  transition: transform 1s 1s;
  margin: auto;
}

.Hamza_Gamal {
  text-shadow: 1px 1px 30px rgba(255, 48, 48, 0.9);
}

.image-caption:hover .image {
  transform: scale(1.1, 1.1);
}

.image-caption:hover .caption {
  opacity: 1;
  transition: opacity 1s;
  transform: rotate(360deg);
}

.image-caption:hover .caption h2 {
  transition: left 1s 1s;
  left: 0;
}

.image-caption:hover .caption p {
  transition: left 1s 1s;
  left: 0;
}

.image-caption {
  position: relative;
  overflow: hidden;
  height: 230px;
  margin: auto;
  width: 240px;
}

.caption {
  position: absolute;
  overflow: hidden;
  left: 20px;
  background-color: rgba(48, 48, 48, 0.6);
  width: 200px;
  height: 200px;
  border-radius: 50%;
  top: 20px;
  opacity: 0;
  transition:
    opacity 0.5s,
    transform 1s;
}

.caption p {
  color: tomato;
  transition: left 0.5s 0.5s;
  margin-top: 20px;
  font-family: var(--main-font);
  font-size: large;
  position: relative;
  left: 100%;
}

.caption h2 {
  transition: left 0.5s 0.5s;
  position: relative;
  left: 100%;
  background-color: rgba(0, 0, 0);
  padding-top: 30px;
  margin: 0;
  font-size: 20px;
  color: tomato;
  width: 90%;
  margin-left: 10px;
}

.main-btn,
.sec-btn {
  padding: 10px 23px;
  text-decoration: none;
  border-radius: 5px;
  margin: 10px;
  display: inline-block;
  font-weight: bold;
  transition: all var(--main-transition) ease-in-out;
}

.sec-btn,
.main-btn {
  background-color: transparent;
  color: var(--main-color);
  border: 2px solid var(--main-color);
  display: inline-block;
  transition: all var(--main-transition) ease-in-out;
}

.main-btn:hover,
.sec-btn:hover {
  background-color: var(--main-color);
  color: #000;
  transform: translateY(-4px);
  box-shadow: 0 6px 20px rgba(226, 59, 59, 0.5);
}
.Welcomeportfolio {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  transition: var(--main-transition);
  gap: 8px;
  cursor: pointer;
}

.Welcomeportfolio:hover {
  color: tomato;
  transform: scale(1.05);
}

.Welcomeportfolio::after {
  content: attr(data-text);
  max-width: 0;
  opacity: 0;
  overflow: hidden;
  white-space: nowrap;
  transition:
    max-width 0.5s ease,
    opacity 0.4s ease;
}

.Welcomeportfolio:hover::after {
  max-width: 200px;
  opacity: 1;
}

/* ////////////////////////    about 🔴     /////////////////////*/

.about {
  background-size: cover;
  width: 100%;
  margin: auto;
  margin-bottom: 50px;
  padding: 50px 0 50px 0;
  background-color: var(--section-background-2);
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: center;
  gap: 50px;
}
.aboutimg {
  position: relative;
  filter: saturate(1.2) contrast(1.1) brightness(0.9);
}
.mark-dev {
  color: red;
  font-weight: bold;
  padding-left: 5px;
}
.back-img {
  position: absolute;
  bottom: -10px;
  right: 20px;
  border: 1px solid #ff3131;
  width: 140px;
  height: 37px;
  font-size: 14px;
  background-color: rgba(255, 65, 65, 0.3);
  backdrop-filter: blur(30px);
  display: flex;
  align-items: center;
  font-weight: bold;
  justify-content: center;
  border-radius: 50px;
}

.about img {
  box-shadow: 0 0 60px 10px rgba(255, 0, 8, 0.2);
  width: 320px;
  border-radius: 50px;
  border: 1px solid oklch(0.3 0.03 260);
  animation: topandbottom 1.3s infinite alternate;
}

.puzziles-about {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  flex-wrap: wrap;
  gap: 20px;
}
.caption-puzzile-about {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
}
.image-about {
  display: flex;
  justify-content: center;
  flex-direction: column;
}

.puzzile-about {
  width: auto;
  min-width: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding: 10px;
  gap: 10px;
  border: #333 solid 0.5px;
  border-radius: 15px;
  text-align: center;
  height: auto;
  max-height: 100px;
  background-color: #202020;
  transition: 0.4s;
}

.puzzile-about:hover {
  transform: translateY(-5px);
  background-color: #313131;
}

.puzzile-about:active {
  transform: scale(0.9);
}

.bottom-puzzile {
  color: rgb(167, 167, 167);
}
.top-puzzile {
  color: rgb(231, 72, 72);
  font-weight: bold;
  font-size: 20px;
}

.about p:first-of-type {
  color: rgb(255, 0, 0);
  font-family: var(--main-font);
  font-optical-sizing: auto;
}

.caption-about {
  color: rgba(255, 255, 255, 0.7);
  font-family: var(--main-font);
  font-size: 17px;
  line-height: 1.4;
  width: auto;
  padding-right: 20px;
  max-width: 400px;
}

/* //////////////////    Services 🔴    /////////////////////////*/

.Servises {
  padding-top: 60px;
  padding-bottom: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.Servises .Servises-content {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-gap: 20px;
  margin-top: 100px;
}
.Servises .Servises-content .srv {
  display: flex;
  margin-bottom: 40px;
}
.Servises .Servises-content .srv i {
  color: var(--main-color);
  flex-basis: 60px;
}
.one-icon-srv {
  font-size: 30px;
  margin-right: 20px;
}
.Servises .Servises-content .srv .text {
  flex: 1;
}
.Servises .Servises-content .srv .text h3 {
  margin: 0 0 20px;
}
.Servises .Servises-content .srv .text p {
  color: gray;
  font-weight: 300;
  line-height: 1.6;
}
.Servises .Servises-content .image-col {
  text-align: center;
  position: relative;
}
.Servises .Servises-content .image-col img {
  width: 260px;
  animation: topandbottom 1.3s infinite alternate;
}
.Servises .Servises-content .image-col::before {
  content: "";
  position: absolute;
  right: 0;
  background-color: rgba(216, 58, 58, 0.4);
  width: 100px;
  height: calc(100% + 100px);
  top: -50px;
  z-index: -1;
}
.Servises .Servises-content .image-col::after {
  content: "";
}
@media (max-width: 767px) {
  .Servises .Servises-content .srv {
    flex-direction: column;
    text-align: center;
  }
  .Servises .Servises-content .srv p {
    max-width: 400px;
    padding-left: 10px;
    padding-right: 10px;
    margin: auto;
  }
  .Servises .Servises-content .srv i {
    margin: auto;
  }
}
@media (max-width: 1199px) {
  .image-col-column {
    display: none;
  }
}
@media (max-width: 1199px) {
  .image-column {
    display: none;
  }
}

/* //////////////////    Projects 🔴    /////////////////////////*/

.Projects {
  width: 100%;
  margin: 70px auto;
  display: flex;
  justify-content: center;
  align-items: stretch;
  padding: 0;
  gap: 25px;
  flex-wrap: wrap;
  max-width: 1689px;
}

.Project {
  display: flex;
  padding: 0;
  align-items: stretch;
  flex-direction: column;
  cursor: pointer;
  overflow: hidden;
  box-sizing: border-box;
  transition: 0.3s;
  width: 37%;
  max-width: 550px;
  border: solid 0.5px rgba(255, 134, 134, 0.2);
  position: relative;
  border-radius: 20px;
}
.Project img {
  border-top-left-radius: 15px;
  border-top-right-radius: 15px;
  filter: brightness(0.7);
  transition:
    transform 0.4s ease-in-out,
    filter var(--main-transition) ease-in-out;
  margin: 0;
  display: block;
  height: 300px;
  width: auto;
}

.Project:hover {
  transform: translate(0, -5px);
  border: solid 0.5px rgba(255, 134, 134, 0.6234);
  transform: translate(0, -5px);
  border: solid 0.5px rgba(255, 134, 134, 0.6234);
  box-shadow:
    0px 20px 50px -10px rgba(226, 59, 59, 0.5),
    0 3px 4px 0px rgba(226, 59, 59, 0.5);
}

.Project:hover img {
  filter: brightness(1);
  transform: scale(1.05);
}
.Project:hover::after {
  opacity: 0;
}
.Project::after {
  content: "";
  position: absolute;
  transition: 1s;
  left: 0;
  bottom: 0;
  width: 100%;
  background: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0) 0%,
    rgba(0, 0, 0, 0.8) 40%,
    rgba(0, 0, 0, 1) 100%
  );
  z-index: 1;
  pointer-events: none;
  height: 70%;
}

.Project:nth-child(4)::after {
  height: 0;
}

.Project a {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.Project .t-c-p {
  position: relative;
  z-index: 2;
  display: flex;
  background-color: #000;
  flex-direction: column;
  flex-grow: 1;
}

.Project .t-c-p h2 {
  color: #fff;
  font-size: 22px;
  transition: 0.3s;
  margin: 0;
  font-weight: bold;
  display: flex;
  align-items: center;
  font-family: "Exo 2", sans-serif;
  padding-left: 10px;
  padding-top: 40px;
}

.Project .t-c-p p {
  transition: 0.3s;
  padding: 15px;
  color: rgb(100, 100, 100);
  border-bottom-left-radius: 15px;
  /* height: auto;
  min-height: 150px; */
  flex-grow: 1;
  height: auto;
  font-family: "Exo 2", sans-serif;
  line-height: 1.7;
  border-bottom-right-radius: 15px;
  margin-bottom: -10px;
}
.Project:hover .t-c-p P {
  color: rgb(170, 170, 170);
}

.Project:hover .Pr {
  color: rgb(170, 170, 170);
  background-color: rgba(255, 179, 179, 0.2);
}

.ProgrammingLanguagesPr {
  height: auto;
  width: 100%;
  display: flex;
  gap: 10px;
  flex-direction: row;
  padding: 10px;
  padding-bottom: 20px;
}
.Pr {
  color: rgb(150, 150, 150);
  font-weight: bold;
  transition: var(--main-transition);
  background-color: rgba(255, 179, 179, 0.1);
  height: 26px;
  width: auto;
  padding: 10px;
  padding-right: 15px;
  padding-left: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: small;
  border-radius: 20px;
}

/* ///////////////////   skills 🔴  ////////////////////////*/

.skills {
  width: 100%;
  background-color: var(--section-background-1);
  padding: 60px 20px;
  font-family: var(--main-font);
  margin: auto;
  box-sizing: border-box;
}

.skills-container {
  max-width: 1000px;
  margin: 90px auto auto auto;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.skill {
  background-color: #161616;
  border: 1px solid #222;
  cursor: pointer;
  border-radius: 16px;
  padding: 24px;
  transition:
    transform var(--main-transition) ease,
    border-color var(--main-transition) ease;
}

.skill:hover {
  transform: translateY(-5px);
  border-color: var(--main-color);
}

.skill:active {
  transform: translateY(-5px) scale(0.93);
}
.skill-header {
  display: flex;
  align-items: center;
  gap: 15px;
  margin-bottom: 20px;
}

.skill-icon {
  font-size: 28px;
  display: flex;
  align-items: center;
}

.skill-name {
  color: #fff;
  font-size: 1.2rem;
  font-weight: 500;
  font-family: var(--main-font);
}

.skill-footer {
  display: flex;
  align-items: center;
  gap: 15px;
  position: relative;
  padding-top: 10px;
}

.skill-footer::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 80%;
  height: 6px;
  background: #222;
  border-radius: 10px;
}

.progress-bar {
  position: absolute;
  top: 0;
  left: 0;
  height: 6px;
  background: linear-gradient(90deg, var(--main-color), #ff7676);
  border-radius: 10px;
}

.skill-percentage {
  color: #888;
  font-size: 0.9rem;
  font-family: var(--main-font);
  margin-left: auto;
}

/* /////////////////////    form 🔴    //////////////////////*/

.footer {
  background-color: var(--section-background-2);
  display: flex;
  justify-content: center;
  align-items: flex-start;
  gap: 40px;
  flex-wrap: wrap;
  padding: 40px;
}

/* --- contact --- */

form {
  background: #070707;
  overflow: hidden;
  display: block;
  max-width: 600px;
  width: 100%;
  flex: 1 1 500px;
  margin: 0;
  border-radius: 10px;
  color: #fff;
  border: rgb(51, 51, 51) 0.1px solid;
  padding: 20px 0;
  margin: 0;
}
.text-form {
  display: flex;
  flex-direction: column;
  gap: 8px;
  width: 90%;
  margin: 0 auto 25px auto;
  text-align: left;
}

.text-form h2 {
  font-size: 24px;
  font-family: var(--main-font);
  color: #fff;
  margin: 0;
}

.caption-form {
  max-width: 100%;
  font-size: 15px;
  color: rgb(150, 150, 150);
  line-height: 1.5;
  margin: 0;
}

.inputs-group {
  display: flex;
  justify-content: space-between;
  width: 90%;
  margin: 0 auto 20px auto;
  gap: 20px;
  flex-wrap: wrap;
}

form input {
  background-color: #070707;
  border: 1px solid #333;
  border-radius: 5px;
  padding: 10px;
  flex: 1;
  font-family: var(--main-font);
  font-weight: 500;
  font-size: medium;
  color: #fff;
}

input::placeholder {
  color: rgb(163, 163, 163);
  opacity: 1;
}

form button {
  padding: 10px;
  background-size: cover;
  background-position: center center;
  border: #333 solid 1px;
  background-color: var(--main-color);
  color: #ffffff;
  font-weight: bold;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  letter-spacing: 1px;
  font-size: 17px;
  cursor: pointer;
  font-family: var(--main-font);
  border-radius: 5px;
  width: 90%;
  transition: var(--main-transition);
}
.btn-form {
  display: flex;
  justify-content: center;
  align-items: center;
}
form button:hover {
  background-color: #ff3131;
}

input:focus,
textarea:focus {
  border-color: rgba(255, 121, 121, 0.7);
  border-width: 1.6px;
  outline: none;
}

textarea {
  color: #fff;
  width: 90%;
  overflow: auto;
  display: flex;
  font-family: var(--main-font);
  font-weight: 500;
  font-size: medium;
  margin: auto;
  resize: vertical;
  min-height: 100px;
  max-height: 150px;
  height: 130px;
  border-radius: 5px;
  background-color: #070707;
  border: 1px solid #333;
  border-radius: 5px;
  padding: 10px;
}
textarea::placeholder {
  color: rgb(163, 163, 163);
  opacity: 1;
}

.IconBtnForm {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 4px;
}
/* --- contactme --- */

.Contactme {
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  max-width: 600px;
  gap: 15px;
  width: 300px;
}

.icon-contactme {
  background-color: rgba(255, 0, 0, 0.2);
  width: 45px;
  height: 45px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 25px;
  color: red;
}

.title-contactme {
  font-weight: bold;
  color: white;
  text-align: left;
  display: block;
}

.data-contactme {
  color: gray;
  font-size: 14px;
  display: block;
}

.Contactme a {
  transition: 0.2s;
}

.Contactme a:hover {
  color: rgb(179, 14, 14);
}

.e-l-p-text {
  display: flex;
  flex-direction: column;
}

.e-l-p {
  background-color: #070707;
  margin: 0;
  display: flex;
  align-items: center;
  gap: 15px;
  width: 100%;
  padding: 20px;
  padding-top: 25px;
  border-radius: 10px;
  border: rgb(51, 51, 51) 0.1px solid;
}

/* ///////////////////    footer 🔴    //////////////////////*/

footer {
  background-color: #000;
  color: gray;
  display: flex;
  flex-direction: column;
  border-top: #2c2c2c 1px solid;
  padding: 50px 0;
  gap: 20px;
}

.footer-container {
  width: 100%;
  margin: 0 auto;
  max-width: 1200px;
  padding: 0 40px;
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.footer-row-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo-box {
  display: flex;
  align-items: center;
}

.logo-box:hover .title-logo {
  color: var(--main-color);
}

.logo-box:hover .logo-image-footer {
  filter: brightness(0) saturate(100%) invert(35%) sepia(86%) saturate(4619%)
    hue-rotate(345deg) brightness(113%) contrast(80%);
}

.title-logo {
  color: #fff;
  transition: 0.5s;
  font-weight: bold;
  font-family: var(--main-font);
  font-size: larger;
  margin-left: -13px;
}

.title-logo:hover {
  color: var(--main-color);
}

.title-logo:hover .logo-image-footer {
  filter: brightness(0) saturate(100%) invert(35%) sepia(86%) saturate(4619%)
    hue-rotate(345deg) brightness(113%) contrast(80%);
}

.logo-image-footer {
  width: 80px;
  height: auto;
  transition: 0.5s;
}

.footer-row-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-top: 1px solid #2c2c2c;
  padding-top: 15px;
}

.footer-caption {
  padding-top: 10px;
  display: inline-block;
  transition: var(--main-transition);
  font-weight: 500;
  white-space: nowrap;
  font-size: 15px;
}
.icon-footer {
  position: relative;
  color: #fff;
  font-size: 18px;
  transition: all var(--main-transition) ease-in-out;
  text-decoration: none;
  height: 38px;
  width: 38px;
  display: inline-flex;
  justify-content: center;
  border-radius: 5px;
  align-items: center;
}

.icon-footer:hover {
  color: var(--main-color);
  background-color: rgba(255, 131, 131, 0.1);
}
.icon-footer::before {
  content: "▼";
  position: absolute;
  bottom: calc(100% + 1px);
  left: 50%;
  transform: translateX(-50%) translateY(-5px) scale(0.85);
  font-size: 11px;
  color: #0f172a;
  text-shadow:
    1px 0 0 rgba(255, 255, 255, 0.15),
    -1px 0 0 rgba(255, 255, 255, 0.15),
    0 1px 0 rgba(255, 255, 255, 0.15);
  z-index: 100000;
  opacity: 0;
  visibility: hidden;
  font-family: var(--main-font);
  transition:
    opacity 0.25s ease-in-out,
    transform 0.25s ease-in-out,
    visibility 0.25s;
  transition-delay: var(--main-transition);
}
.icon-footer::after {
  content: attr(data-tooltip);
  position: absolute;
  bottom: calc(100% + 9px);
  left: 50%;
  transform: translateX(-50%) translateY(-5px) scale(0.85);
  background-color: #0f172a;
  color: #fff;
  font-family: var(--main-font);
  letter-spacing: 1px;
  font-size: 11px;
  font-weight: bold;
  white-space: nowrap;
  padding: 5px 10px;
  border-radius: 6px;
  border: 1px solid rgba(255, 255, 255, 0.15);
  z-index: 99999;
  opacity: 0;
  visibility: hidden;
  transition:
    opacity 0.25s ease-in-out,
    transform 0.25s ease-in-out,
    visibility 0.25s;
  transition-delay: var(--main-transition);
}

.icon-footer:hover::before,
.icon-footer:hover::after {
  opacity: 1;
  visibility: visible;
  transform: translateX(-50%) translateY(0) scale(1);
}

.logo-footer:hover .logo-image-footer {
  transform: scale(1.05);
  filter: brightness(0) saturate(100%) invert(35%) sepia(86%) saturate(4619%)
    hue-rotate(345deg) brightness(113%) contrast(80%);
}
#toast {
  position: fixed;
  top: 15%;
  right: 40%;
  background: #22c55e;
  color: #fff;
  padding: 14px 18px;
  border-radius: 10px;
  font-size: 14px;
  font-weight: 500;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
  opacity: 0;
  visibility: hidden;
  transform: translateY(-20px);
  transition: all var(--main-transition) ease;
  z-index: 99999;
}

#toast.show {
  opacity: 1;
  visibility: visible;
  transform: translateY(0);
}

.btn-back-to-top {
  background-color: #000;
  border: 1px solid rgba(226, 59, 59, 0.6);
  width: 48px;
  height: 48px;
  border-radius: 50%;
  text-decoration: none;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: large;
  z-index: 9999;
  position: fixed;
  bottom: 20px;
  right: 20px;
  transition: all var(--main-transition) ease-in-out;
  animation: showButton linear both;
  animation-timeline: scroll();
  animation-range: entry 0 exit 500px;
}

.btn-back-to-top img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  transform: scale(1.6);
  transition: transform var(--main-transition) ease-in-out;
}

.btn-back-to-top:hover {
  background-color: #000;
  border-color: var(--main-color);
  transform: translateY(-4px) scale(1);
  box-shadow: 0 3px 9px 2px rgba(255, 75, 75, 0.6);
}

.btn-back-to-top:hover img {
  transform: scale(1.6);
}

/* ///////////// media 🔴 //////////////// */

@media (max-width: 470px) {
  .title-section {
    font-size: 70px;
  }
}

@media (max-width: 950px) {
  .nav-links {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: #111;
  }

  .nav-phone {
    display: block;
  }

  .logo {
    margin-left: -35px;
  }

  .hamburger {
    display: block;
  }

  .nav-links.active {
    display: block;
  }

  .hamburger {
    display: block;
  }
}

@media (max-width: 600px) {
  @keyframes typing {
    to {
      width: 360px;
    }
  }

  .hero p {
    font-size: 18px;
  }
}

@media (max-width: 964px) {
  .caption-puzzile-about {
    margin-top: 50px;
    margin-left: 30px;
  }
}

@media (max-width: 1007px) {
  .Project {
    width: 40%;
    max-width: 400px;
  }
}

@media (max-width: 750px) {
  .Project {
    width: 90%;
    max-width: 400px;
  }
}

@media (max-width: 635px) {
  .skills {
    width: 90%;
  }

  textarea {
    padding-bottom: 0;
    margin-bottom: 0;
  }

  button {
    width: 100%;
  }
}

@media (max-width: 777px) {
  .footer-caption {
    margin: auto;
    display: block;
    margin-bottom: 20px;
  }
}

@media (max-width: 600px) {
  .logo-image-footer {
    width: 110px;
    margin-right: -20px;
  }

  .footer-row-top {
    flex-direction: column;
    gap: 0;
    align-items: center;
    text-align: center;
  }

  .logo-box {
    flex-direction: row;
    gap: 0;
    padding-bottom: 15px;
    border-bottom: 1px solid #2c2c2c;
    width: 100%;
    justify-content: center;
    align-items: center;
  }

  .title-logo {
    margin-left: 0;
    font-size: 18px;
  }

  .social-box {
    width: 100%;
    display: flex;
    justify-content: center;
    gap: 15px;
    padding-top: 15px;
    padding-bottom: 0;
  }

  .footer-row-bottom {
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 0;
    border-top: none;
    padding-top: 0;
  }

  .footer-caption {
    width: 100%;
    text-align: center;
    padding-top: 15px;
    padding-bottom: 15px;
    margin: 0;
    white-space: normal;
    border-top: 1px solid #2c2c2c;
  }
}

@media (max-width: 909px) {
  .Contactme {
    width: 100%;
  }

  form {
    width: 100%;
  }
}

@media (max-width: 600px) {
  .inputs-group {
    flex-direction: column;
    gap: 15px;
  }

  form input {
    width: 100%;
  }
}
@media (max-width: 600px) {
  .text-form {
    text-align: center;
    margin-bottom: 20px;
  }
}

@media (max-width: 480px) {
  .icon-footer::before,
  .icon-footer::after {
    display: none;
  }
}

/* ///////////////////////////    Keyframes 🔴    ////////////////////*/

@keyframes show-border {
  from {
    background-color: transparent;
    width: 100%;
    border-radius: 0;
    box-shadow:
      0px -1px 8px 6px rgba(255, 255, 255, 0),
      0 3px 4px 0px rgba(255, 255, 255, 0);
  }

  to {
    background: rgba(4, 4, 4, 0.5);
    backdrop-filter: blur(3px);
    box-shadow:
      0px -1px 8px 6px rgba(255, 255, 255, 0.05),
      0 3px 4px 0px rgba(255, 255, 255, 0.03);
  }
}

@keyframes lettel-top-nav {
  from {
    top: 0px;
  }

  to {
    top: 15px;
    border-radius: 0px 0px 20px 20px;
  }
}

@keyframes Pulse {
  0% {
    box-shadow: 0 0 1px #ff6e6e;
  }

  50% {
    box-shadow: 0 0 15px #ff6e6e;
  }

  100% {
    box-shadow: 0 0 1px #ff6e6e;
  }
}

@keyframes typing {
  from {
    width: 0;
  }

  to {
    width: 470px;
  }
}

@keyframes blink {
  50% {
    border-color: transparent;
  }
}

@keyframes showButton {
  from {
    opacity: 0;
    visibility: hidden;
    transform: scale(0);
  }
  to {
    opacity: 1;
    visibility: visible;
    transform: scale(1);
  }
}

@keyframes logonavtwo {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}

@keyframes logonav {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes topandbottom {
  from {
    transform: translate(0, -15px);
  }
  to {
    transform: translate(0, 0px);
  }
}
</style>
    <title>Hamza Gamal | Portfolio</title>

    <!-- ///////////////// -->

    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"
    />
    <link
      href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400..700&family=Exo+2:ital,wght@0,100..900;1,100..900&family=Fira+Sans:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Playwrite+DE+SAS:wght@300&family=Roboto:ital,wght@0,100..900;1,100..900&family=Rubik+Storm&display=swap"
      rel="stylesheet"
    />
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css"
    />
  </head>

  <body id="home">
    <!-- /////////   Navbar 🔴 ////////////// -->
    <header>
      <nav class="navbar">
        <div class="nav-container">
          <div class="logo">
            <a href="https://hamza-gamal.github.io/portfolio/">
              <div class="img-logo">
                <img
                  class="image-logo"
                  src="images/logo-white.png"
                  alt="logo"
                />
                <img
                  class="image-logo-2"
                  src="images/logo-al-safha-al-portofolio.png"
                  alt="logo"
                />
              </div>
              Hamza Gamal
            </a>
          </div>

          <div class="nav-phone">
            <span class="icon-nav">
              <span></span>
              <span></span>
              <span></span>
            </span>

            <div class="nav-links-phone">
              <li><a href="#home">Home</a></li>
              <li><a href="#about">About</a></li>
              <li><a href="#Services">Services</a></li>
              <li><a href="#Projects">Projects</a></li>
              <li><a href="#Skills">Skills</a></li>
              <li><a href="#Contact">Contact </a></li>
              <div id="sun" class="sun-phone">
                <div class="sun-phone-child">
                  <i class="fa-solid fa-sun"></i> <span>Light Mode</span>
                </div>
              </div>
            </div>
          </div>

          <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#Services">Services</a></li>
            <li><a href="#Projects">Projects</a></li>
            <li><a href="#Skills">Skills</a></li>
            <li><a href="#Contact">Contact </a></li>
            <div id="sun" class="sun"><i class="fa-solid fa-sun"></i></div>
            <div class="moon"><i class="fa-solid fa-moon"></i></div>
          </ul>
        </div>
      </nav>
    </header>

    <!-- ////////////  Hero 🔴 ////////////// -->

    <section class="hero">
      <div class="hero-content">
        <div class="image-caption">
          <div class="image-2-caption">
            <!-- <img class="image" src="images/hamza-pic4.jfif" alt="moparmeg" /> -->
            <img class="image" src="images/about.png" alt="moparmeg" />
          </div>
          <div class="caption">
            <h2>Hamza Gamal</h2>
            <p>Frontend Developer | Designer | Programming Engineer</p>
          </div>
        </div>
        <div class="text-hero">
          <h3 class="Welcomeportfolio" data-text="to My portfolio">Welcome</h3>
          <h1 class="Hamza_Gamal">HAMZA GAMAL</h1>
          <p class="typewriter">
            Frontend Developer | Designer | Programming Engineer
          </p>
          <div>
            <a href="#Projects" class="main-btn">View Work</a>
            <a  href="#Contact" class="sec-btn">Let's Talk</a>
          </div>
        </div>
      </div>
    </section>
    <span class="stop"></span>

    <!-- ///////////  About Me 🔴  ///////// -->

    <section class="about" id="about">
      <div class="aboutimg">
        <img class="image-about" src="images/about.png" alt="my image" />
        <div class="back-img">
          Front-End Dev <span class="mark-dev">&lt;/&gt;</span>
        </div>
      </div>
      <div class="caption-puzzile-about">
        <p>ABOUT ME</p>
        <h2>Hi, I'm Hamza Gamal 👋</h2>

        <p class="caption-about">
          I'm an Egyptian Front-End Developer dedicated to creating clean and
          responsive web designs. I build websites using HTML, CSS, and
          JavaScript, and I have already developed several projects, including a
          Holy Quran website.
        </p>

        <div class="puzziles-about">
          <div class="puzzile-about">
            <div class="top-puzzile">4+</div>
            <div class="bottom-puzzile">Projects</div>
          </div>

          <div class="puzzile-about">
            <div class="top-puzzile" style="font-size: 40px; margin: -15px 0">
              ∞
            </div>
            <div class="bottom-puzzile">Attention to detail</div>
          </div>

          <div class="puzzile-about">
            <div class="top-puzzile">100%</div>
            <div class="bottom-puzzile">Responsive Design</div>
          </div>
        </div>

        <!-- <div class=" puzzile-about">
          <div
            style="
              color: rgb(231, 72, 72);
              margin-top: 15px;
              font-weight: bold;
              font-size: 20px;
            "
          >
            +13
          </div>
          <div style="color: rgb(167, 167, 167); margin-top: 8px">
            Years Old
          </div>
        </div> -->
      </div>
    </section>

    <!-- ///////////  Services 🔴  ///////// -->

    <div class="Servises">
      <div class="container" id="Services">
        <h2 class="title-section">Services</h2>
        <p>What can I do for you ?</p>
        <div class="Servises-content">
          <div class="col">
            <!-- Start Servises -->
            <div class="srv">
              <i class="fas fa-palette fa-2x"></i>
              <div class="text">
                <h3>Graphic Design</h3>
                <p>
                  Graphic design is the process of visual communication and
                  problem-solving using one or more of typography, photography
                  and illustration.
                </p>
              </div>
            </div>
            <div class="srv">
              <i class="fab fa-sketch fa-2x"></i>
              <div class="text">
                <h3>UI & UX</h3>
                <p>
                  Process of enhancing user satisfaction with a product by
                  improving the usability, accessibility, and pleasure provided
                  in the interaction.
                </p>
              </div>
            </div>
          </div>
          <div class="col">
            <div class="srv">
              <div class="one-icon-srv">
                <i class="bi bi-bounding-box"></i>
              </div>
              <div class="text">
                <h3>Web Design</h3>
                <p>
                  Web design encompasses many different skills and disciplines
                  in the production and maintenance of websites.
                </p>
              </div>
            </div>

            <div class="srv">
              <i class="fas fa-pencil fa-2x"></i>
              <div class="text">
                <h3>Web Development</h3>
                <p>
                  Web development is a broad term for the work involved in
                  developing a web site for the Internet or an intranet.
                </p>
              </div>
            </div>
            <!-- End Servises -->
          </div>
          <div class="col">
            <div class="image-col image-column">
              <img src="images/Services.png" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ///////////  Projects 🔴  //////////// -->

    <h2 class="title-section" id="Projects">Projects</h2>
    <p>Check Out My Work</p>
    <section class="Projects">
      <div class="Project">
        <a target="_blank" href="https://hamza-gamal.github.io/quran-kareem/">
          <img src="images/image copy 8.png" alt="Quran" />
          <div class="t-c-p">
            <h2>Quran</h2>
            <p>
              An online website containing the entire Holy Quran for reading,
              featuring a clean, elegant, and easy-to-use user interface , Read
              and reflect upon the verses of God in a tranquil experience .
            </p>
            <div class="ProgrammingLanguagesPr">
              <div class="PrHTML Pr">HTML</div>
              <div class="PrCSS Pr">CSS</div>
              <div class="PrJS Pr">JS</div>
              <!-- <div class="PrResponsive Pr">Responsive</div> -->
            </div>
          </div>
        </a>
      </div>

      <div class="Project">
        <a target="_blank" href="https://hamza-gamal.github.io/portfolio/">
          <img src="images/image copy 7.png" alt="Portfolio" />
          <div class="t-c-p">
            <h2>Portfolio</h2>
            <p>
              This is my portfolio. It was created in 2025, featuring a clean,
              elegant, and easy-to-use user interface. It displays my skills,
              projects, and personal information
            </p>
            <div class="ProgrammingLanguagesPr">
              <div class="PrHTML Pr">HTML</div>
              <div class="PrCSS Pr">CSS</div>
              <!-- <div class="PrJS Pr">JS</div> -->
              <div class="PrResponsive Pr">Responsive</div>
            </div>
          </div>
        </a>
      </div>

      <div class="Project">
        <a target="_blank" href="https://hamza-gamal.github.io/leon/">
          <img src="images/leon.png" alt="leon" />
          <div class="t-c-p">
            <h2>Leon</h2>
            <p>
              A light-mode website built using HTML5, CSS3, and JavaScript as a
              showcase project. It features an eye-comfortable design that is
              fully responsive and optimized to look great on all device
              screens.
            </p>
            <div class="ProgrammingLanguagesPr">
              <div class="PrHTML Pr">HTML</div>
              <div class="PrCSS Pr">CSS</div>
              <!-- <div class="PrJS Pr">JS</div> -->
              <div class="PrResponsive Pr">Responsive</div>
            </div>
          </div>
        </a>
      </div>

      <div class="Project">
        <a target="_blank" href="https://hamza-gamal.github.io/restaurant/">
          <img src="images/imageresturant.png" alt="Restaurant" />
          <div class="t-c-p">
            <h2>Restaurant</h2>
            <p>
              An experimental restaurant website designed as a concept project
              to showcase my modern UI layouts and responsive frontend
              development skills
            </p>
            <div class="ProgrammingLanguagesPr">
              <div class="PrHTML Pr">HTML</div>
              <div class="PrCSS Pr">CSS</div>
              <div class="PrJS Pr">JS</div>
              <!-- <div class="PrResponsive Pr">Responsive</div> -->
            </div>
          </div>
        </a>
      </div>
    </section>

    <!-- //////////////  Skills 🔴  ////////////// -->

    <div class="skills" id="Skills">
      <h2 class="title-section">Skills</h2>
      <p>My Web Tech Stack</p>
      <div class="skills-container">
        <div class="skills-grid">
          <!-- HTML5 -->
          <div class="skill">
            <div class="skill-header">
              <span class="skill-icon"
                ><i class="fa-brands fa-html5" style="color: #e34c26"></i
              ></span>
              <span class="skill-name">HTML5</span>
            </div>
            <div class="skill-footer">
              <div class="progress-bar" style="width: 100%"></div>
              <span class="skill-percentage">100%</span>
            </div>
          </div>

          <!-- CSS3 -->
          <div class="skill">
            <div class="skill-header">
              <span class="skill-icon"
                ><i class="fa-brands fa-css3-alt" style="color: #264de4"></i
              ></span>
              <span class="skill-name">CSS3</span>
            </div>
            <div class="skill-footer">
              <div class="progress-bar" style="width: 95%"></div>
              <span class="skill-percentage">95%</span>
            </div>
          </div>

          <!-- JavaScript -->
          <div class="skill">
            <div class="skill-header">
              <span class="skill-icon"
                ><i class="fa-brands fa-js" style="color: #f7df1e"></i
              ></span>
              <span class="skill-name">JavaScript</span>
            </div>
            <div class="skill-footer">
              <div class="progress-bar" style="width: 10%"></div>
              <span class="skill-percentage">10%</span>
            </div>
          </div>

          <!-- UI Design -->
          <div class="skill">
            <div class="skill-header">
              <span class="skill-icon"
                ><i class="fa-solid fa-desktop" style="color: #a855f7"></i
              ></span>
              <span class="skill-name">UI Design</span>
            </div>
            <div class="skill-footer">
              <div class="progress-bar" style="width: 75%"></div>
              <span class="skill-percentage">75%</span>
            </div>
          </div>

          <!-- UX Design -->
          <div class="skill">
            <div class="skill-header">
              <span class="skill-icon"
                ><i class="fa-solid fa-users-gear" style="color: #0ea5e9"></i
              ></span>
              <span class="skill-name">UX Design</span>
            </div>
            <div class="skill-footer">
              <div class="progress-bar" style="width: 90%"></div>
              <span class="skill-percentage">90%</span>
            </div>
          </div>
          <!-- Responsive Design -->
          <div class="skill">
            <div class="skill-header">
              <span class="skill-icon"
                ><i
                  class="fa-solid fa-mobile-screen-button"
                  style="color: #10b981"
                ></i
              ></span>
              <span class="skill-name">Responsive Design</span>
            </div>
            <div class="skill-footer">
              <div class="progress-bar" style="width: 95%"></div>
              <span class="skill-percentage">95%</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- ///////////   footer 🔴 //////////// -->

    <section class="footer">
      <div style="width: 100%">
        <h2 class="title-section" id="Contact">Contact</h2>
        <p style="margin-bottom: 10px">Fill the form to connect.</p>
      </div>

      <form
        action="https://formspree.io/f/xbdpvqge"
        method="POST"
        class="Contact"
      >
        <div class="text-form">
          <h2>Send a Message</h2>
          <p>
            Have a project in mind or want to discuss potential opportunities?
            Feel free to reach out.
          </p>
        </div>
        <span class="inputs-group">
          <input
            class="al-input"
            required
            type="text"
            name="username"
            minlength="2"
            maxlength="30"
            placeholder="Name"
          />
          <input
            name="email"
            minlength="3"
            maxlength="40"
            type="email"
            required
            placeholder="Email"
          />
        </span>

        <textarea
          required
          minlength="5"
          placeholder="Your Message"
          name="Message"
        ></textarea>
        <br />

        <div class="btn-form">
          <button type="submit">
            <span class="IconBtnForm">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="lucide lucide-send mr-2 h-4 w-4"
              >
                <path
                  d="M14.536 21.686a.5.5 0 0 0 .937-.024l6.5-19a.496.496 0 0 0-.635-.635l-19 6.5a.5.5 0 0 0-.024.937l7.93 3.18a2 2 0 0 1 1.112 1.11z"
                ></path>
                <path d="m21.854 2.147-10.94 10.939"></path>
              </svg>
            </span>
            Send Message
          </button>
        </div>
      </form>

      <div class="Contactme">
        <div class="email e-l-p">
          <div class="icon-contactme">
            <i class="fa-regular fa-envelope"></i>
          </div>
          <div class="e-l-p-text">
            <span class="title-contactme">Email</span>
            <a
              target="_blank"
              href="mailto:thehamzagamal@gmail.com"
              class="data-contactme"
              >thehamzagamal@gmail.com</a
            >
          </div>
        </div>

        <div class="Location e-l-p">
          <div class="icon-contactme">
            <i class="fa-brands fa-whatsapp"></i>
          </div>
          <div class="e-l-p-text">
            <span class="title-contactme">WhatsApp</span>
            <a
              target="_blank"
              href="https://wa.me/201121904745"
              class="data-contactme"
              >Chat on WhatsApp</a
            >
          </div>
        </div>

        <div class="phone e-l-p">
          <div class="icon-contactme">
            <i class="fa-solid fa-location-dot"></i>
          </div>
          <div class="e-l-p-text">
            <span class="title-contactme">Location</span>
            <span class="data-contactme">Cairo, Egypt</span>
          </div>
        </div>
      </div>
    </section>
    <!--  ///////////////////    footer 🔴    ////////////////////// -->
    <footer>
      <div class="footer-container">
        <div class="footer-row-top">
          <div class="logo-box">
            <a href="https://hamza-gamal.github.io/portfolio/">
              <img
                class="logo-image-footer"
                src="images/logo-white.png"
                alt="logo"
              />
            </a>
            <a
              class="title-logo"
              href="https://hamza-gamal.github.io/portfolio/"
              >Hamza Gamal</a
            >
          </div>

          <div class="social-box">
            <a
              data-tooltip="GitHub"
              class="icon-footer"
              target="_blank"
              href="https://github.com/hamza-gamal"
              ><i class="fa-brands fa-github"></i
            ></a>
            <a
              data-tooltip="Youtube"
              class="icon-footer"
              target="_blank"
              href="https://www.youtube.com/@HamzaGamalDev"
              ><i class="fa-brands fa-youtube"></i
            ></a>
            <a
              data-tooltip="LinkedIn"
              class="icon-footer"
              target="_blank"
              href="https://www.linkedin.com/in/HamzaGamalDev/"
              ><i class="fa-brands fa-linkedin"></i
            ></a>
            <a
              data-tooltip="Instagram"
              class="icon-footer"
              target="_blank"
              href="https://www.instagram.com/hamzagamaldev"
              ><i class="fa-brands fa-instagram"></i
            ></a>
            <a
              data-tooltip="Tiktok"
              class="icon-footer"
              target="_blank"
              href="https://www.tiktok.com/@hamzagamaldev"
              ><i class="fa-brands fa-tiktok"></i
            ></a>
          </div>
        </div>

        <div class="footer-row-bottom">
          <p class="footer-caption">
            Frontend Developer | student | Programming engineer
          </p>
          <span class="footer-caption">Made by Hamza Gamal © 2025 - 2026</span>
        </div>
      </div>
    </footer>
    <a href="#" class="btn-back-to-top">
      <!-- <img class="image-logo" src="images/logo-white.png" alt="logo" /> -->
      ↑
      <!-- <i class="fa-notdog-duo fa-solid fa-arrow-up"></i> -->
    </a>
    <div id="toast"></div>
    <script src="script.js"></script>
  </body>
</html>
