<script>
    import Blob from "./Blob.svelte";
</script>

<!-- Rotating planet with text and rings around it -->
<section>
	<div class="galaxy">
		<img class="planet" src="images/planet.svg" alt="" />

		<h1 class="title">
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
		</h1>

		<img class="rings" src="images/fullrings.svg" alt="" />
        <Blob topAbsolute={"5rem"} leftAbsolute={"8rem"}/>
	</div>

    <div class="blobs">
        <Blob bottomAbsolute={"9rem"} rightAbsolute={"-1.5rem"} blobWidth={"155px"} rotateBlob={"180deg"}/>
        <Blob bottomAbsolute={"0.5rem"} leftAbsolute={"-5rem"} blobWidth={"180px"} rotateBlob={"180deg"}/>
    </div>


	<a href="#posts">Launch</a>
</section>

<style>
	section {
		position: relative;
		width: 100%;
		height: 100dvh;
        overflow-x: hidden;
	}

	.galaxy {
		display: flex;
		position: absolute;
		justify-content: center;
		align-items: center;
		overflow: hidden;
        left: 50%;
        top: 20%;
        transform: translate(-50%, -28%);
	}

    .blobs{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        overflow: hidden;
    }

	.planet {
		position: absolute;
		animation: orbit 90s linear infinite;
		width: 15rem;
		height: 15rem;
        z-index: 1;
	}

	.rings {
		width: 38rem;
		height: 38rem;
	}

	.title {
		position: absolute;
		margin: 0 auto;
		width: 50px;
		font-size: 70px;
        z-index: 1;
	}

	.title span {
		color: var(--primary-white);
		font-weight: bold;
		font-size: 56px;
		font-family: var(--title-font);
		-webkit-text-stroke: 1px var(--primary-black);
		position: absolute;
		bottom: 0;
		left: 50%;
		transform-origin: bottom center;
		margin-left: -17px;
		width: 35px;
		height: 150px;
		line-height: 10px;
		text-align: center;
		/* border: solid 1px var(--primary-black); */
		text-shadow: 0px 4px 0px #090909 !important;
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

	@keyframes orbit {
		0% {
			transform: rotate(0deg);
		}
		100% {
			transform: rotate(360deg);
		}
	}

	a {
		position: absolute;
		bottom: 5rem;
		left: 50%;
		transform: translateX(-50%);
		border: none;
		border-radius: 10px;
		background: transparent;
		/* width: 200px; */
		height: 50px;
		color: var(--primary-black);
		font-size: 1.3rem;
		font-family: var(--body-font);
		letter-spacing: 3px;
		text-transform: uppercase;
        font-weight: 100;
        transition: font-size 0.2s ease-in-out;
	}

    a:hover {
        font-size: 1.5rem;
        cursor: pointer;
    }

    a::after {
        content: '';
        position: absolute;
        bottom: -50px;
        left: 49%;
        transform: translateX(-49%);
        width: 1px;
        height: 45px;
        background: var(--primary-black);
        animation: pulse 3s ease-in-out infinite;
    }

    @keyframes pulse {
        0% {
            bottom: -40px;
            /* height: 50px; */
        }
        50% {
            bottom: -60px;
            /* height: 35px; */
        }
        100% {
            bottom: -40px;
            /* height: 50px; */
        }
    }
</style>
