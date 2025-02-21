# Spacecraft Builder

_Build a spacecraft inventory by adding items with quantity and purpose, plus receive real-time validation feedback. View the live inventory and delete from it._

<table>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1n33hmBGqHMDrVW_bt1ljW5fqBQhrxagW" alt="Initial Page Load" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1487Bh6BNSnFpEleIYyGI2TsCGl_o5DmA" alt="Validation Errors" width="500px" />
    </td>
  </tr>

  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=14kfCukOwW9U3uxnmI1eUZPVjjzvKj99M" alt="Active Inventory" width="500px" />
    </td>
  </tr>
</table>

[Click here to watch the demo video](https://drive.google.com/file/d/1-hLljuKJuVknGAU6E5H1IKTk4pcgeTyO/view?usp=drive_link)

## Summary:

### **React Forms Practice with:**

- Building forms with React
- Component-based architecture
- State management
- Handling user inputs
- Managing interactions between parent and child components

### **Component Architecture**

- SpacecraftBuilder --> ItemForm
- SpacecraftBuilder --> InventoryDisplay
- InventoryDisplay --> ItemCard
- InventoryDisplay --> ItemAction

### **State Management**

SpacecraftBuilder

- top-level component for state
- manages state for items array, passing down props to children components
- initializes generateId() and passes to children

ItemForm

- manages state for formData
- passes data **up** to SpacecraftBuilder to add items
- manages error handling for input validations using state and conditional logic

ItemAction

- renders a button on an item; when clicked, uses setItems() from SpacecraftBuilder to remove an item by its id
