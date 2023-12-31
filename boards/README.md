Hello. Most people won't need to do anything with this folder, but it does need to exist so the build doesn't print an unnecessary warning message.

If you have used this repository as a jumping-off point for a user-config repo for more than just MechWild: it is possible to add more boards and shields to this folder, but consider [creating a Zephyr module](https://zmk.dev/docs/development/new-shield#new-zephyr-module-repository) and adding them to the [`west` manifest](../config/west.yml) instead.
