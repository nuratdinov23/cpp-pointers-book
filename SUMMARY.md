# Summary

[О книге](README.md)

---

# Введение и Архитектура Проекта
- [Инструкция проекта (Свод правил)](project-instructions.md)
- [Контекст проекта (База знаний)](project-context.md)

---

# Этап 0. Фундамент

## Глава 0.1. Память и объекты
- [Т1. Память, байт, адрес](topics/T1_memory_byte_address.md)
- [Т2. Переменная, объект, тип, sizeof](topics/T2_variable_object_type_sizeof.md)

## Глава 0.2. Время жизни и ошибки
- [Т3. Стек, куча, статическая память; время жизни, область видимости](topics/T3_storage_duration_lifetime_scope.md)
- [Т4. UB; ошибки компиляции, линковки, выполнения; lvalue/rvalue](topics/T4_ub_errors_lvalue_rvalue.md)

---

# Этап 1. Базовые указатели

## Глава 1.1. Указатель как значение и объект
- [Т5.1. Указатель: объявление, инициализация, присваивание; &, *; nullptr; размер](topics/T5.1_pointer_basics_nullptr.md)
- [Т5.2. Состояния указателя; сравнение; вывод](topics/T5.2_pointer_states_comparison.md)
- [Т6. Указатели и const, volatile, constexpr](topics/T6_pointers_const_volatile_constexpr.md)

## Глава 1.2. Смежные понятия
- [Т7. Указатель и ссылка](topics/T7_pointer_and_reference.md)
- [Т8. Указатель на указатель](topics/T8_pointer_to_pointer.md)
- [Т9. void*](topics/T9_void_pointer.md)

---

# Этап 2. Арифметика, массивы, память, функции, строки

## Глава 2.1. Арифметика и массивы
- [Т10. Арифметика указателей](topics/T10_pointer_arithmetic.md)
- [Т11.1. Массивы и decay](topics/T11.1_arrays_and_decay.md)
- [Т11.2. Указатель на массив T(*)[N], многомерные массивы](topics/T11.2_pointer_to_array_multidimensional.md)

## Глава 2.2. Динамическая память
- [Т12.1. new/delete, new[]/delete[], утечки, двойное удаление](topics/T12.1_new_delete_leaks_double_free.md)
- [Т12.2. malloc/free](topics/T12.2_malloc_free.md)

## Глава 2.3. Функции и строки
- [Т13. Указатели и функции: параметры, возврат, T**, T*&, висячие указатели](topics/T13_pointers_and_functions.md)
- [Т14. C-строки: char*, const char*, '\0', литералы, <cstring>](topics/T14_c_strings.md)

---

# Этап 3. Классы

## Глава 3.1. Указатели и объекты
- [Т15.1. Указатель на объект, ->, this](topics/T15.1_pointer_to_object_arrow_this.md)
- [Т15.2. Связные структуры](topics/T15.2_linked_data_structures.md)

## Глава 3.2. Полиморфизм и копирование
- [Т16. Наследование и полиморфизм через указатели: virtual, виртуальный деструктор, срез](topics/T16_inheritance_polymorphism_virtual.md)
- [Т17. Глубокое и поверхностное копирование, правило трёх](topics/T17_copying_rule_of_three.md)

---

# Этап 4. Указатели на функции и члены

- [Т18. Указатели на функции: callback, таблицы, лямбда без захвата](topics/T18_function_pointers_callbacks.md)
- [Т19. Указатели на члены класса (поля и методы), .* и ->*](topics/T19_pointers_to_members.md)

---

# Этап 5. Умные указатели

## Глава 5.1. Владение и RAII
- [Т20.1. RAII](topics/T20.1_raii_concept.md)
- [Т20.2. Семантика перемещения (минимум)](topics/T20.2_move_semantics_basics.md)
- [Т20.3. Правила пяти и нуля](topics/T20.3_rules_of_five_and_zero.md)

## Глава 5.2. Стандартные умные указатели
- [Т21. std::unique_ptr](topics/T21_std_unique_ptr.md)
- [Т22. std::shared_ptr](topics/T22_std_shared_ptr.md)
- [Т23.1. std::weak_ptr, циклические ссылки](topics/T23.1_std_weak_ptr_cycles.md)
- [Т23.2. Умные указатели в интерфейсах](topics/T23.2_smart_pointers_in_interfaces.md)

---

# Этап 6. Приведения, устройство, библиотека, диагностика

## Глава 6.1. Приведения и представление
- [Т24.1. static_cast, up/downcast](topics/T24.1_static_cast.md)
- [Т24.2. dynamic_cast, RTTI](topics/T24.2_dynamic_cast_rtti.md)
- [Т24.3. const_cast, reinterpret_cast, uintptr_t, Си-приведение](topics/T24.3_const_reinterpret_c_casts.md)
- [Т25. Strict aliasing, выравнивание, type punning, bit_cast](topics/T25_strict_aliasing_alignment_type_punning.md)

## Глава 6.2. Под капотом
- [Т26.1. Адресное пространство, кадр стека](topics/T26.1_address_space_stack_frame.md)
- [Т26.2. vptr/vtable](topics/T26.2_vptr_vtable.md)
- [Т26.3. Padding](topics/T26.3_structure_padding.md)
- [Т26.4. Аллокатор кучи](topics/T26.4_heap_allocator.md)

## Глава 6.3. Библиотека и диагностика
- [Т27.1. Итераторы, data(), инвалидация](topics/T27.1_iterators_data_invalidation.md)
- [Т27.2. string_view, span](topics/T27.2_string_view_span.md)
- [Т28. Диагностика: предупреждения компилятора, санитайзеры, Valgrind, отладчик](topics/T28_diagnostics_sanitizers_debuggers.md)

---

# Этап 7. Итог

- [Т29.1. Сводные сравнительные таблицы](topics/T29.1_summary_tables.md)
- [Т29.2. Итоговая практика](topics/T29.2_final_practice.md)
- [Т30. Указатели в Unreal Engine 5 (по желанию)](topics/T30_pointers_in_ue5.md)
