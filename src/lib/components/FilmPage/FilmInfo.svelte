<div class="container mx-auto">
	<div class="film-info">
		<div class="film-info__details">
			<h1>ПО СООБРАЖЕНИЯМ СОВЕСТИ</h1>
			<div>
				<div>
					<b>Год: </b>2016
				</div>
				<div>
					<b>Жанр: </b>биография, военный, драма, история
				</div>
				<div>
					<b>Страна: </b>Австралия, США, Великобритания, Китай
				</div>
				<div>
					<b>Режиссер: </b>Мэл Гибсон
				</div>
			</div>
			<div class="film-info__description">
				Восхождение циника-гедониста на бизнес-олимп 1980-х. Блистательный тандем Леонардо ДиКаприо
				и Мартина Скорсезе
			</div>
			<div class="film-info__rate">
				<div class="flex items-center gap-2"><img src="/icons/kp.svg" alt="kp" /> 7.1</div>
				<div class="flex items-center gap-2"><img src="/icons/imdb.svg" alt="kp" /> 7.1</div>
			</div>
		</div>
		<div class="film-info__img">
			<img src="/images/film-bg.png" alt="film-name" />
		</div>
	</div>
</div>

<style lang="scss">
	.film-info {
		display: grid;
		grid-template-columns: 40% 60%;
		padding: 65px 0;
		@media (max-width: theme('screens.desktop')) {
			display: flex;
			flex-direction: column-reverse;
			gap: 50px;
			padding: 30px 0;
		}
	}
	.film-info__details {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		font-size: 18px;
		padding-right: 50px;
		@media (max-width: theme('screens.desktop')) {
			gap: 30px;
		}
	}
	.film-info__rate {
		display: flex;
		align-items: center;
		gap: 30px;
	}
	.film-info__img {
		border-radius: 20px;
		overflow: hidden;
		img {
			width: 100%;
		}
	}
</style>
