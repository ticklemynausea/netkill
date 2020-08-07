# netkill

Usage: `netkill [-s signum] <expr> [<expr>] ...`

Kills processes that are bound to TCP or UDP ports. `<expr>` is of the form `protocol@host:port`. Omitting the protocol will default to TCP. Using an integer as an expression will signal all processes bound to that TCP port. Otherwise, it will signal all processes bound to that TCP host.

signum defaults to `-9` (sigkill)

Examples:
- `netkill 3000 8080`
- `netkill UDP:50000`
- `netkill my.frontend.local my.backend.local localhost:9999`
