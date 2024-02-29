# Make your Leonis
## Requirements
!!! npm "Node Package Manager"
    The builder is available on [npmjs.com :octicons-link-external-24:](https://www.npmjs.com/package/){target='_blank'} named `@leonis/builder`.

For configure your Leonis, you need to have installed:
<div class="grid cards" markdown>
-   :fontawesome-brands-node-js:{ .lg .middle } __Node JS__

    ---

    You need to install NodeJS.

    [:octicons-arrow-right-24: Install](https://nodejs.org/en/download)

-   :octicons-command-palette-24:{ .lg .middle } __Builder__

    ---

    You need to install the Leonis Builder.

    ```bash
    npm install -g @leonis/builder
    ```
</div>
## Configure
For configure your Leonis, you need to create a `config.yml` or any other file with the same extension.
### Required fields
A leonis config file must have the following fields:

-   `name`: Your username
-   `description`: A little description about you
-   `background`: The background image of your page (For the path, see [here](#file-paths))
### File paths
For multiple fields, you have to specify the path of the file.
To specify the path of the file, you need to make a folder named `resources`.
And inside the folder, you need to put the files.

After, in the field, you need to put the name of the file.

### Effects
You can add effects to your page. There are effects for the background, your name, and your description.

!!! note
    All the fields are optional.

In the config file, this is the syntax:
```yaml
effects:
  background:
  name:
  description:
```
#### Background
The effects for the background are:

<div class="grid cards" markdown>

-   `blurred`: The background is blurred.

    For this effect, you can specify the intensity of the blur.

    ```yaml
    effects: 
      background: blurred
    background_blur: 5px
    ```

    ---

    ![Blurred](assets/blurred.png)
    [:octicons-zoom-in-24: Zoom](assets/blurred.png){target='_blank'}

-   `old_tv`: The background is like an old TV.

    ---

    ![Old TV](assets/oldtv.png)
    [:octicons-zoom-in-24: Zoom](assets/oldtv.png){target='_blank'}

-   `night_time`: The background is darken.
    
    ---

    ![Night Time](assets/nighttime.png)
    [:octicons-zoom-in-24: Zoom](assets/nighttime.png){target='_blank'}

</div>

#### Name
The effects for the name are:

<div class="grid cards" markdown>

-   `rainbow`: The name is like a rainbow.

    ---

    ![Rainbow](assets/rainbow.gif)
    [:octicons-zoom-in-24: Zoom](assets/rainbow.gif){target='_blank'}

-   `flash`: The name is flashing.

    ---

    ![Flash](assets/flash.gif)
    [:octicons-zoom-in-24: Zoom](assets/flash.gif){target='_blank'}

</div>

#### Description
The effects for the description are:

<div class="grid cards" markdown>

-   `typewriter`: The description is like a typewriter.
    
    ---

    ![Typewriter](assets/typewriter.gif)

    [:octicons-zoom-in-24: Zoom](assets/typewriter.gif){target='_blank'}
</div>

### Links
You can add links to your page. There are links for your social media and your projects.

In the config file, this is the syntax:
```yaml
links:
    - icon: Icon
      url: Link
      color: Color
```
#### Icon
The icon is the icon of the link.
Icons are from [Simple Icons](https://simpleicons.org/).

#### URL
This is the URL of the project or the social media.

#### Color
For the style, we add a colored shadow to the icon.

This is the color of the shadow.

### Profile
This is multiple things related to your profile.

For, the profile, this is the syntax:
```yaml
profile:
  field: Value
```

#### Blur
This is the blur of the container of the profile.

Blur is expressed in pixels.
```yaml
profile:
  blur: 5px
```

#### Opacity
This is the opacity of the container of the profile.

Opacity is expressed in percentage.
```yaml
profile:
  opacity: 20
```

#### Avatar
!!! info end "File path"
    For the path, see [here](#file-paths).

This is the avatar of the profile.

```yaml
profile:
  avatar: avatar.png
```

#### Layout
This is the layout for your username, description and avatar.

The layout can be `center`, `left` or `right`.
```yaml
profile:
  layout: center
```

#### Discord
This is your Discord ID, for show your Discord Status.
```yaml
profile:
  discord: "902671568856047636"
```

#### Geolocation
This is your geolocation, if you want to show it.
```yaml
profile:
  geolocation:
    latitude: 48.569045
    longitude: 7.6796789
```

### Music
!!! info end "File path"
    For the path, see [here](#file-paths).

This is the music for your page.
The music add a background music to your page.

This feature add a message when a person load your page before start the music.

For the music, this is the syntax:
```yaml
music: music.mp3
```

### Backend
This is the backend for get Discord Status.
For the backend, this is the syntax:
```yaml
backend: https://leonis.oriondev.fr
```

## Build
For build your Leonis, you need to run the following command:
```bash
leonis
```

### Options
The builder have two options:

-   `--input`: The path of the config file.
-   `--output`: The path of the output folder.
