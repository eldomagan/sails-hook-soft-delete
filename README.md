# Sails hook soft delete

This hook add soft delete functionality to Waterline ORM

## Installation

```shell
npm install --save sails-hook-soft-delete
```

```shell
# For yarn users
yarn add sails-hook-soft-delete
```

## Usage

### Deleting record

Now the `Model.destroyOne()` method will mark the record as soft-deleted. It set the deletedAt attribute to current date.

If you want to completely remove a record, use the `Model.forceDestroyOne()`method.

You can also use `Model.destroy()` and `Model.forceDestroy()` to soft-delete/delete many record.

### Restoring record

Once a record is soft-deleted, you can restore it using `Model.restoreOne()` /  `Method.restore()` method.

### Quering records

`Model.find()` / `Model.findOne()` will now find record which are not soft-deleted.

If you want to include soft-deleted record, use `Model.findWithTrashed()` method

To get only soft-deleted record, use `Model.findTrashed()` method


