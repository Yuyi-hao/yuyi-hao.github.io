---
layout: default
title: PROJECTS
icon: fas fa-briefcase
order: 2
---

# Projects

<div class="container-fluid px-0">
    <div class="row row-cols-1 row-cols-md-2 row-cols-xl-2 g-4 mb-4">
        {% for project in site.data.projects_list %}
            <div class="col">
                {% include project_card.html
                    project=project
                %}
            </div>
        {% endfor %}
    </div>
</div>







1. Cycle-gan <python ml torch ghibli>
2. Pomodoro <html css js>
3. clock-using-js <html css js>
4. snog0 <go, raylib>
5. Checker <python raylib>
6. wordflow <python flask html css js>
7. Memory Game <python pygame>
8. cat-extension <chrome extension js css>
9. simple-js-site <html css js>
10. Fiblock <>
11. Game of life 
12. Polyrythemic sound <python tkinter>
13. breakout <zig sdl>
14. hide-info-png
15. Todo-cli
16. password-generator
17. ytHistoryAnalyzer 
18. Login-Form css
19. hand-written-digit recogination
20. colorfinerhexcode
21. card-order-summary 
22. Speed test gui
23. Random recipices
24. Python-book solution 
25. sudoku_solver
26. Hangman 
27. Tic-Tac-Toe
28. digital-clock
29. space-war
30. joke-generator