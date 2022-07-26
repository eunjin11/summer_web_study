<script context="module" lang="ts" style="margin: 0;">
	export const prerender = true;
	const keyword_item: string[] = [
		'지구한바퀴 세계여행',
		'그림 웹툰',
		'시사 이슈',
		'IT 트렌드',
		'사진 촬영',
		'취향저격 영화 리뷰',
		'오늘은 이런 책',
		'뮤직 인사이드',
		'글쓰기 코치',
		'직장인 현실 조언',
		'스타트업 경험담',
		'육아 이야기',
		'요리 레시피',
		'건강 운동',
		'멘탈 관리 심리 탐구',
		'디자인 스토리',
		'문화 예술',
		'건축 설계',
		'인문학 철학',
		'쉽게 읽는 역사',
		'우리집 반려동물',
		'멋진 캘리그래피',
		'사랑 이별',
		'감성 에세이'
	];
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section style="margin: 0;">
	<!--<Counter />-->
	<head>
		<title>글이 작품이 되는 공간, 브런치</title>

		<!--<link rel="stylesheet" href="style.css" />-->
	</head>
	<body style="margin: 0;">
		<div class="banner" style="text-align: center;">
			<!-- svelte-ignore a11y-missing-attribute -->
			<img
				style="margin: 0 auto;"
				src="https://t1.daumcdn.net/section/oc/d27ae25db6cb4f3da246edc8365b76ae"
				height="60px"
				width="960px"
			/>
		</div>

		<div style="width: 100%; height: 40px;" />

		<span class="menu_button" />

		<span class="logo" />

		<span class="search" />

		<span class="start"> 시작하기 </span>

		<div class="text">글이 작품이 되는 공간, 브런치</div>

		<div class="text2">브런치에 담긴 아름다운 작품을 감상해 보세요.</div>
		<div class="text2">그리고 다시 꺼내보세요.</div>
		<div class="text2" style="color: #DADADA;">서랍 속 간직하고 있는 그 글과 감성을.</div>

		<div
			style="width: 100%; height: 30px; text-align: right; float:right;
        margin-top: 20px; margin-right: 300px;
        "
		>
			<span
				style=" color: #00c3bd;
            font-family: Georgia,sans-serif;
            font-size: 11px;
            font-style: italic;
            padding-top: 2px;">update</span
			>

			<span
				style="color: #959595;
            font-size: 12px;
            padding-left: 7px;"
			>
				글쓰기 알림 설정 추가 안내</span
			>
		</div>

		<div style="width: 100%; height: 50px;" />

		<div class="editor_pic">
			<span
				class="item"
				style="
            background-color: white;
            height: 520px;
            display: inline-block;
            "
			/>

			<span
				class="item"
				style="
            height: 520px;
            width: 480px;
            display: inline-block;
            background-image: url(https://img1.daumcdn.net/thumb/C520x520.fjpg/?fname=https://t1.daumcdn.net/section/oc/b89ecf2a54bc4184b7409ad3e6c9f0f9);
            "
			>
				<span class="item_text" />
			</span>

			<span
				class="item"
				style="
            background-image: url(https://img1.daumcdn.net/thumb/C480x260.fjpg/?fname=https://t1.daumcdn.net/section/oc/436a3849cb8c47bab812419b26069e49);
            height: 260px;
            width: 480px;
            display: inline-block;
            "
			>
				<span class="item_text" />
			</span>

			<span
				class="item"
				style="
            background: url(https://img1.daumcdn.net/thumb/C320x520.fjpg/?fname=https://t1.daumcdn.net/section/oc/f13313f7e28f4e3a904edca4d9b63174);
            height: 520px;
            width:auto;
            display: inline-block;
            "
			>
				<span class="item_text" />
			</span>

			<span
				class="item"
				style="
            background-image: url(https://img1.daumcdn.net/thumb/C480x260/?fname=http://t1.daumcdn.net/brunch/service/user/3b5L/image/STmlrEyvqD1Ca8UrlwR43uVYMKQ.png);
            display: inline-block;
            "
			>
				<span class="item_text" />
			</span>
		</div>

		<div class="number_menu" />

		<div class="brunch_keyword" />

		<div class="brunch_keyword_text" />

		<div class="keyword_container">
			{#each keyword_item as keyword}
				<div class="keyword_item">
					<div class="keyword_text">{keyword}</div>
				</div>
			{/each}
		</div>

		<div class="brunch_writers">
			<div class="brunch_writer" />

			<div class="brunch_writer_recommend" />

			<div style="margin-top: 42px;" />

			<span style="margin-left: 43%; margin-bottom: 100px;">
				<span class="writer_button"> 결혼 </span>
				<span class="writer_button"> 요리 </span>
				<span class="writer_button"> 사진 </span>
			</span>

			<div style="margin-top: 42px;" />

			<div class="writer_list">
				<div class="writers">
					<div class="writer_img">
						<!-- svelte-ignore a11y-missing-attribute -->
						<img
							src="https://img1.daumcdn.net/thumb/C120x120/?fname=http://t1.daumcdn.net/brunch/service/user/2hny/image/YDNI6dK5ZhizFaW5F96DKhPSWqw.png"
							width="80"
							height="80"
						/>
					</div>
					<div class="writer_name">리즈</div>
					<div class="writer_job">여행작가</div>
					<div class="writer_explain">
						나 오늘이 있으니 그대가 있으니 정말 고마워, 고마워... - 리즈의 때로 사진, 때로 여행~
					</div>
				</div>
				<div class="writers">
					<div class="writer_img">
						<!-- svelte-ignore a11y-missing-attribute -->
						<img
							src="https://img1.daumcdn.net/thumb/C120x120/?fname=http://t1.daumcdn.net/brunch/service/user/2ALn/image/40yeTbORc0hM1Yu_8r1qRdYiRUM.jpg"
							width="80"
							height="80"
						/>
					</div>
					<div class="writer_name">뚜윤</div>
					<div class="writer_job">크리에이터</div>
					<div class="writer_explain">
						반갑습니다! 인생을 여행으로 만들며 뚜벅뚜벅 걸어가고 있는 뚜윤입니다:)
					</div>
				</div>
				<div class="writers">
					<div class="writer_img">
						<!-- svelte-ignore a11y-missing-attribute -->
						<img
							src="https://img1.daumcdn.net/thumb/C120x120/?fname=http://t1.daumcdn.net/brunch/service/user/2hny/image/YDNI6dK5ZhizFaW5F96DKhPSWqw.png"
							width="80"
							height="80"
						/>
					</div>
					<div class="writer_name">리즈</div>
					<div class="writer_job">여행작가</div>
					<div class="writer_explain">
						나 오늘이 있으니 그대가 있으니 정말 고마워, 고마워... - 리즈의 때로 사진, 때로 여행~
					</div>
				</div>
				<div class="writers">
					<div class="writer_img">
						<!-- svelte-ignore a11y-missing-attribute -->
						<img
							src="https://img1.daumcdn.net/thumb/C120x120/?fname=http://t1.daumcdn.net/brunch/service/user/2hny/image/YDNI6dK5ZhizFaW5F96DKhPSWqw.png"
							width="80"
							height="80"
						/>
					</div>
					<div class="writer_name">리즈</div>
					<div class="writer_job">여행작가</div>
					<div class="writer_explain">
						나 오늘이 있으니 그대가 있으니 정말 고마워, 고마워... - 리즈의 때로 사진, 때로 여행~
					</div>
				</div>
				<div class="writers">
					<div class="writer_img">
						<!-- svelte-ignore a11y-missing-attribute -->
						<img
							src="https://img1.daumcdn.net/thumb/C120x120/?fname=http://t1.daumcdn.net/brunch/service/user/2hny/image/YDNI6dK5ZhizFaW5F96DKhPSWqw.png"
							width="80"
							height="80"
						/>
					</div>
					<div class="writer_name">리즈</div>
					<div class="writer_job">여행작가</div>
					<div class="writer_explain">
						나 오늘이 있으니 그대가 있으니 정말 고마워, 고마워... - 리즈의 때로 사진, 때로 여행~
					</div>
				</div>
				<div class="writers">
					<div class="writer_img">
						<!-- svelte-ignore a11y-missing-attribute -->
						<img
							src="https://img1.daumcdn.net/thumb/C120x120/?fname=http://t1.daumcdn.net/brunch/service/user/2hny/image/YDNI6dK5ZhizFaW5F96DKhPSWqw.png"
							width="80"
							height="80"
						/>
					</div>
					<div class="writer_name">리즈</div>
					<div class="writer_job">여행작가</div>
					<div class="writer_explain">
						나 오늘이 있으니 그대가 있으니 정말 고마워, 고마워... - 리즈의 때로 사진, 때로 여행~
					</div>
				</div>
			</div>
		</div>

		<div class="writer_application">
			<!-- svelte-ignore a11y-missing-attribute -->
			<img src="https://t1.daumcdn.net/brunch/static/test/new_pc_top/5.png" />
		</div>

		<div class="recommended_article" />

		<div class="recommended_article_text" />

		<div class="black_banner">
			<div class="under_banner_list">
				<div class="under_banner_item">브런치 이용안내</div>
				<div class="under_banner_item">이용약관</div>
				<div class="under_banner_item">브런치팀 공지사항</div>
				<div class="under_banner_item">작가신청</div>
				<div class="under_banner_item">이전 이용약관</div>
				<div class="under_banner_item">브런치 카카오톡 채널</div>
				<div class="under_banner_item">작가 지원 프로젝트</div>
				<div class="under_banner_item" id="kakao">카카오 개인정보 처리방침</div>
				<div class="under_banner_item">브런치 인스타그램</div>
				<div class="under_banner_item" />
				<div class="under_banner_item">제휴제안</div>
				<div class="under_banner_item">브런치 페이스북</div>
				<div class="under_banner_item">청소년 보호정책</div>
				<div class="under_banner_item">고객센터</div>
				<div class="under_banner_item" />
				<div class="under_banner_item">운영정책</div>
				<div class="under_banner_item" />
				<div class="under_banner_item" />
			</div>
		</div>
	</body>
</section>

<style>
	@import url(//fonts.googleapis.com/earlyaccess/nanummyeongjo.css);

	.head {
		margin: 0px;
	}

	.menu_button {
		background: url(https://t1.daumcdn.net/brunch/static/img/help/pc/ico_view_cover.v4.png);
		display: inline-block;
		height: 22px;
		margin-right: 5px;
		margin-left: 20px;
		width: 27px;
	}

	.logo {
		background: url(https://t1.daumcdn.net/brunch9/static/images/pc/logo_brunch_v1.png);
		width: 72px;
		display: inline-block;
		height: 22px;
	}

	.search {
		background: url(https://t1.daumcdn.net/brunch/static/img/help/pc/ico_view_cover.v4.png);
		margin: 0 0 0 16px;
		margin-right: 30px;
		float: right;

		background-position: -30px 0;
		width: 22px;
		height: 22px;
	}

	.start {
		border: 1px solid #959595;
		border-radius: 16px;
		color: #666;
		font-family: 'Noto Sans Light', sans-serif;
		font-size: 12px;
		height: 28px;
		line-height: 28px;
		margin-top: -5px;
		text-align: center;
		width: 64px;

		float: right;
	}

	.text {
		font-size: 40px;
		display: block;
		margin: 0 auto;
		padding-top: 10px;
		padding-bottom: 10px;
		width: 960px;
		text-align: left;
		font-family: 'Nanum Myeongjo', sans-serif;
		letter-spacing: -0.05em;
	}

	.text2 {
		font-size: 32px;
		color: #cacaca;
		display: block;
		margin: 0 auto;
		width: 960px;
		text-align: left;
		font-family: 'Nanum Myeongjo', sans-serif;
		letter-spacing: -0.05em;

		padding-bottom: 5px;
	}

	.banner {
		background-color: black;
	}

	.editor_pic {
		margin-top: 22px;
		width: 100%;
		/*그리드를 이용해보자.. 어떻게든*/
		display: grid;
		grid-template-rows: 260px 260px;
		grid-template-columns: auto 480px 480px auto;
		margin-bottom: 30px;
	}

	.number_menu {
		width: 192px;
		height: 12px;
		background: url(https://t1.daumcdn.net/brunch/static/img/help/pc/top/img_paging.v2.png);
		background-position: 0 -10px;

		margin-left: auto;
		margin-right: auto;
	}

	.brunch_keyword {
		background-image: url(https://t1.daumcdn.net/brunch9/static/images/pc/txt_brunch_v5_181004_v2.png);
		background-position: -101px -300px;

		height: 13px;
		margin-top: 142px;
		width: 266px;
		margin-left: auto;
		margin-right: auto;
	}

	.brunch_keyword_text {
		background-image: url(https://t1.daumcdn.net/brunch9/static/images/pc/txt_brunch_v5_181004_v2.png);
		background-position-x: 210px;

		height: 11px;

		width: 155px;
		margin-top: 15px;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50px;
	}

	.item:nth-child(1) {
		grid-row: 1/3;
	}

	.item:nth-child(2) {
		grid-row: 1/3;
	}

	.item_text {
		margin-top: 80px;
		display: block;
		font-family: 'Nanum Myeongjo', sans-serif;
		font-size: 28px;
		font-weight: normal;
		letter-spacing: -0.025em;
		line-height: 36px;
		padding-top: 12px;

		text-align: center;
	}

	.keyword_container {
		width: 968px;
		margin: auto;
		display: grid;
		grid-template-rows: repeat(3, 121px);
		grid-template-columns: repeat(8, 121px);
	}

	.keyword_text {
		top: 35%;
		position: relative;
		font-family: 'Noto Sans DemiLight', 'Malgun Gothic';
	}

	.keyword_item:hover {
		display: inline-block;
		border: 1px solid #00c3bd;
		color: #00c3bd;
	}
	.keyword_item {
		display: inline-block;
		border: 1px solid #eee;
		font-size: 14px;
		height: 119px;
		line-height: 18px;
		text-align: center;
		width: 119px;
		position: relative;
	}

	.brunch_writers {
		background-color: #fafafa;
		margin-top: 150px;
		padding-top: 100px;
		padding-bottom: 100px;
	}

	.brunch_writer {
		background-image: url(https://t1.daumcdn.net/brunch9/static/images/pc/txt_brunch_v5_181004_v2.png);

		background-position: 0 -175px;
		height: 13px;
		width: 258px;

		margin-left: auto;
		margin-right: auto;
	}

	.brunch_writer_recommend {
		background-image: url(https://t1.daumcdn.net/brunch9/static/images/pc/txt_brunch_v5_181004_v2.png);
		background-position: -270px -70px;
		height: 11px;
		margin-top: 15px;
		width: 84px;

		margin-left: auto;
		margin-right: auto;
	}

	.writer_button {
		background-color: #fff;
		border: 1px solid #eee;
		border-radius: 25px;
		color: #959595;
		display: inline-block;
		font-family: 'Noto Sans Light', 'Malgun Gothic';
		font-size: 15px;
		line-height: 18px;
		margin: 0 2px;
		overflow: hidden;
		padding: 7px 16px 6px;
	}

	.writer_list {
		width: 960px;
		height: 790px;
		margin: auto;
		display: grid;
		grid-template-rows: repeat(2, 1fr);
		grid-template-columns: repeat(3, 1fr);
	}

	.writers {
		background-color: white;
		width: 310px;
		height: 380px;
		border: 50px 50px;
	}

	/*html에서 serve를 하고 로컬호스트 주소로 들어가지 않으면
css적용이 안되던데 왜 그런지 궁금함
-링크 수정하니까 해결*/

	.writer_application {
		margin-top: 50px;
		margin-bottom: 50px;
		text-align: center;
	}

	.recommended_article {
		background-image: url(https://t1.daumcdn.net/brunch9/static/images/pc/txt_brunch_v5_181004_v2.png);

		background-position: 0 -225px;
		height: 13px;
		margin-top: 152px;
		width: 380px;

		margin-left: auto;
		margin-right: auto;
	}

	.recommended_article_text {
		background-image: url(https://t1.daumcdn.net/brunch9/static/images/pc/txt_brunch_v5_181004_v2.png);

		background-position: 0 -75px;
		height: 11px;
		margin-bottom: 47px;
		width: 162px;

		margin-top: 15px;
		margin-left: auto;
		margin-right: auto;
	}

	.writer_img {
		background-color: #fff;
		border-radius: 50%;
		overflow: hidden;
		display: inline-block;
		margin: 0 auto;
	}

	.writers {
		text-align: center;
	}

	.writer_img {
		margin-top: 40px;
	}

	.writer_name {
		word-wrap: break-word;
		font-family: 'Nanum Myeongjo', sans-serif;
		font-size: 20px;
		letter-spacing: -0.02em;
		line-height: 28px;
		max-height: 57px;
		padding: 17px 12px 0;
		white-space: normal;
		word-break: keep-all;
	}

	.writer_explain {
		-webkit-line-clamp: inherit;
		color: #959595;
		font-weight: 300;
		height: 60px;
		line-height: 20px;
		margin-top: 16px;
		opacity: 1;
		padding: 0;
		font-size: 12px;

		width: 230px;
		margin: 0 auto;
		margin-top: 16px;
	}

	.black_banner {
		padding-top: 48px;
		background-color: black;
		height: 380px;
	}

	.under_banner_list {
		display: grid;

		float: right;
		width: 960px;

		grid-template-rows: repeat(6, 34.8px);
		grid-template-columns: repeat(3, 232px);
	}

	.under_banner_item {
		color: #d9d9d9;
		font-size: 13px;
		font-weight: 300;
		letter-spacing: -0.02em;
		padding: 0;
		font-family: 'Noto Sans Light', sans-serif;
	}

	#kakao {
		color: #fff;
		font-family: 'Noto Sans Regular';
		font-size: 13px;
	}

	.under_banner_item:hover {
		color: white;
		text-decoration: underline;
	}
</style>
