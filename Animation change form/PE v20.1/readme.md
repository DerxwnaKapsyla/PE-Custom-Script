# How to install
Put the `Plugins` folder and the `Graphics` folder in your game's root folder.

# Scripts
## My script `Animation use item`
### If you use it
1. In file `3 - Add animation.rb`, you need to add `animation use item` like normal and then add `animation change form`

## Write new function
1. Read file `3 - Add animation.rb`
1. Use `ItemHandlers::AnimationForm.add` not `ItemHandlers::UseOnPokemon.add`
1. Use 2 methods
```
scene.change_form_animation -> Change animation (normal)
scene.change_form_animation_fusion -> Change animation (fusion)
```
You can add { } to add like `scene.pbRefresh`, `scene.pbHardRefresh` or delete pokemon with this `$Trainer.remove_pokemon_at_index(chosen)`
#### Explain when write methods
##### change_form_animation
You need to add 3 values such as `pokemon name, position of pokemon, form of pokemon`
> Write this method: scene.change_form_animation(pokemon name, position of pokemon, form of pokemon)
##### change_form_animation_fusion
You need to add 6 values such as `pokemon name first, position of pokemon first, form of pokemon first, pokemon name second, position of pokemon second, form of pokemon second`
> Write this method: scene.change_form_animation_fusion(pokemon name first, position of pokemon first, form of pokemon first, pokemon name second, position of pokemon second, form of pokemon second)

## Examples
I wrote some examples, you can find `# Add animation` to learn.

# Graphics
In folder example, you can see this is graphic with multiple frames. Each frame is square.

Name of graphics, it's name of pokemon or name_form, same as PE (raw).
