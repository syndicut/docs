# Deleting a disk snapshot

> [!IMPORTANT]
>
> Deleting a snapshot is an operation that cannot be canceled or reversed. You cannot restore a deleted snapshot.

To delete a snapshot:

---

**[!TAB Management console]**

1. In the management console, select the folder the snapshot belongs to.
1. Click on the **Yandex Compute Cloud** tile.
1. On the **Virtual machines** page, go to the **Disk snapshots** tab.
1. In the line with the appropriate snapshot, click ![](../../../_assets/dots.png) and select the **Delete** command.
1. Confirm the deletion.

**[!TAB CLI]**

[!INCLUDE [default-catalogue](../../../_includes/default-catalogue.md)]

1. See the description of the CLI's delete snapshot commands:

    ```
    $ yc compute snapshot delete --help
    ```

1. Get a list of all snapshots:

    ```
    $ yc compute snapshot list
    +----------------------+----------------------+----------------------+--------+--------------------------+
    |          ID          |         NAME         |     PRODUCT IDS      | STATUS |       DESCRIPTION        |
    +----------------------+----------------------+----------------------+--------+--------------------------+
    | fd8rlt1u2rf0lps3rqm9 | my-yc-snapshot-fhm53 | f2ecl5vhsftdean0sr6s | READY  | my first snapshot via yc |
    +----------------------+----------------------+----------------------+--------+--------------------------+
    ```

1. Select the `ID` or `NAME` of the snapshot you need.
1. Delete the snapshot:

    ```
    $ yc compute snapshot delete \
        --name my-yc-snapshot-fhm53
    ```

---
