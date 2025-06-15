<script lang="ts">
    import { Grid, Row, Column } from "carbon-components-svelte";
    import "carbon-components-svelte/css/all.css"

    let rows = 10;
    let columns = 10;
</script>

<div>
    <Grid class="game-grid">
        {#each Array(rows) as _, row_idx}
            <Row>
                {#each Array(columns) as _, col_idx}
                    <Column class="text-xs">({row_idx}, {col_idx})</Column>
                {/each}
            </Row>
        {/each}
    </Grid>
</div>