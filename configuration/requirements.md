---
icon: markdown
description: >-
  Requirements enables conditional checks based on various parameters, such as
  player permissions, numeric values, and custom conditions. can be used on
  click or view on requirements of buttons
---

# Requirements



{% hint style="info" %}
Requirement object is the same for view and click requirements, which means you can put it anywhere you need
{% endhint %}

## Operators

| Operator                           | Example                                                                                |
| ---------------------------------- | -------------------------------------------------------------------------------------- |
| EXISTS (exists)                    | `"%balance% exists"`                                                                   |
| GREATER\_THEN (>)                  | `"%balance% > 10"`                                                                     |
| GREATER\_THAN\_OR\_EQUAL (=> , >=) | `"%balance% >= 10"`                                                                    |
| LESS\_THAN\_OR\_EQUAL (<= , = <)   | `"%balance% =< 10"`                                                                    |
| LESS\_THAN (<)                     | `"balance% > 10"`                                                                      |
| EQUALS (= , == , ===)              | `"balance% = 10"`                                                                      |
| NOT\_EQUALS (!= , !== , !===)      | `"balance% != 10"`                                                                     |
| CONTAINS (contains)                | `"%status% contains afk"`                                                              |
| NOT\_CONTAINS (!contains)          | `"%status% !contains afk"`                                                             |
| IS (:)                             | <p>permission: "permission.needed"<br>permission: "!permission.user.shouldnt.have"</p> |
