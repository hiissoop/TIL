- styling
    - index.js
    
    ```jsx
    import { Parent, Child, firstChildStyle } from "../../../styles/emotion2";
    
    export default function BoardWriteUI() {
    
      return (
        <div>
          <Parent>
            <Child css={firstChildStyle}>green</Child>
            <Child>green2</Child>
          </Parent>
          <Child>red</Child>
        </div>
      );
    }
    ```
    
    - style.js
    
    ```jsx
    import { jsx } from "@emotion/react";
    import styled from "@emotion/styled";
    import { css } from '@emotion/react';
    
    export const Parent = styled.div`
     width: 500px;
     height: 500px;
     border: 1px solid red;
    `
    
    export const Child = styled.div`
    color: green;
    `
    
    export const firstChildStyle = css`
      margin-bottom: 12px;
    `;
    ```