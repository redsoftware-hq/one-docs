# **Custom Scripts & Formatting Functions in OneLead**

OneLead supports **custom scripts** to process and format lead data before saving it into the CRM. These functions help with **data validation, transformation, and automation**.

This guide covers:
- **Built-in functions available in OneLead**
- **How to use formatting functions in Lead Mapping**
- **Creating custom functions**
- **Best practices for customization**

---

## **Built-in Formatting Functions**
The following functions are available and can be applied during **Lead Mapping**.

| **Function Name** | **Description** |
|------------------|---------------|
| **format_phone_number** | Formats a phone number into `+country_code-local_number` format and ensures validity. takes param value default_region if not passed it's "IN"|
| **calculate_age** | Calculates age based on date of birth. |
| **extract_country_from_address** | Extracts the country name from an address string. |
| **add_prefix** | Adds a prefix to a value if not empty. |
| **capitalize_name** | Capitalizes the first letter of each word in a name. |
| **current_date** | Returns the current date. |

---

## **Using Formatting Functions in Lead Mapping**
To apply a formatting function:
1. Go to **"Meta Ads Page Config"** > **"Quick Map Lead Fields"**.
2. Select the desired function in the **Formatting Function** column.
3. The function will automatically transform the lead data before saving.

---

## **Creating Custom Formatting Functions**
You can create custom functions and register them for use in OneLead.

### **Steps to Add a New Function**
1. Define a **Python function**.
2. Use the `@register_function("function_name")` decorator.
3. The function becomes available in **OneLead’s Formatting Function dropdown**.

**Example: Convert Text to Uppercase**
```python
@register_function("convert_to_uppercase")
def convert_to_uppercase(value):
    return value.upper() if value else value
```

---

## **Best Practices**
✔️ Keep function logic **simple and efficient**.  
✔️ Handle **edge cases** (e.g., missing values, incorrect formats).  
✔️ Use **error handling** (`try-except`) to prevent failures.  
✔️ Test functions before applying them to live data.  

---

## **Future Enhancements (Upcoming: low priority)**
- **Dynamic Function Parameters:** Define parameters via UI.
- **Function Chaining:** Apply multiple functions sequentially.
- **Additional Built-in Helpers:** Date formatting, currency conversion, etc.
- Contributions are always welcome.

---

## **Next Steps**
- [Meta Form Mapping](../meta/meta_form_mapping.md)
- [Meta Webhook Lead Logs](../meta/meta_webhook_lead_logs.md)

