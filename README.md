# nur-packages

**My personal [NUR](https://github.com/nix-community/NUR) repository**

![Build and populate cache](https://github.com/ondt/nur-packages/workflows/Build%20and%20populate%20cache/badge.svg)

# Adding the NUR repository to `configuration.nix`
```nix
nixpkgs.config.packageOverrides = pkgs: {
    nur = import (fetchTarball "https://github.com/nix-community/NUR/archive/master.tar.gz") {
        inherit pkgs;
    };
};
```
