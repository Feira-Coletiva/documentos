# 💾 Backend - Projeto X

## 📂 Estrutura de Pastas

```bash
src/main/java/com/seuprojeto/
├── controller/     # REST Controllers - Endpoints da API
├── service/        # Regras de negócio
├── repository/     # Interfaces de acesso a dados (JpaRepository)
├── model/          # Entidades JPA (mapeamento de tabelas)
└── dto/            # Data Transfer Objects (se houver)
```

> 💡 Obs: Caso use `src/test/java`, organize os testes seguindo o mesmo pacote base.

## ✅ Boas práticas recomendadas

### 📌 Perfis de Ambiente

Crie arquivos de configuração separados para cada ambiente:

```bash
src/main/resources/
├── application.properties          # Configuração geral
├── application-dev.properties      # Ambiente de desenvolvimento
├── application-test.properties     # Ambiente de testes
└── application-prod.properties     # Ambiente de produção
```

Para selecionar o perfil:

```bash
spring.profiles.active=dev
```

### 📌 Configuração de CORS

Se o front-end e back-end estiverem em origens diferentes (exemplo: `localhost:5500` e `localhost:8080`), **habilite o CORS**.

**Exemplo global usando** `WebMvcConfigurer` :

```java
@Configuration
public class CorsConfig implements WebMvcConfigurer {

    @Override
    public void addCorsMappings(CorsRegistry registry) {
        registry.addMapping("/**")
                .allowedOrigins("http://localhost:5500")
                .allowedMethods("GET", "POST", "PUT", "DELETE", "OPTIONS")
                .allowedHeaders("*");
    }
}
```

### 📌 Testes (opcional, mas recomendado)

Estruture os testes em:

```java
src/test/java/com/seuprojeto/
```

- Exemplos de testes possíveis:
    - Testes de controller (@WebMvcTest)
    - Testes de service (@SpringBootTest ou @DataJpaTest)

## ✅ Mesmo testes simples de endpoints e regras de negócio já ajudam muito a evitar bugs futuros.

### 📌 Documentação da API (Swagger / OpenAPI)

Se desejar, documente a API usando Swagger.

Ferramentas recomendadas:

- **springdoc-openapi** (moderno)

- **springfox-swagger** (mais antigo, mas usado ainda)

**Exemplo com SpringDoc**:

1. Adicione a dependência:

```xml
<dependency>
    <groupId>org.springdoc</groupId>
    <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
    <version>2.3.0</version>
</dependency>
```
2. Após iniciar a aplicação, acesse a documentação via:

```properties
http://localhost:8080/swagger-ui/index.html
``` 

**Exemplos de anotações úteis**:

```java
@RestController
@RequestMapping("/api/produtos")
public class ProdutoController {

    @Operation(summary = "Lista todos os produtos")
    @ApiResponses(value = {
        @ApiResponse(responseCode = "200", description = "Lista retornada com sucesso"),
        @ApiResponse(responseCode = "500", description = "Erro interno do servidor")
    })
    @GetMapping
    public List<Produto> listarTodos() {
        return produtoService.listarTodos();
    }
}
```

## ✅ Dicas extras

- Padronize seus commits (ex: seguindo Conventional Commits)
- Mantenha o código limpo e com boas práticas
- Utilize o README.md para documentar endpoints e principais comandos de build/run/test
