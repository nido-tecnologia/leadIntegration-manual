# Integração de Fomulários diversos (NIDOImóvel)
Manual de Integração

***Segue o mesmo padrão de necessidades da integração de Leads porem apenas com os campos enviados no JSON sendo diferentes, para saber sobre o processo convencional de integração: [CLIQUE AQUI](./README.md)***

## Itens Diferenciados
- \_\_ENDPOINT_CLIENTE__
   - Ex: http://sistemadocliente.nidoimovel.com.br/index.php/api/siteFormsIntegration
   
## Retornos da aplicação
|Status|Descrição|
|-:|-|
|201|Sucesso|
|40x|Problemas na validação dos dados enviados|
|50x|Problema de Token ou Problema Genérico|
   
## Campos do JSON
 - **id**, identificador do formulário no site
 - **created_at**, data de criação do formulário, formato *YYYY-MM-DD HH:MM:SS*
 - **formType**, codigo do tipo de formulário cadastrado no sistema (tabela 1 **)
 - **formData**, array livre contendo todos os campos do formulário

---

`** Tabela 1`

Os tipos de formulário são um cadastro livre no sistema porem vem com uma carga padrão com os seguintes tipos:

  | codigo | descrição           |
  |-------:|:-------------------:|
  |      1 | Fale Conosco        |
  |      2 | Trabalhe Conosco    |
  |      3 | Cadastrar Imóvel    |
  |      4 | Indicação de Imóvel |
