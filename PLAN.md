## YNAB Dash
I'd like to see my monthly spending aggregated by category group and by daily spending.
This would allow me to see:
1. How much I am spending based on the broad themes that I use category groups for (e.g., "Wants" vs. "Needs")
2. What days of the week I tend to spend the most on (mainly for curiosity)
3. When my spending occurs during the month (how fast am I spending through my assigned money)

### Module Structure
```
src
  common
    tab-nav
      TabNav
    components
      Header
      Footer
      PageContainer
  pages
    budget-selector
        BudgetSelectorPage
    dash
        tabs
          transactions
            TransactionsTab
            components
          categories
            CategoriesTab
            components
          daily
            DailyTab
            components
        DashPage
  App
```