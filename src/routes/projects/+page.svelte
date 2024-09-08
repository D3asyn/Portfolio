<script>
	let projects = [{ name: 'Elso Ora', date: '2024-09-05', link: 'https://d3asyn.github.io/95/' }];

	const colors = ['love', 'gold'];
</script>

<div class="table">
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
</div>

<style>
	table {
		border-collapse: collapse;
		width: 60%;
		margin: auto;
		background-color: #f6c177;
		box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
	}

	th,
	td {
		padding: 12px;
		text-align: left;
		border-bottom: 1px solid #3e8fb0;
	}

	th {
		background-color: #ebbcba;
		color: #232136;
	}

	a {
		color: #232136;
		text-decoration: none;
	}

	a:hover {
		text-decoration: underline;
	}
</style>
