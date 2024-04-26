# How to change the textStyle of the header cells in a Flutter DataTable (SfDataGrid)?.

In this article, we will show you how to change the textStyle of the header cells in a [Flutter DataTable](https://www.syncfusion.com/flutter-widgets/flutter-datagrid).

Initialize the [SfDataGrid](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/SfDataGrid-class.html) widget with all the necessary properties. The [GridColumn.label](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/GridColumn/label.html) is used to display the required widget in a column header. Under the label property of [GridColumn](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/GridColumn-class.html), the corresponding header text widget is loaded. Therefore, you can add the required header text style to the loaded text widget.

```dart
 @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Syncfusion Flutter DataGrid'),
      ),
      body: SfDataGrid(
        source: employeeDataSource,
        columnWidthMode: ColumnWidthMode.fill,
        columns: <GridColumn>[
          GridColumn(
              columnName: 'id',
              label: Container(
                  padding: const EdgeInsets.all(16.0),
                  alignment: Alignment.center,
                  child: const Text(
                    'ID',
                    style: TextStyle(
                        color: Colors.red, fontWeight: FontWeight.bold),
                  ))),
          GridColumn(
              columnName: 'name',
              label: Container(
                  padding: const EdgeInsets.all(8.0),
                  alignment: Alignment.center,
                  child: const Text(
                    'Name',
                    style: TextStyle(
                        color: Colors.green, fontWeight: FontWeight.bold),
                  ))),
          GridColumn(
              columnName: 'designation',
              label: Container(
                  padding: const EdgeInsets.all(8.0),
                  alignment: Alignment.center,
                  child: const Text(
                    'Designation',
                    style: TextStyle(
                        color: Colors.blueAccent, fontWeight: FontWeight.bold),
                    overflow: TextOverflow.ellipsis,
                  ))),
          GridColumn(
              columnName: 'salary',
              label: Container(
                  padding: const EdgeInsets.all(8.0),
                  alignment: Alignment.center,
                  child: const Text(
                    'Salary',
                    style: TextStyle(
                        color: Colors.pink, fontWeight: FontWeight.bold),
                  ))),
        ],
      ),
    );
  }
```

You can download this example in [GitHub](https://github.com/SyncfusionExamples/How-to-change-the-textStyle-of-the-header-cells-in-a-Flutter-DataTable-SfDataGrid).