<script>
    import Container from "../../container.svelte";
    import Feature from "../features/feature.svelte";
    const featuresContent = [
        {
            title: "Web development",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores quae porro consequatur aliquam, incidunt eius magni provident",
            bg: "red",
        },
        {
            title: "UI Design",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores quae porro consequatur aliquam, incidunt eius magni provident",
            bg: "orange",
        },
        {
            title: "Interaction",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores quae porro consequatur aliquam, incidunt eius magni provident",
            bg: "red",
        },
        {
            title: "User Expereince",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores quae porro consequatur aliquam, incidunt eius magni provident",
            bg: "orange",
        },
    ];
</script>

<div class="text-center mt-16">
    <Container>
        <h2 class="text-3xl font-bold text-zinc-950">Our Featured Courses</h2>
        <p class="my-8">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores
            quae porro consequatur aliquam, incidunt eius magni provident,
            doloribus omnis minus temporibus perferendis nesciunt quam
            repellendus nulla nemo ipsum odit corrupti consequuntur possimus,
            vero mollitia velit ad consectetur. Alias, laborum excepturi nihil
            autem nemo numquam, ipsa architecto non, magni consequuntur.
        </p>
        <div class="grid lg:grid-cols-4 gap-4">
            <div class="[&_.top]:bg-red-400 bg-zinc-100">
                <Feature {...featuresContent[0]}>
                    <div class="pt-12">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor"
                            class="size-12 text-white mx-auto"
                            viewBox="0 0 16 16"
                        >
                            <path
                                d="M2.5.5A.5.5 0 0 1 3 0h10a.5.5 0 0 1 .5.5q0 .807-.034 1.536a3 3 0 1 1-1.133 5.89c-.79 1.865-1.878 2.777-2.833 3.011v2.173l1.425.356c.194.048.377.135.537.255L13.3 15.1a.5.5 0 0 1-.3.9H3a.5.5 0 0 1-.3-.9l1.838-1.379c.16-.12.343-.207.537-.255L6.5 13.11v-2.173c-.955-.234-2.043-1.146-2.833-3.012a3 3 0 1 1-1.132-5.89A33 33 0 0 1 2.5.5m.099 2.54a2 2 0 0 0 .72 3.935c-.333-1.05-.588-2.346-.72-3.935m10.083 3.935a2 2 0 0 0 .72-3.935c-.133 1.59-.388 2.885-.72 3.935"
                            />
                        </svg>
                    </div>
                </Feature>
            </div>
            <div class="[&_.top]:bg-orange-400 bg-zinc-100">
                <Feature {...featuresContent[1]}>
                    <div class="pt-12">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor"
                            class="size-12 text-white mx-auto"
                            viewBox="0 0 16 16"
                        >
                            <path
                                d="M6.002 5.5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0"
                            />
                            <path
                                d="M2.002 1a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V3a2 2 0 0 0-2-2zm12 1a1 1 0 0 1 1 1v6.5l-3.777-1.947a.5.5 0 0 0-.577.093l-3.71 3.71-2.66-1.772a.5.5 0 0 0-.63.062L1.002 12V3a1 1 0 0 1 1-1z"
                            />
                        </svg>
                    </div>
                </Feature>
            </div>
            <div class="[&_.top]:bg-green-400 bg-zinc-100">
                <Feature {...featuresContent[2]}>
                    <div class="pt-12">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor"
                            class="size-12 text-white mx-auto"
                            viewBox="0 0 16 16"
                        >
                            <path
                                d="M6 12q0 1-.25 1.5H5a.5.5 0 0 0 0 1h6a.5.5 0 0 0 0-1h-.75Q10 13 10 12h4c2 0 2-2 2-2V4c0-2-2-2-2-2H2C0 2 0 4 0 4v6c0 2 2 2 2 2z"
                            />
                        </svg>
                    </div>
                </Feature>
            </div>
            <div class="[&_.top]:bg-sky-400 bg-zinc-100">
                <Feature {...featuresContent[2]}>
                    <div class="pt-12">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor"
                            class="size-12 text-white mx-auto"
                            viewBox="0 0 16 16"
                        >
                            <path
                                d="m10.495 6.92 1.278-.619a.483.483 0 0 0 .126-.782c-.252-.244-.682-.139-.932.107-.23.226-.513.373-.816.53l-.102.054c-.338.178-.264.626.1.736a.48.48 0 0 0 .346-.027ZM7.741 9.808V9.78a.413.413 0 1 1 .783.183l-.22.443a.6.6 0 0 1-.12.167l-.193.185a.36.36 0 1 1-.5-.516l.112-.108a.45.45 0 0 0 .138-.326M5.672 12.5l.482.233A.386.386 0 1 0 6.32 12h-.416a.7.7 0 0 1-.419-.139l-.277-.206a.302.302 0 1 0-.298.52z"
                            />
                            <path
                                d="M8 0a8 8 0 1 0 0 16A8 8 0 0 0 8 0M1.612 10.867l.756-1.288a1 1 0 0 1 1.545-.225l1.074 1.005a.986.986 0 0 0 1.36-.011l.038-.037a.88.88 0 0 0 .26-.755c-.075-.548.37-1.033.92-1.099.728-.086 1.587-.324 1.728-.957.086-.386-.114-.83-.361-1.2-.207-.312 0-.8.374-.8.123 0 .24-.055.318-.15l.393-.474c.196-.237.491-.368.797-.403.554-.064 1.407-.277 1.583-.973.098-.391-.192-.634-.484-.88-.254-.212-.51-.426-.515-.741a7 7 0 0 1 3.425 7.692 1 1 0 0 0-.087-.063l-.316-.204a1 1 0 0 0-.977-.06l-.169.082a1 1 0 0 1-.741.051l-1.021-.329A1 1 0 0 0 11.205 9h-.165a1 1 0 0 0-.945.674l-.172.499a1 1 0 0 1-.404.514l-.802.518a1 1 0 0 0-.458.84v.455a1 1 0 0 0 1 1h.257a1 1 0 0 1 .542.16l.762.49a1 1 0 0 0 .283.126 7 7 0 0 1-9.49-3.409Z"
                            />
                        </svg>
                    </div>
                </Feature>
            </div>
        </div>
    </Container>
</div>
