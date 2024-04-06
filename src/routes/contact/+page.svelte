<script>
    import SubHeader from "$lib/components/common/sub-header.svelte";
    import Container from "$lib/components/container.svelte";
</script>

<SubHeader title="Contact"></SubHeader>
<Container>
    <iframe
        title="UMA Mental Arithmetic"
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3988.5998452095355!2d103.83236527562939!3d1.4160560985705966!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x31da141221546bcd%3A0xaa9525c15a7e8aed!2zVU1BIE1FTlRBTCBBUklUSE1FVElDICjlpKfmiJDlv4Pnrpcp!5e0!3m2!1sen!2ssg!4v1712331319121!5m2!1sen!2ssg"
        style="border:0;"
        allowfullscreen={false}
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
        class="w-full aspect-[3/2] mt-16"
    ></iframe>
    <div class="grid gap-4 xl:grid-cols-2 mt-8">
        <form class="space-y-4">
            <label>
                <span>Name*</span>
                <input type="text" />
            </label>
            <label>
                <span>Email*</span>
                <input type="email" />
            </label>
            <label>
                <span>Subject*</span>
                <input type="text" />
            </label>
            <label>
                <span>Message*</span>
                <textarea name="" id=""></textarea>
            </label>
            <button class="bg-blue-500 px-6 py-2.5 text-white">Submit</button>
        </form>
        <div class="space-y-4">
            <h3>Contact Info</h3>
            <p class="text-zinc-950 font-bold">
                Lorem ipsum dolor sit amet, cadipisicing sit amet, consectetur
                adipisicing elit. Atque sed, quidem quis praesentium.
            </p>
            <p>
                Lorem ipsum dolor sit amet, cadipisicing sit amet, consectetur
                adipisicing elit. Lorem ipsum dolor sit amet, cadipisicing sit
                amet, consectetur adipisicing elit. Atque sed, quidem quis
                praesentium Atque sed, quidem quis praesentium, ut unde fuga
                error commodi architecto, laudantium culpa tenetur at id, beatae
                pet.
            </p>
            <div class="font-bold text-zinc-950">
                <p>UMA Maths</p>
                <p>Block 845 Yishun Street 81 Khatib Central Singapore</p>
            </div>
            <div>
                <p>Phone:+65-67596978</p>
                <p>Mobile:+6591281568</p>
                <p>
                    <a href="mailto:zhushuihua@maths.education"
                        >zhushuihua@maths.education</a
                    >
                </p>
            </div>
        </div>
    </div>
</Container>

<style class="postcss">
    label {
        @apply flex flex-col gap-2;
    }
    label input,
    label textarea {
        @apply border p-2 w-full;
    }
    label textarea {
        @apply resize-none h-48;
    }
</style>
