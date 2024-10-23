<script lang="ts">
	import * as images from '../image';

	interface TypeQuiz {
		id: number;
		name: string;
		imageUrl: 'chemistry' | 'biology';
		questions: {
			id: number;
			text: string;
			answer: string;
			options: { id: number; text: string; lable: string }[];
		}[];
	}

	export let quiz: TypeQuiz;
</script>

<div class="quiz-card shadow w-[250px] rounded overflow-hidden cursor-pointer m-2">
	<img class="h-44" src={images[quiz.imageUrl]} alt="" />
	<div class="flex items-center justify-between py-3 px-2">
		<h1 class="font-bold">{quiz.name}</h1>
		<p>{quiz.questions.length} questions</p>
	</div>
</div>
