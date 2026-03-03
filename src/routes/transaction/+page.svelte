<script lang="ts">
    import { Button, TableHead } from "flowbite-svelte";
    import {
        Table,
        TableBody,
        TableHeadCell,
        TableBodyRow,
        TableBodyCell,
    } from "flowbite-svelte";

    const items = [
        {
            id: "1",
            type: "Type",
            merchant: "Noel Crispin",
            date: "26 December, 1:00 PM",
            category: "Category",
            amount: "0.00",
        },
        {
            id: "2",
            type: "Type",
            merchant: "Title",
            date: "26 December, 1:00 PM",
            category: "Category",
            amount: "200.00",
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
            shadow
            hoverable
            class="shadow-md rounded-full border border-border-warm"
        >
            <TableHead>
                <TableHeadCell>Type</TableHeadCell>
                <TableHeadCell>Merchant</TableHeadCell>
                <TableHeadCell>Date</TableHeadCell>
                <TableHeadCell>Category</TableHeadCell>
                <TableHeadCell>Amount</TableHeadCell>
            </TableHead>
            <TableBody>
                {#each items as item (item.id)}
                    <TableBodyRow>
                        <TableBodyCell>{item.type}</TableBodyCell>
                        <TableBodyCell>{item.merchant}</TableBodyCell>
                        <TableBodyCell>{item.date}</TableBodyCell>
                        <TableBodyCell>{item.category}</TableBodyCell>
                        <TableBodyCell>{item.amount}</TableBodyCell>
                    </TableBodyRow>
                {/each}
            </TableBody>
        </Table>
        >>>>>>> b76d1aa (Initial Commit)

        <div class="ml-2">
            <span class="text-xs"
                >Showing transaction {items.length} of {items.length}</span
            >
        </div>
    </div>
</div>
