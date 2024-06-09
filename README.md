# L24Compiler
A compiler about L24
<program> = "main" "{" <stmt_list> "}"
<stmt_list> = {<stmt> ";"}
<stmt> = <assign_stmt>| <if_stmt> |<while_stmt> |<scan_stmt> | <print_stmt> 
<assign_stmt> = <ident> "=" <expr> 
<if_stmt> = "if" "("<bool_expr>")" "then" "{"<stmt_list>"}" "end"
               |"if" "("<bool_expr>")" "then" "{"<stmt_list>"}" "else" "{"<stmt_list>"}" "end"
<while_stmt> = "while" "("<bool_expr>")" "{"<stmt_list>"}"
<scan_stmt> = "scan" "(" <ident {"," <ident>} ")" 
<print_stmt> = "print" "(" <expr> {"," <expr>} ")" 
<bool_expr> = <expr> ("=="|"!="|"<"|"<="|">"|">=") <expr>
<expr> = ["+"|"-"] <term> {("+"|"-") <term>}
<term> = <factor> {("*"|"/") <factor>}
<factor> = <ident> | <number> | "("<expr>")"
