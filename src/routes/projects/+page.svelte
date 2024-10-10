<script>
	let projects = [
		{
			name: 'Elso Ora',
			desc: 'Elso orai gyakorlas',
			date: '2024-09-05',
			link: 'https://d3asyn.github.io/95/'
		},
		{
			name: 'Masodik Ora',
			desc: 'Javascript addNumber()',
			date: '2024-09-11',
			link: 'https://d3asyn.github.io/911/'
		},
		{
			name: 'Harmadik Ora',
			desc: 'svelte orai project',
			date: '2024-09-12',
			link: 'https://d3asyn.github.io/svelteora/'
		},
		{
			name: 'Node.js',
			desc: 'node proba',
			date: '2024-09-12',
			link: 'https://github.com/D3asyn/node912'
		},
		{
			name: 'Fetch',
			desc: 'fetching json',
			date: '2024-09-18',
			link: 'https://d3asyn.github.io/918/'
		},
		{
			name: 'Todo list',
			desc: 'Todo list local storage',
			date: '2024-09-19',
			link: 'https://d3asyn.github.io/103/'
		},
		{
			name: 'Json orarend',
			desc: 'Svelte orarend json',
			date: '2024-09-25',
			link: 'https://d3asyn.github.io/orarendszft/'
		},
		{
			name: 'Dvd',
			desc: 'Bouncing dvd logo',
			date: '2024-10-03',
			link: 'https://d3asyn.github.io/dvd/'
		},
		{
			name: 'WheaterForecast',
			desc: 'Long és Lat alapú időjárás',
			date: '2024-10-09',
			link: 'https://d3asyn.github.io/WeatherForecast/'
		},
		{
			name: 'Calculator',
			desc: 'szamitogep',
			date: '2024-10-10',
			link: 'https://d3asyn.github.io/Calculator/'
		}
];

	const colors = ['love', 'gold'];
</script>

<div class="table">
	<table>
		<thead>
			<tr>
				<th>Project Name</th>
				<th>Date</th>
				<th>Description</th>
				<th>Link</th>
			</tr>
		</thead>
		<tbody>
			{#each projects as project, index}
				<tr class={colors[index % colors.length]}>
					<td>{project.name}</td>
					<td>{project.date}</td>
					<td>{project.desc}</td>
					<td style="text-align: center;"><a href={project.link} target="_blank">View</a></td>
				</tr>
			{/each}
		</tbody>
	</table>
</div>

<style>
	table {
		border-collapse: collapse;
		width: 90%;
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
		padding: 10px;
		color: #eb6f92;
		background: #191724;
		text-decoration: none;
		transition: color 0.2s ease-in-out;
		border-radius: 0.5rem;
	}

	a:hover {
		color: #f6c177;
	}
</style>
