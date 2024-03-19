<script>
    // @ts-nocheck
    export let chartInfo = {};
    const title = chartInfo.title;
    let slug = title
        .toLowerCase()
        .replace(/ /g, "-")
        .replace(/[^\w-]+/g, "");
</script>

<div
    class="max-w-fit bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
>
    <div class="w-full h-64 rounded-t-lg px-10">
        <img
            class="w-full h-full object-cover overflow-x-scroll"
            src={chartInfo.src}
            alt={chartInfo.title}
        />
    </div>

    <div class="p-5">
        <h5
            class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
        >
            {chartInfo.title}
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
            {chartInfo.description}
        </p>

        <a
            href={`/details/${slug}`}
            class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
        >
            Code
            <svg
                class="rtl:rotate-180 w-3.5 h-3.5 ml-2"
                fill="none"
                viewBox="0 0 14 10"
            >
                <path
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M1 5h12m0 0L9 1m4 4L9 9"
                />
            </svg>
        </a>
    </div>
</div>
