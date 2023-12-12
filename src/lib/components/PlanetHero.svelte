<!-- Rotating planet with text and rings around it -->
<section>
	<div class="galaxy">
		<img class="planet" src="images/planet.svg" alt="" />
		<!-- <img class="rings" src="images/rings.svg" alt="" /> -->

		<!-- <svg
			viewBox="0 0 300 300"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
            id="heroText"
		>
			<path
				id="curve"
				fill="none"
				stroke="none"
				d="M 32.550491,148.48008 A -108.15144,-108.15144 0 0 1 140.70194,40.328644 -108.15144,-108.15144 0 0 1 248.85338,148.48008 -108.15144,-108.15144 0 0 1 140.70194,256.63153 -108.15144,-108.15144 0 0 1 32.550491,148.48008 Z"
			/>
			<text fill="#000000" letter-spacing="6" font-weight="bold">
				<textPath xlink:href="#curve" startOffset="25"
					>The Coding Galaxy</textPath
				>
			</text>
		</svg> -->

		<!-- <img src="images/heroText.svg" alt=""> -->
        <div class="title">
            <span>T</span>
            <span>H</span>
            <span>E</span>
            <span>&nbsp;</span>
            <span>C</span>
            <span>O</span>
            <span>D</span>
            <span>I</span>
            <span>N</span>
            <span>G</span>
            <span>&nbsp;</span>
            <span>G</span>
            <span>A</span>
            <span>L</span>
            <span>A</span>
            <span>X</span>
            <span>Y</span>
        </div>

        <!-- <img class="underring" src="images/underring.svg" alt=""> -->
        <img class="rings" src="images/fullrings.svg" alt="">
	</div>
</section>

<style>
	section {
		width: 100%;
		height: 100vh;
        position: relative;
	}

	.galaxy {
		display: flex;
		position: relative;
		justify-content: center;
		align-items: center;
		overflow: hidden;
	}

	.planet {
		position: absolute;
		animation: orbit 90s linear infinite;
		width: 15rem;
		height: 15rem;
	}

	.rings {
		width: 38rem;
		height: 38rem;
	}

    .underring {
        position: absolute;
        width: 18rem;
		height: 18rem;
    }

    .title {
        position: absolute;
        width: 50px;
        margin: 0 auto;
        font-size: 70px;
    }

    .title span {
        font-size: 56px;
        font-weight: bold;
        font-family: var(--title-font);
        color: var(--primary-white);
        -webkit-text-stroke: 1px var(--primary-black);
        /* border: solid 1px var(--primary-black); */
        text-shadow: 0px 4px 0px #090909 !important;
        position: absolute;
        bottom: 0;
        left: 50%;
        width: 35px;
        height: 150px;
        margin-left: -17px;
        line-height: 10px;
        text-align: center;
        transform-origin: bottom center;
    }

    .title span:nth-child(1) {
        transform: rotate(-75deg);
        text-shadow: -3px 2px 0px #090909;
    }

    .title span:nth-child(2) {
        transform: rotate(-65deg);
        text-shadow: -3px 2px 0px #090909;
    }

    .title span:nth-child(3) {
        transform: rotate(-55deg);
        text-shadow: -3px 2px 0px #090909;
    }

    .title span:nth-child(4) {
        transform: rotate(-50deg);
    }

    .title span:nth-child(5) {
        transform: rotate(-40deg);
        text-shadow: -2px 2px 0px #090909;
    }

    .title span:nth-child(6) {
        transform: rotate(-30deg);
        text-shadow: -1px 2px 0px #090909;
    }

    .title span:nth-child(7) {
        transform: rotate(-20deg);
        text-shadow: -1px 2px 0px #090909;
    }

    .title span:nth-child(8) {
        transform: rotate(-10deg);
        text-shadow: 0px 2px 0px #090909;
    }

    .title span:nth-child(9) {
        transform: rotate(0deg);
        text-shadow: 0px 2px 0px #090909;
    }

    .title span:nth-child(10) {
        transform: rotate(10deg);
        text-shadow: 0px 2px 0px #090909;
    }

    .title span:nth-child(11) {
        transform: rotate(15deg);
    }

    .title span:nth-child(12) {
        transform: rotate(25deg);
        text-shadow: 2px 2px 0px #090909;
    }

    .title span:nth-child(13) {
        transform: rotate(35deg);
        text-shadow: 2px 2px 0px #090909;
    }

    .title span:nth-child(14) {
        transform: rotate(45deg);
        text-shadow: 2px 2px 0px #090909;
    }

    .title span:nth-child(15) {
        transform: rotate(55deg);
        text-shadow: 2px 2px 0px #090909;
    }

    .title span:nth-child(16) {
        transform: rotate(65deg);
        text-shadow: 2px 2px 0px #090909;
    }

    .title span:nth-child(17) {
        transform: rotate(75deg);
        text-shadow: 2px 2px 0px #090909;
    }

	/* #heroText {
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 1;
    }

	path {
		fill: transparent;
	}

	text {
		position: absolute;
		font-weight: bold;
		font-size: 2rem;
		fill: var(--primary-black);
		font-family: var(--title-font);
	} */

	@keyframes orbit {
		0% {
			transform: rotate(0deg);
		}
		100% {
			transform: rotate(360deg);
		}
	}
</style>
