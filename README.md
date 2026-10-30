# organizarquivo-apt

APT repository for [organizarquivo](https://github.com/eduardozitinho1/organizarquivo).

Served via GitHub Pages at https://eduardozitinho1.github.io/organizarquivo-apt/

## Debian / Ubuntu / Mint / Pop!_OS / WSL

    sudo install -d -m 0755 /etc/apt/keyrings
    sudo curl -fsSL https://eduardozitinho1.github.io/organizarquivo-apt/organizarquivo.gpg -o /etc/apt/keyrings/organizarquivo.gpg
    echo "deb [signed-by=/etc/apt/keyrings/organizarquivo.gpg] https://eduardozitinho1.github.io/organizarquivo-apt stable main" | sudo tee /etc/apt/sources.list.d/organizarquivo.list
    sudo apt update
    sudo apt install organizarquivo

## Termux

    pkg install curl gnupg
    mkdir -p "$PREFIX/etc/apt/keyrings"
    curl -fsSL https://eduardozitinho1.github.io/organizarquivo-apt/organizarquivo.gpg -o "$PREFIX/etc/apt/keyrings/organizarquivo.gpg"
    echo "deb [signed-by=$PREFIX/etc/apt/keyrings/organizarquivo.gpg] https://eduardozitinho1.github.io/organizarquivo-apt termux main" > "$PREFIX/etc/apt/sources.list.d/organizarquivo.list"
    pkg update
    pkg install organizarquivo-termux
