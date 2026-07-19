# HomeVisibility

Whether this hub is visible on the home screen
  - all: Visible to all users
  - none: Visible to no users
  - admin: Visible to only admin users
  - shared: Visible to shared users

## Example Usage

```java
import dev.plexapi.sdk.models.shared.HomeVisibility;

HomeVisibility value = HomeVisibility.ALL;
```


## Values

| Name     | Value    |
| -------- | -------- |
| `ALL`    | all      |
| `NONE`   | none     |
| `ADMIN`  | admin    |
| `SHARED` | shared   |