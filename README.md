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
                        .outerCircleColor(R.color.blue)
                        .outerCircleAlpha(0.96f)
                        .targetCircleColor(R.color.white)
                        .titleTextSize(20)
                        .titleTextColor(R.color.white)
                        .descriptionTextSize(10)
                        .descriptionTextColor(R.color.white)
                        .textColor(R.color.white)
                        .textTypeface(Typeface.DEFAULT)
                        .dimColor(R.color.black)
                        .drawShadow(true)
                        .cancelable(false)
                        .tintTarget(true)
                        .transparentTarget(false)
                        .icon(ContextCompat.getDrawable(this, R.drawable.andro_icon))
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
                        TapTarget.forView(btn1, "Button 1", "This is First Button")
                                .outerCircleColor(R.color.blue)
                                .outerCircleAlpha(0.96f)
                                .targetCircleColor(R.color.white)
                                .titleTextSize(20)
                                .titleTextColor(R.color.white)
                                .descriptionTextSize(10)
                                .descriptionTextColor(R.color.white)
                                .textColor(R.color.white)
                                .textTypeface(Typeface.DEFAULT)
                                .dimColor(R.color.black)
                                .drawShadow(true)
                                .cancelable(false)
                                .tintTarget(true)
                                .transparentTarget(false)
                                .icon(ContextCompat.getDrawable(this, R.drawable.andro_icon))
                                .targetRadius(60),

                        TapTarget.forView(btn2, "Button 2", "This is Second Button")
                                .outerCircleColor(R.color.blue)
                                .outerCircleAlpha(0.96f)
                                .targetCircleColor(R.color.white)
                                .titleTextSize(20)
                                .titleTextColor(R.color.white)
                                .descriptionTextSize(10)
                                .descriptionTextColor(R.color.white)
                                .textColor(R.color.white)
                                .textTypeface(Typeface.DEFAULT)
                                .dimColor(R.color.black)
                                .drawShadow(true)
                                .cancelable(false)
                                .tintTarget(true)
                                .transparentTarget(false)
                                .icon(ContextCompat.getDrawable(this, R.drawable.baseline_3d_rotation_24))
                                .targetRadius(60),

                        TapTarget.forView(btn3, "Button 3", "This is Third Button")
                                .outerCircleColor(R.color.blue)
                                .outerCircleAlpha(0.96f)
                                .targetCircleColor(R.color.white)
                                .titleTextSize(20)
                                .titleTextColor(R.color.white)
                                .descriptionTextSize(10)
                                .descriptionTextColor(R.color.white)
                                .textColor(R.color.white)
                                .textTypeface(Typeface.DEFAULT)
                                .dimColor(R.color.black)
                                .drawShadow(true)
                                .cancelable(false)
                                .tintTarget(true)
                                .transparentTarget(false)
                                .icon(ContextCompat.getDrawable(this, R.drawable.user))
                                .targetRadius(60),

                        TapTarget.forView(btn4, "Button 4", "This is Four Button")
                                .outerCircleColor(R.color.blue)
                                .outerCircleAlpha(0.96f)
                                .targetCircleColor(R.color.white)
                                .titleTextSize(20)
                                .titleTextColor(R.color.white)
                                .descriptionTextSize(10)
                                .descriptionTextColor(R.color.white)
                                .textColor(R.color.white)
                                .textTypeface(Typeface.DEFAULT)
                                .dimColor(R.color.black)
                                .drawShadow(true)
                                .cancelable(false)
                                .tintTarget(true)
                                .transparentTarget(false)
                                .icon(ContextCompat.getDrawable(this, R.drawable.baseline_1k_24))
                                .targetRadius(60)).listener(new TapTargetSequence.Listener() {
                    @Override
                    public void onSequenceFinish() {
                        Toast.makeText(MainActivity.this, "Well Done", Toast.LENGTH_SHORT).show();
                    }

                    @Override
                    public void onSequenceStep(TapTarget lastTarget, boolean targetClicked) {
                    }

                    @Override
                    public void onSequenceCanceled(TapTarget lastTarget) {

                    }
                }).start();
```


<img src="https://raw.githubusercontent.com/KeepSafe/TapTargetView/master/.github/video.gif"/>





