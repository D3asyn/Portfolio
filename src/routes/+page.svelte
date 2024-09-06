<script>
	let projects = [{ name: 'Elso Ora', date: '2024-09-05', link: 'https://d3asyn.github.io/95/' }];

	const colors = ['red', 'orange'];
</script>

<body>
	<h1>Portfolio</h1>
	<table>
		<thead>
			<tr>
				<th>Project Name</th>
				<th>Date</th>
				<th>Link</th>
			</tr>
		</thead>
		<tbody>
			{#each projects as project, index}
				<tr class={colors[index % colors.length]}>
					<td>{project.name}</td>
					<td>{project.date}</td>
					<td><a href={project.link} target="_blank">View Project</a></td>
				</tr>
			{/each}
		</tbody>
	</table>
</body>

<style>
	:global(body) {
		background: aquamarine;
		margin: 0;
		padding: 0;
		font-family: Arial, sans-serif;
	}

	h1 {
		color: red;
		margin-bottom: 20px;
		text-align: center;
	}

	table {
		border-collapse: collapse;
		width: 60%;
		margin: auto;
		background-color: white;
		box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
	}

	th,
	td {
		padding: 12px;
		text-align: left;
		border-bottom: 1px solid #ddd;
	}

	th {
		background-color: #f2f2f2;
		color: red;
	}

	.red {
		background-color: red;
		color: white;
	}

	.orange {
		background-color: orange;
		color: white;
	}

	.aquamarine {
		background-color: aquamarine;
		color: black;
	}

	a {
		color: aquamarine;
		text-decoration: none;
	}

	a:hover {
		text-decoration: underline;
	}
</style>
