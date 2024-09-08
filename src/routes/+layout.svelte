<body>
	<wrapper>
		<header>
			<nav>
				<ul>
					<li><h1 class="typewriter">D3asyn</h1></li>
					<li>
						<a href="/Portfolio">Home</a>
					</li>
					<li>
						<a href="/Portfolio/about">About</a>
					</li>
					<li>
						<a href="/Portfolio/projects">Projects</a>
					</li>
				</ul>
			</nav>
		</header>
		<body>
			<wrapper>
				<br />
				<br />
				<slot></slot>
				<br />
				<br />
			</wrapper>
		</body>
		<div class="footer love">
			<p>&copy; 2024 D3asny <br />All rights reserved.</p>
		</div>
	</wrapper>
</body>

<style>
	:global(body) {
		background: #191724;
		margin: 0;
		padding: 0;
		font-family: Arial, sans-serif;
	}
	wrapper {
		display: flex;
		flex-direction: column;
		min-height: 86.3vh;
	}
	:global(.base) {
		background-color: #191724;
		color: #eb6f92;
	}

	:global(.love) {
		background-color: #eb6f92;
		color: #191724;
	}

	:global(.gold) {
		background-color: #f6c177;
		color: #191724;
	}
	:global(.rose) {
		background-color: #ebbcba;
		color: #191724;
	}

	:global(.pine) {
		background-color: #31748f;
		color: #f6c177;
	}

	:global(.foam) {
		background-color: #9ccfd8;
		color: #191724;
	}
	:global(.iris) {
		background-color: #c4a7e7;
		color: #191724;
	}
	.typewriter {
		color: #191724;
		border-right: #191724 2px solid;
		animation: blink 0.75s step-end infinite;
	}

	@keyframes blink {
		50% {
			border-color: transparent;
		}
	}

	header {
		width: 100%;
		padding: 10px;
		background-color: #eb6f92;
	}

	ul {
		margin: 0;
		padding: 0;
		display: flex;
		gap: 1rem;
		list-style: none;
	}

	a {
		display: block;
		padding-inline: 20px;
		padding-block: 25px;
		color: #eb6f92;
		background: #191724;
		text-decoration: none;
		transition: color 0.2s ease-in-out;
		border-radius: 0.5rem;
	}

	a:hover {
		color: #f6c177;
	}
	.footer {
		text-align: center;
		background-color: #eb6f92;
		color: #232136;
	}
</style>
