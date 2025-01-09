# Foundations of Computer Science Lab05

Your goal is to recreate this program from the sample code provided:
- <http://homer.stuy.edu/~dw/netlogo/lab05_obf.html>

### Instructions
At the end of this file, you will see a large code block. It contains some instructions and starter code for this assignment. You should:
- Copy the code block into a new NetLogo program.
- In NetLogo, fill in the procedures and add the required interface elements.
- When done, save the file as __lab05.nlogo__, and upload the entire file to this repository.

```
; For this assignment, you will need to create procedures
; and interface elements.
; Use this example as your guide:
; http://homer.stuy.edu/~dw/netlogo/lab05_obf.html
;
; This program will simulate an ecosystem made
; of wolves, sheep and grass.
;
; The wolves and sheep roam around the world.
; as they do so, they loose health. They can gain
; health by eating, but if they hit 0 health they die.
; The wolves and sheep also reproduce.
;
; The patches are land, which will either be grass or dirt
; Grass patches stay grass unless eaten by a sheep.
; Dirt patches will regrow into grass after 30 ticks
;
; You will need to create interface elements:
;   2 sliders
;   1 switch
;   2 buttons
;   1 plot (the plot should include a title and the legend)
;
; The world is 51x51, with a patch size of 10

; breeds and custom properties are already set
; leave this code alone
breed [wolves wolf]
breed [sheep a-sheep]
turtles-own [health]
patches-own [clock]

; setup
;
; clear the screen
; create numWolves wolves and numSheep sheep
;
; the visual properties of the wolves and sheep
; should match the web demo version.
;
; wolves should have starting health in the range [0, 40)
; sheep should have starting health in the range [0, 8)
;
; patches should have a 50/50 chance to be grass  or dirt
;    grass patches are green
;    dirt patches are brown and have a clock value in the range [0, 30)
to setup

end



; go
;
; To work correctly, go should call
; other procedures defined below when possible.
;
; Wolves should eat sheep, reproduce with
; a 5% chance of reproduction and decrease
; their health by 1.
;
; Sheep should eat grass and reproduce with
; a 4% chance of reproduction. If grass? is true,
; decrease their health by 1. Otherwise, leave
; health alone.
;
; All turtles should move randomly,
; and potentially die.
;
; Dirt patches should grow.
to go

end

; eat-sheep
;
; If there is a sheep on the same patch
; as the calling turtles (which will be a wolf),
; one sheep should die and the calling wolf
; should increase its health by 20
to eat-sheep

end

; eat-grass
;
; If the patch the calling turtles (which will
; be a sheep) is green and grass? is true,
; the patch should become brown and reset its
; clock to 30. The calling sheep should
; increase its health by 4
to eat-grass

end


; grow
;
; If the clock of a brown patch is 0,
; the patch should become green.
; Otherwise, the patch should decrease its
; clock by 1
to grow

end

; death
;
; If a turtle's health is less than
; 0, it should die.
to death

end


; reproduce
;
; The calling turtle should have a rate%
; chance of creating a new turtle. The
; calling turtle and the new turtle should
; each have half the amount of health that
; the calling turtle started with. The new
; turtle should immediately wiggle.
;
; hatch is a turtle procedure.
; hatch 1
; Will create a new turtle, that is an exact
; copy of the "parent" turtle, aside from who
; number. All other properties will be identical.
; If you give hatch a command block as the second
; parameter, the new trutle will run those commands
; (similar to crt or cro)
to reproduce [rate]

end


; wiggle
;
; You do not need to modify this code
to wiggle
  rt random 45
  lt random 45
  fd 1
end
```
