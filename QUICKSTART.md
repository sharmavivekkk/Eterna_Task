# Quick Start Guide

## Installation

1. Install dependencies:
```bash
npm install
```

## Development

2. Start the development server:
```bash
npm run dev
```

3. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Features Overview

### Token Table Features

- **Sorting**: Click any column header to sort (Token, Price, 24h Change, Volume, Liquidity)
- **Real-time Updates**: Prices update every 2 seconds with smooth color transitions
- **Interactive Elements**:
  - Click any row to view detailed token information in a modal
  - Hover over truncated addresses to see full address
  - Click info buttons for Final Stretch and Migrated tokens
  - Hover over rows to see external link button

### Token Categories

- **New Pairs** (Green badge): Recently created trading pairs
- **Final Stretch** (Yellow badge): Tokens in final stretch period with countdown
- **Migrated** (Gray badge): Tokens migrated from other addresses

### Loading States

- Initial load shows shimmer skeleton rows
- Progressive loading as data arrives
- Error states with retry functionality

## Performance

- All interactions are optimized for <100ms response time
- Memoized components prevent unnecessary re-renders
- Smooth animations and transitions
- No layout shifts during loading

## Code Structure

The project follows atomic design principles:

- **Atoms**: `components/atoms/` - Smallest reusable components
- **Molecules**: `components/molecules/` - Composite components
- **Organisms**: `components/organisms/` - Complex UI sections
- **Hooks**: `hooks/` - Custom React hooks
- **Utilities**: `lib/` - Shared utilities and store

## Testing

Run type checking:
```bash
npm run type-check
```

Run linting:
```bash
npm run lint
```

## Build for Production

```bash
npm run build
npm start
```

## Notes

- The WebSocket connection is mocked for demonstration purposes
- Token data is generated locally for development
- All components are fully typed with TypeScript strict mode
- The UI is responsive and accessible

