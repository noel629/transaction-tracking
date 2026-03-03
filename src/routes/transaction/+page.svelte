<script lang="ts">
    import { Button } from "flowbite-svelte";
    import { Table } from "flowbite-svelte";

    const items = [
        {
            type: "Type",
            merchant: "Title",
            date: "26 December, 1:00 PM",
            category: "Category",
            amount: "0.00",
        },
    ];
</script>

<div class="flex h-full w-full overflow-hidden">
    <div class="flex-1 flex flex-col overflow-y-auto">
        <div class="flex w-full justify-between items-end mb-8">
            <div>
                <h1 class="text-2xl font-medium">Transactions</h1>
                <p>Manage and review monthly expenses.</p>
            </div>

            <Button color="light" pill>December 2025</Button>
        </div>

        <Table
            {items}
            shadow
            hoverable
            class="shadow-md rounded-full border border-border-warm"
        ></Table>

        <div class="ml-2">
            <span class="text-xs"
                >Showing transaction {items.length} of {items.length}</span
            >
        </div>
    </div>
</div>
