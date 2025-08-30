Thank you for using Optimal-Table

Developed by Suresh Kumar M

This Optimal table is built to simplify the table component which is optimized in a way where the table by itself can handle your API calls including fetch, update, add, delete with using the apiConfig parameter. The table offers backend based pagination, page per row, export to CSV, excel and PDF, search filters and provides both frontend and backend sorting. Requires only two parameters to be passed and you save 4+ hours on creating a reusable table component, All with one package!

Happy coding!

NPM packages required :

1) axios
2) react-toastify
3) xlsx
4) file-saver
5) jspdf
6) jspdf-autotable

Usage :

```bash

<TableComponent
    apiConfig={apiConfig}
    headerValues={headerValues}
/>

```

apiConfig consists few of the below listed properties :

```bash

const apiConfig = {
    method: 'get',
    url: `http://localhost:5000/api/getAll`,
    query: {},
    params: {},
    data: {},
    headers: {
        authorization: tokenData
    },
    toastEnabled: false,
    operation: "fetch"
}

```

headerValues consist of these parameters for rendering :

```bash

const headerValues: any[] = [
    { header: "Name", accessor: "name", sortable: true },
    { 
        header: "Status", 
        accessor: "status", 
        render: (_value: any, row: any) => {}
    }
]

```