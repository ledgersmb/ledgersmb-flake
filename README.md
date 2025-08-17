# Goals

## Dev shells (nix develop)

* Load Perl, all necessary libraries, whatever front-end build tools we need (Vite, Quasar, etc), CLI admin tool, wrapper for starting dev environment

## Apps (nix run)

* Dev configuration - run Postgres, Caddy, Starman `nix run .#develop`
* Production - run Starman only `nix run .#starman`
* Demo - run dev instance, load demo data `nix run .#demo`

## Build targets (nix build)

* Build JS `nix build .#ui`
* Build Docker image with Starman `nix build .#starman`
* Build Docker image with Starman + Nginx (or Caddy?) `nix build .#dockerweb`
* Build VM image (QEMU/KVM) with Starman + Postgres + Nginx/Caddy `nix build .#vm`
* Build zip `nix build .#zip`
* Build .tar.gz `nix build .#default`
* Build Nginx/Caddy Docker image with local UI/ directory `nix build .#web`

## Template

* Kickstart a new dev instance `nix flake init --template github:ledgersmb/LedgerSMB#default`
* Run a dev LSMB instance with demo data `nix run github:ledgersmb/LedgerSMB#demo`
