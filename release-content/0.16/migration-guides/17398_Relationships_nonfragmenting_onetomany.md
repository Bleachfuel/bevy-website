- Replace `ChildBuilder` with `ChildSpawnerCommands`.
- Replace calls to `.set_parent(parent_id)` with `.insert(ChildOf(parent_id))`.
- Replace calls to `.replace_children()` with `.remove::<Children>()` followed by `.add_children()`. Note that you’ll need to manually despawn any children that are not carried over.
- Replace calls to `.despawn_recursive()` with `.despawn()`.
- Replace calls to `.despawn_descendants()` with `.despawn_related::<Children>()`.
- If you have any calls to `.despawn()` which depend on the children being preserved, you’ll need to remove the `Children` component first.
