# Tap Target Prompt - Onboarding

## Installation

dependencies
```
implementation ("com.getkeepsafe.taptargetview:taptargetview:1.13.3")
```
or
```
implementation (libs.taptargetview)
```

## Usage

Simple usage for one items

```
        TapTargetView.showFor(this,
                TapTarget.forView(btn1, "This is a Button 01", "We have the best targets, believe me")
                        // All options below are optional
                        .outerCircleColor(R.color.red)
                        .outerCircleAlpha(0.96f) 
                        .targetCircleColor(R.color.white)
                        .titleTextSize(20)
                        .titleTextColor(R.color.white)
                        .descriptionTextSize(10) 
                        .descriptionTextColor(R.color.red)
                        .textColor(R.color.blue)
                        .textTypeface(Typeface.SANS_SERIF) 
                        .dimColor(R.color.black)
                        .drawShadow(true)
                        .cancelable(false) 
                        .tintTarget(true)
                        .transparentTarget(false) 
                        .targetRadius(60),
                new TapTargetView.Listener() {
                    @Override
                    public void onTargetClick(TapTargetView view) {
                        super.onTargetClick(view);
                        Toast.makeText(MainActivity.this, "This is Promote Display", Toast.LENGTH_SHORT).show();
                    }
                });
```

## Usage (Another)
Usage for Many Items

```
new TapTargetSequence(this)
    .targets(
        TapTarget.forView(findViewById(R.id.never), "Gonna"),
        TapTarget.forView(findViewById(R.id.give), "You", "Up")
                .dimColor(android.R.color.never)
                .outerCircleColor(R.color.gonna)
                .targetCircleColor(R.color.let)
                .textColor(android.R.color.you),
        TapTarget.forBounds(rickTarget, "Down", ":^)")
                .cancelable(false)
                .icon(rick))
    .listener(new TapTargetSequence.Listener() {
        @Override
        public void onSequenceFinish() {
            
        }
        
        @Override
        public void onSequenceStep(TapTarget lastTarget, boolean targetClicked) {

        }

        @Override
        public void onSequenceCanceled(TapTarget lastTarget) {

        }
    });
```


<img src="https://raw.githubusercontent.com/KeepSafe/TapTargetView/master/.github/video.gif"/>





