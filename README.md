# Video-Preview

The Video preview and Validator for react.

## Installation and usage

The easiest way to use video-preview is to install it from npm and build it into your app with Webpack.

```
yarn add @think42labs/video-preview
```

Then use it in your app.

```JavaScript
import React from 'react';
import VideoPreview from  '@think42labs/video-preview';

class App extends Component {
  constructor(props){
    super(props);
    this.state = {
      videoDetails: {}
    }
  }
  handleFileChange = e => {
    this.setState({videoDetails: e.currentTarget.files[0]})
  }
  render() {
    return (
      <div className="App">
        <input type="file" name="video_file" onChange={this.handleFileChange}/>
        <VideoPreview 
          src={this.state.videoDetails}
          size={10}
          preview={true}
          width={520}
          height={340}
          controls={true}
          autoPlay={true}
        />
      </div>
    );
  }
}
```

# Props

Common props you may want to specify include:

* src - accepts video details
* size - the maximum size of the video file
* preview - preview the video after selected
* width - width of the video player
* height - height of the video player
* controls - enables/disables the default browser controls
* autoPlay - autoplays the video after it gets loaded

# License

MIT Licensed. Copyright (c) Krishna 2018.
