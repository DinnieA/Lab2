fun main() {
    // Створення мапи коефіцієнтів для валют
    val conversionRates = mapOf(
        "usd" to 0.027,  // Коефіцієнт для USD
        "eur" to 0.025,  // Коефіцієнт для EUR
        "pln" to 0.12    // Коефіцієнт для PLN
    )

    while (true) {
        // Запит користувача на введення суми в гривнях
        println("Введіть суму в гривнях (або 'exit' для виходу):")
        val inputAmount = readLine() ?: ""

        // Якщо користувач вводить "exit", зупиняємо програму
        if (inputAmount.lowercase() == "exit") {
            println("Програма завершена.")
            break
        }

        // Перевірка, чи введено число
        val amount = inputAmount.toDoubleOrNull()
        if (amount == null) {
            println("Введіть коректну кількість!")
            continue
        }

        // Запит користувача на вибір валюти
        println("Оберіть валюту (usd, eur, pln):")
        val currency = readLine()?.lowercase()

        // Виконання конвертації згідно з вибраною валютою
        val result = when (currency) {
            "usd" -> amount * conversionRates["usd"]!!
            "eur" -> amount * conversionRates["eur"]!!
            "pln" -> amount * conversionRates["pln"]!!
            else -> {
                // Якщо валюта некоректна, викидаємо виключення
                println("Некоректна валюта. Спробуйте знову.")
                continue
            }
        }

        // Виведення результату з округленням до 2 знаків
        println("Результат: %.2f".format(result))
    }
}
