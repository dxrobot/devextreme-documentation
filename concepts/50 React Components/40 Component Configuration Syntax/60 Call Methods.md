To call UI component methods, you need the UI component instance. Create a <a href="https://reactjs.org/docs/refs-and-the-dom.html" target="_blank">ref</a> and attach it to the target component via the `ref` property. Implement a getter that returns the instance taken from the ref. In the following code, this approach is used to get a `TextBox` instance:
    
    <!-- tab: App.js -->
    import Button from 'devextreme-react/button';
    import TextBox from 'devextreme-react/text-box';

    class App extends React.Component {
        constructor(props) {
            super(props);
            
            this.textBoxRef = React.createRef();
            
            this.focusTextBox = () => {
                this.textBox.focus()
            };
        }

        get textBox() {
            return this.textBoxRef.current.instance;
        }

        render() {
            return (
                <div>
                    <TextBox ref={this.textBoxRef} />
                    <Button text="Focus TextBox" onClick={this.focusTextBox} />
                </div>
            );
        }
    }

Alternatively, you can assign the UI component instance to a variable and use it to call the methods. This approach is not compatible with <a href="https://reactjs.org/docs/hooks-intro.html" target="_blank">React Hooks</a>.

    <!-- tab: App.js -->
    import Button from 'devextreme-react/button';
    import TextBox from 'devextreme-react/text-box';

    class App extends React.Component {
        constructor(props) {
            super(props);
            
            this.saveTextBoxInstance = this.saveTextBoxInstance.bind(this);
            this.focusTextBox = this.focusTextBox.bind(this);
        }

        saveTextBoxInstance(e) {
            this.textBoxInstance = e.component;
        }

        focusTextBox() {
            this.textBoxInstance.focus();
        }

        render() {
            return (
                <div>
                    <TextBox onInitialized={this.saveTextBoxInstance} />
                    <Button text="Focus TextBox" onClick={this.focusTextBox} />
                </div>
            );
        }
    }

If you use <a href="https://reactjs.org/docs/hooks-intro.html" target="_blank">React Hooks</a>, implement the <a href="https://reactjs.org/docs/hooks-reference.html#useref" target="_blank">useRef</a> hook and attach it to the target component via the `ref` property:

    <!-- tab: App.js -->
    import Button from 'devextreme-react/button';
    import TextBox from 'devextreme-react/text-box';
    import React, { useRef } from 'react';

    export default function App() {      
        const textBox = useRef(null);
        const focusTextBox = () => {
            textBox.current.instance.focus();
        };
        return (
            <div>
                <TextBox ref={textBox} />
                <Button text="Focus TextBox" onClick={focusTextBox} />
            </div>
        );       
    }
