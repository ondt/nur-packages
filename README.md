# nur-packages

**My personal [NUR](https://github.com/nix-community/NUR) repository**

![Build and populate cache](https://github.com/ondt/nur-packages/workflows/Build%20and%20populate%20cache/badge.svg)

# Available packages
- [`nur.repos.ondt.lemonade`](https://github.com/Snowlabs/lemonade): A multithreaded alternative to [lemonbar](https://github.com/krypt-n/bar) written in rust

# Installing a package
```console
$ nix-shell -p nur.repos.ondt.lemonade
```

or

```console
$ nix-env -f '<nixpkgs>' -iA nur.repos.ondt.lemonade
```

or

```console
# configuration.nix
environment.systemPackages = with pkgs; [
  nur.repos.ondt.lemonade
];
```

# Adding the NUR repository to `configuration.nix`
```nix
nixpkgs.config.packageOverrides = pkgs: {
    nur = import (fetchTarball "https://github.com/nix-community/NUR/archive/master.tar.gz") {
        inherit pkgs;
    };
};
```
