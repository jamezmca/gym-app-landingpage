<script>
    import ProductCard from "./ProductCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    let productFeatures = [
        {
            featureList: [
                "Daily streak counter",
                "Weights and reps tracker",
                "Community challenges",
                "Every workout is new and exciting",
            ],
            description:
                "Swoley moley ensures all users have the information they need to train safely and train effectively.",
            imgUrl: "assets/selection.png",
        },
        {
            featureList: [
                "Select your preferences",
                "Personalize your workouts",
                "Customize your training",
                "Guarantees progress on all core exercises",
            ],
            description:
                "Build you streaks and see your progress with our amazing tracking and analytics features.",
            imgUrl: "assets/training.png",
        },
        {
            featureList: [
                "Eliminating guesswork",
                "Save time",
                "Achieve the performance you seek",
                "Builds functional strength",
            ],
            description:
                "Enter as much information about yourself as you desire to ensure all workouts are personalized to your every need.",
            imgUrl: "assets/goal.png",
        },
    ];
</script>

<SectionWrapper id="product">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                Start your lifetime <span class="text-indigo-400"
                    >gym streak</span
                > today
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                Features For Everyone
            </h3>
        </div>

        {#each productFeatures as productFeature, index}
            <ProductCard {productFeature} {index}>
                {#if index === 0}
                    Experience a beginner exercise <span
                        class="text-indigo-400 font-medium">master</span
                    > class
                {:else if index === 1}
                    Lay the foundations for <span
                        class="text-indigo-400 font-medium">routine</span
                    > and consistency
                {:else}
                    Workouts specific to your <span
                        class="text-indigo-400 font-medium">environment</span
                    >
                    and
                    <span class="text-indigo-400 font-medium">expertise</span>
                {/if}
            </ProductCard>
        {/each}
    </div>
</SectionWrapper>
