# Prakses Asistents deployment

This repository is the Prakses Asistents fork of Buzz. Upstream is
<https://github.com/block/buzz>.

Production infrastructure and operational configuration are maintained in the
private `praksesasistents/buzz-infrastructure` repository. Production container
images are published under `ghcr.io/praksesasistents/buzz` and must be promoted
by immutable digest.

Keep `main` synchronized with upstream. Place organization-specific application
changes on reviewed branches and preserve a clear upstream merge path.

Infrastructure changes must allocate new network addresses for Buzz. Existing
production, allowlisted, and VPN egress addresses must never be detached,
released, reassociated, or repurposed for this service.
