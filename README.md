Saiku-fullscreen
================

A Saiku UI Fullscreen plugin. For when you would like to show tables and graphs for an audience in a presentation.

Some of the rendering plugins I've made, makes best use of large screen real estate. This is a fairly simple plugin utilizing the [fullscreen API](https://developer.mozilla.org/en-US/docs/Web/Guide/API/DOM/Using_full_screen_mode).

This is a very early release. It is not done yet. Do not install and expect production quality. It will require something more recent than a stone age browser. Chrome and Firefox has had this for some years, but I am not sure when IE got support for it.

The plugin should be improved by having som css rules, to increase font sizes in some of the visualizations. How to add fullscreen pseudo classes is documentet in before mentioned link.

I have been thinkin of implementing key press detection of arrow keys, so one could walk through the open tabs in Saiku. Then one could prepare a presentation, where the tabs became sort of "slides".

Installation
------------
- Clone into your saiku-ui/js/saiku/plugins/ folder.
- Create this line inside the index.html

        <!-- Saiku plugins -->
        <script type="text/javascript" src="js/saiku/plugins/Fullscreen/plugin.js" defer></script>
- Some css is needed as well. This is where customization is needed. I haven't figured out any one size fits all rules yet.

        /*For some weird reason you can not have all css queries
        separated by commas, and have just one of these...*/
        .workspace_results:fullscreen {
          width: 100%;
          height: 100%;
          background-color: #FFF;  
        }
        .workspace_results:-moz-full-screen {
          width: 100%;
          height: 100%;
          background-color: #FFF;
        }
        .workspace_results:-webkit-full-screen {
          width: 100%;
          height: 100%;
          background-color: #FFF;
        }
        .workspace_results:fullscreen table {
            margin: 0 auto;
            font-size: 200%;
        }
        .workspace_results:-webkit-full-screen table {
            margin: 0 auto;
            font-size: 200%;
        }
        .workspace_results:-moz-full-screen table {
            margin: 0 auto;
            font-size: 200%;
        }
