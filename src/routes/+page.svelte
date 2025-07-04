<script lang="ts">
  let fileList = [
    {
      name: "Pictures",
      canCd: true,
      size: "2M",
      lastChanged: "21.03.2024",
    },
    {
      name: "Music",
      canCd: true,
      size: "2M",
      lastChanged: "21.03.2024",
    },
    {
      name: "Code",
      canCd: true,
      size: "2M",
      lastChanged: "21.03.2024",
    },
    {
      name: "Project.docx",
      canCd: false,
      size: "2M",
      lastChanged: "21.03.2024",
    },
    {
      name: "key.txt",
      canCd: false,
      size: "2M",
      lastChanged: "21.03.2024",
    },
    {
      name: "archive.zip",
      canCd: true,
      size: "2M",
      lastChanged: "21.03.2024",
    },
  ];
</script>

<main class="container">
  <div class="file-table">
    <div class="file-table-header">
      <div class="file-table-col">Name</div>
      <div class="file-table-col">Size</div>
      <div class="file-table-col">Last changed</div>
    </div>

    {#each fileList as file}
      <div class="file-table-row">
        <div class="file-table-col">{file.name}</div>
        <div class="file-table-col">{file.size}</div>
        <div class="file-table-col">{file.lastChanged}</div>
      </div>
    {/each}
  </div>
</main>

<style>
  .file-table {
    display: grid;
    grid-template-columns: repeat(3, auto);
    grid-template-rows: auto;
  }

  .file-table-row,
  .file-table-header {
    display: contents;

    .file-table-col {
      padding: 0.2rem 0.5rem;
    }
  }

  .file-table-header {
    .file-table-col {
      background-color: #ffd198;
    }
  }

  .file-table-row {
    .file-table-col {
      background-color: #fff9f3;
    }

    &:nth-child(2n) {
      .file-table-col {
        background-color: #fbecda;
      }
    }
  }
</style>
