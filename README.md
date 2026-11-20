# Spotify 3D / arquivo de escuta

Uma estante 3D para organizar e ouvir uma coleção musical local. A interface usa Astro e CSS 3D; não há integração com a API do Spotify.

## Como adicionar um álbum

1. Coloque a capa quadrada em `public/covers/`.
2. Coloque os arquivos de áudio em `public/audio/<id-do-album>/`.
3. Adicione o álbum em `src/data/albums.json`.

Exemplo:

```json
{
  "id": "meu-album",
  "title": "Meu Álbum",
  "shortTitle": "Meu Álbum",
  "artist": "Minha Banda",
  "year": 2026,
  "color": "#b46e49",
  "cover": "/covers/meu-album.jpg",
  "tracks": [
    {
      "title": "Minha Música",
      "src": "/audio/meu-album/01-minha-musica.mp3",
      "duration": "3:42"
    }
  ]
}
```

## Desenvolvimento

```sh
npm install
npm run dev
```

O player usa o elemento de áudio nativo do navegador. Os caminhos cadastrados podem apontar para MP3, WAV ou OGG.

## Validação

```sh
npm run build
```
