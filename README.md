package com.example.app

import android.content.Intent
import android.os.Bundle
import androidx.appcompat.app.AppCompatActivity
import androidx.cardview.widget.CardViewa

class AppActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_app)

        // Хичээлийн карт дээр дарах үйлдэл
        val cardLesson = findViewById<CardView>(R.id.cardLesson)
        cardLesson.setOnClickListener {
            val intent = Intent(this, LessonActivity::class.java)
            startActivity(intent)
        }

        // Сорил өгөх карт дээр дарах үйлдэл
        val cardQuiz = findViewById<CardView>(R.id.cardQuiz)
        cardQuiz.setOnClickListener {
            val intent = Intent(this, QuizActivity::class.java)
            startActivity(intent)
        }
    }
}
