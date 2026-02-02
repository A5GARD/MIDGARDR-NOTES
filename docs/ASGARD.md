


What started as a React UI components library has evolved into a full-stack development toolkit. As such, it has now transitioned into an SDK and even though it sounds like everything just got more complicated, it has actually made things far simpler and easier.

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> **ASGARD SDK**
 
## Architecture

The SDK is built on three foundational layers:

- **UI Components** - Everything that returns JSX/renders to DOM
- **Services** - External integrations and business logic
- **Utilities** - App-layer infrastructure

Complemented by VSCode extensions and NPM packages that streamline development workflows.

## Design Philosophy

**Flat over nested.** Sub-categories (E-Commerce, Core, Marketing) work well for small libraries but create unnecessary complexity at scale. All nested structures have been flattened to root-level categories or merged into existing ones.

**Norse mythology naming** embraced throughout - from the SDK name (Asgard) to individual packages.

**Category-first organization.** While the codebase serves three architectural layers, the file structure prioritizes categorical clarity over hierarchical depth. This scales better and reduces cognitive overhead.
