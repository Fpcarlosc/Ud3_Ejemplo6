# Ud3_Ejemplo6
_Ejemplo 6 de la Unidad 3._ 

Vamos a ver el ciclo de vida de una Actividad usando mensajes de _Log_. 
Para ello sólo tenemos que ver el fichero _MainActivity.java_:
```
public class MainActivity extends AppCompatActivity {

    public static final String LOG_TAG = "MainActivity: ";

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Log.v(LOG_TAG, "onCreate");
    }

    @Override
    protected void onStart() {
        super.onStart();

        Log.v(LOG_TAG, "onStart");
    }

    @Override
    protected void onResume() {
        super.onResume();

        Log.v(LOG_TAG, "onResume");
    }

    @Override
    protected void onPause() {
        super.onPause();

        Log.v(LOG_TAG, "onPause");
    }

    @Override
    protected void onStop() {
        super.onStop();

        Log.v(LOG_TAG, "onStop");
    }

    @Override
    protected void onDestroy() {
        super.onDestroy();

        Log.v(LOG_TAG, "onDestroy");
    }
}
```

Como podemos ver se han sobreescrito los métodos _callback_ de los estados de la aplicación, de tal forma que podremos ver en la
consola de _Logcat_ cómo la aplicación va pasando de un estado a otro. 

Haremos pruebas como pulsar en el botón de _Home_, ir hacia atrás, volver a la aplicación, etc.
