React server components

- Способ рендерить содержимое на сервере и стримить его на клиент без последующей гидрации
- В отличие от [[SSR]] стримит HTML-статику не только при первом запросе, но и при дальнейшей навигации
- Индексируется поисковиками

RSC - компоненты , которые рендерятся только на сервере и только 1 раз!

Пример:
~~~jsx
async function MoviesPage() {
	const movies = await getMoviesFromServer()
	
	return (
		<ul>
			{
				movies.map((movie) => (
					<li key={movie.id}>
						{movie.name}
					</li>
				))
			}
		</ul>
	)
}

export default MoviesPage;
~~~



[[React]] [[Next]] 