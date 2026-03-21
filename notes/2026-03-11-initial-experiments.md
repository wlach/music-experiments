# A minor scale

Experiments interacting with chatgpt and strudel, trying to reproduce something vaguely industrial.

```js
stack(
  note("<a1 e1 e1 e1 e1 ~ ~ ~ ~ bb1 bb1 bb1 bb1 a1 a1>*4")
    .sound("metal")
    .lpf("300 500 250 450")
    .gain(0.8)
    .room(0.5),

  note("<a1 e1 e1 e1 e1>*4")
    .sound("sawtooth")
    .lpf(sine.range(120, 240).slow(4))
    .gain(1)
    .attack(0.02)
    .release(0.2),
);
```

## Notes on implementation

"metal" sound is actually kind of tinny. lpf/gain/room designed to give it more weight (need to figure out what those parameters mean)

"sawtooth" sound meant to represent the bass. Use a sine wave to make it sort of throb in and out. I think attack/release somehow related to that.

## Psychological impact

Feels vaguely menacing but honestly more cheesey than anything. The bflat after the pause indicate something is "off" in that cheap horror movie kind of way.

Other experiments I tried with piano, just trying to get a sense of what's going on.

Campy horror:

```js
note("<a3 bb3 a3 bb3 a3>*4").sound("piano");
```

Vaguely campy cinematic (not quite as bad):

```js
note("<a3 e3 f3 e3 a3>*4").sound("piano");
```

(ChatGPT describes it as a "A structural anchor (A and E), A dissonant neighbor (F)")

Vaguely industrial, not really musical but probably gussied up with the right sample.

```js
note("<a3 a3 ~ e3 a3 ~ e3>*4").sound("piano");
```
