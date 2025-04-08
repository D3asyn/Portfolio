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
			desc: 'szamologép',
			date: '2024-10-10',
			link: 'https://d3asyn.github.io/Calculator/'
		},
		{
			name: 'New Animation',
			desc: 'Animation balls bouncing',
			date: '2024-12-5',
			link: 'https://animationd3.netlify.app/'
		},
		{
			name: 'Minesweeper',
			desc: 'Minweeper game',
			date: '2024-12-18',
			link: 'https://d3asyn.github.io/minesweeper/'
		},
		{
			name: 'Calendar',
			desc: 'WeeklyCalendar',
			date: '2025-3-05',
			link: 'https://d3asyncalendar.netlify.app/'
		},
		{
			name: "Nine men's morris",
			desc: 'Malom',
			date: '2025-3-06',
			link: 'https://github.com/D3asyn/NIne'
		},
		{
			name: 'AuthAndCrud',
			desc: 'AuthAndCrud',
			date: '2025-3-12',
			link: 'https://authandcrudd3asyn.netlify.app/profile/login'
		}
	];

	const colors = ['love', 'gold'];
</script>

<div class="title">
	<h1>My Projects</h1>
</div>

<table class="styled-table">
	<thead class="love">
		<tr>
			<th>Project Name</th>
			<th>Description</th>
			<th>Date</th>
			<th>Link</th>
		</tr>
	</thead>
	<tbody>
		{#each projects as project}
			<tr>
				<td>{project.name}</td>
				<td>{project.desc}</td>
				<td>{project.date}</td>
				<td><a href={project.link} target="_blank">View Project</a></td>
			</tr>
		{/each}
	</tbody>
</table>

<style>
	.title h1 {
		text-align: center;
		color: #f6c177;
		margin-bottom: 20px;
	}

	th {
		background-color: #ebbcba;
	}

	.styled-table {
		width: 90%;
		margin: 0 auto;
		border-collapse: collapse;
		box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
		background-color: #191724;
		color: #ebbcba;
	}

	.styled-table th,
	.styled-table td {
		padding: 12px;
		text-align: left;
		border: 1px solid #ddd;
	}

	.styled-table th {
		background-color: #ebbcba;
		color: black;
	}

	.styled-table tr:nth-child(even) {
		background-color: #2a2a2a;
	}

	.styled-table tr:hover {
		background-color: #444;
	}

	a {
		color: #f6c177;
		text-decoration: none;
	}

	a:hover {
		text-decoration: underline;
	}
</style>
