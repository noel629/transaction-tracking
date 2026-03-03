<script lang="ts">
    import { Button } from "flowbite-svelte";
    import { Table } from "flowbite-svelte";
    import { Carousel } from "flowbite-svelte";
    import { AccordionItem, Accordion } from "flowbite-svelte";
    import { Toast } from "flowbite-svelte";
    import { FireOutline, CashSolid } from "flowbite-svelte-icons";
</script>

<div class="flex h-full w-full">
    <Accordion>
        <AccordionItem>
            {#snippet header()}Total Spending So far<FireOutline
                    class="h-6 w-6"
                />{/snippet}
            <p class="text-gray-500 dark:text-gray-400">
                Current month Spending
            </p>
            <p class="mb-2 text-gray-500 dark:text-gray-400 font-bold">
                RM4,000
            </p>
            <p class="text-gray-500 dark:text-gray-400">
                vs Previous months spending
            </p>
            <p
                class="font-bold mb-2 text-gray-500 dark:text-gray-400 font-bold"
            >
                RM5,000
            </p>
        </AccordionItem>
    </Accordion>
    <Accordion>
        <AccordionItem>
            {#snippet header()}Transactions <CashSolid />{/snippet}
            <p class="mb-2 text-gray-500 dark:text-gray-400 font-bold">47</p>
            <p class="mb-2 text-gray-500 dark:text-gray-400">
                Entries this month.
            </p>
        </AccordionItem>
    </Accordion>
</div>

<div></div>
