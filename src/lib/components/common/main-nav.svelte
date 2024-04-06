<script>
    import { page } from "$app/stores";
</script>

<ul class="main-nav uppercase space-y-4 md:space-y-0">
    <li><a href="/" class:active={$page.route.id == "/"}>Home</a></li>
    <li>
        <a href="/about" class:active={$page.route.id == "/about"}>About Us</a>
    </li>
    <li>
        <a href="/courses" class:active={$page.route.id == "/courses"}
            >Courses</a
        >
    </li>
    <li>
        <a href="/portfolio" class:active={$page.route.id == "/portfolio"}
            >Portfolio</a
        >
    </li>
    <li>
        <a href="/pricing" class:active={$page.route.id == "/pricing"}
            >Pricing</a
        >
    </li>
    <li>
        <a href="/contact" class:active={$page.route.id == "/contact"}
            >Contact</a
        >
    </li>
</ul>
