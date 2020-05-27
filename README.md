# Design Systems Notebook

Notes and findings on Design Systems and their implementation in different frameworks (HTML, React, Web Components, etc).

## Getting Started

1. `yarn` in the project root to install all dependencies.
1. Navigate to a package: `cd /packages/react`
1. Run Storybook: `yarn storybook`

### Workspaces

This project is setup using Yarn Workspaces. All notebooks are stored in the `/packages/` folder and share dependencies where possible. This also allows us to create packages like a component library (or CSS framework) and use it across multiple libraries.

## Creating Notes

This project uses Storybook Docs for authoring notes in MDX. Each Storybook project is setup with Docs where possible and looks for MDX files in `/<project>/stories/` with the file extensions `.stories.mdx`.

### Template

Here is the basic format of a MDX file:

```mdx
import { Meta, Story, Preview } from '@storybook/addon-docs/blocks';
import { Button } from '../../components/Base/Button';

<Meta title="Components/Button" component={Button} />

# Button

A basic button.

<Preview>
  <Story name="Basic">
    <Button>Test</Button>
  </Story>
</Preview>
```