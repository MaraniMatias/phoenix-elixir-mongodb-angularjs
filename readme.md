# Introducción

# Requisitos
Tener instalado Elixir and Erlang, [Guia de instalacion](http://elixir-lang.org/install.html) o [aqui](https://github.com/MaraniMatias/elixir-hola-mundo).
Opcional tener instalado [NodeJS](https://nodejs.org/).

Luego en la terminal
```sh
$ mix local.hex
$ mix archive.install https://github.com/phoenixframework/archives/raw/master/phoenix_new.ez
```

# Comencemos
Phoenix usa [Brunch.io](http://brunch.io/) para administrar archivos.
Con el siguiente comando creamos la base de nuestra aplicacion web.
Uso `--database mysql` or `--database mongodb` porque predeterminado Phoenix usa PogresSQL.
Deforma predeterminada Phoenix usa [Ecto](http://www.phoenixframework.org/docs/ecto-models) para accesos ala base de datos, se puede desactivar con `--no-ecto`.

* NodeJS instalado.
```sh
$ mix phoenix.new myAppWeb --database mongodb
```
* Sin tener NodeJS
```sh
$ mix phoenix.new myAppWeb --no-brunch --database mongodb
```
Hora nos pide instalar dependencias.
Antes vemos a actualizar las versiones de las dependencias según [Hex](https://hex.pm/).

Abrimos el archivo `mix.exs` en la raíz de nuestra app `myAppWeb`.
```elixir
  defp deps do
    [{:phoenix, "~> 1.2.1"},
     {:phoenix_pubsub, "~> 1.0"},
     {:phoenix_ecto, "~> 3.2.1"},
     {:mongodb_ecto, ">= 0.1.5"},
     {:phoenix_html, "~> 2.9.2"},
     {:phoenix_live_reload, "~> 1.0.7", only: :dev},
     {:gettext, "~> 0.13.0"},
     {:cowboy, "~> 1.0.4"},
     {:phoenix_expug, "~> 0.0.3"}]
  end
```
Ahora a descargar/instalar las dependencias
```sh
$ mix deps.get
```


# Bibliografía
* [Phoenix Framework](http://www.phoenixframework.org)
