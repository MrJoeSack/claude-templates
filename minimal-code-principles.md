# Guiding Principles for AI-Assisted Development

When contributing to this project with the help of AI assistants, please follow these core principles to ensure efficient, maintainable, and well-integrated code.

## The Primary Goal: Minimal Generated Code

**Write the absolute minimum amount of new code required to implement a feature.**

AI assistants should focus on integrating with and calling our existing high-level infrastructure rather than generating entire modules from scratch. This approach:
- Reduces bugs by leveraging tested code
- Simplifies maintenance through consistent patterns
- Lowers the context required for follow-up prompts
- Ensures faster development cycles

## Leverage the Existing Infrastructure

Our project features a robust, opinionated infrastructure that handles common functionalities:
- CRUD operations
- Authentication and authorization
- Data services and validation
- API routing and middleware
- Error handling and logging

Always default to using these existing patterns and services. For example:
- Instead of writing a new API endpoint from scratch, add a new function to the existing service layer
- Use established data access patterns rather than creating new database queries
- Extend existing validation schemas instead of building new ones

## Maintain Unified Context (Monorepo)

Our front-end and back-end code are intentionally kept in a single repository. This architectural decision provides AI assistants with complete context, leading to:
- More cohesive code generation
- Correct integration between layers
- Consistent naming and patterns across the stack

When prompting AI, provide files from both front-end and back-end when relevant to ensure the assistant understands the full context of your request.

## Prioritize Simplicity in the Tech Stack

Our technology choices are optimized for effective AI collaboration:
- **Plain JavaScript (ES6+)** over TypeScript for clearer, more direct code
- Simple, proven libraries over complex frameworks
- Explicit patterns over implicit conventions

AI assistants should always:
- Generate code that matches the existing language and style
- Follow established patterns found in the codebase
- Avoid introducing new dependencies or paradigms

Remember: The best AI-generated code is the code that seamlessly integrates with what already exists, not code that reinvents the wheel.