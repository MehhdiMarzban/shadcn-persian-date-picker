# Shadcn Persian Date Picker

A beautiful, accessible, and customizable Persian (Jalali) date picker component for React applications built with Shadcn UI components.

![Shadcn Persian Date Picker](https://shadcn-persian-calendar.mehdi-marzban.ir/og.png)

## Demo

Check out the live demo: [https://shadcn-persian-calendar.mehdi-marzban.ir/](https://shadcn-persian-calendar.mehdi-marzban.ir/)

## Features

- 🇮🇷 Persian (Jalali/Shamsi) calendar support
- 🎨 Fully customizable with Tailwind CSS
- 🌙 Dark mode support
- ♿ Accessible (WAI-ARIA compliant)
- 📱 Responsive design
- 🔄 Year switcher
- 📅 Single date, range, and multiple date selection modes
- 🌐 RTL support

## Installation

```bash
npx shadcn add https://shadcn-persian-calendar.mehdi-marzban.ir/persian-calendar.json
```

## Prerequisites

This component is built on top of Shadcn UI components. Make sure you have the following dependencies installed:

```bash
npm install @radix-ui/react-slot lucide-react react-day-picker date-fns
```

## Usage

### Basic Usage

```tsx
"use client";

import { useState } from "react";
import { PersianCalendar } from "@/components/ui/persian-calendar";

export default function Home() {
  const [date, setDate] = useState<Date | undefined>(new Date());

  return (
    <div className="flex min-h-screen flex-col items-center justify-center p-4">
      <PersianCalendar
        mode="single"
        selected={date}
        onSelect={setDate}
        className="rounded-md border"
      />
    </div>
  );
}
```

## Props

The `PersianCalendar` component accepts all props from `react-day-picker/persian` with some additional options:

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `className` | `string` | `""` | Additional CSS classes |
| `showOutsideDays` | `boolean` | `true` | Show days from previous/next months |
| `showYearSwitcher` | `boolean` | `true` | Enable year switcher functionality |
| `yearRange` | `number` | `12` | Number of years to display in year switcher |
| `numberOfMonths` | `number` | `1` | Number of months to display |
| `mode` | `"single" \| "multiple" \| "range" \| "default"` | `"single"` | Selection mode |
| `selected` | `Date \| Date[] \| DateRange \| undefined` | - | Selected date(s) |
| `onSelect` | `(date: Date \| Date[] \| DateRange \| undefined) => void` | - | Selection change handler |

Plus all styling class props for customizing different parts of the calendar.

## Customization

The component is built with Tailwind CSS and can be fully customized by passing class names to the appropriate props:

```tsx
<PersianCalendar
  className="rounded-xl border shadow-lg"
  monthsClassName="gap-2"
  dayClassName="text-base"
  selectedClassName="bg-blue-500 text-white"
  // ... other styling props
/>
```

## Contributing

Contributions are welcome! If you'd like to help improve this component, please feel free to submit a pull request.

## License

MIT

---

For more information, visit the [demo site](https://shadcn-persian-calendar.mehdi-marzban.ir/).

If you have any suggestions or would like to contribute to make this component even better, please don't forget to submit a pull request. Your help is greatly appreciated!
