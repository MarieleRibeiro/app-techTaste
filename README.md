# 🍔 TechTaste - Aplicativo de Delivery

<div align="center">
  <img src="assets/logo.png" alt="TechTaste Logo" width="200"/>
  
  ### Aplicativo de delivery de comida desenvolvido em Flutter
  
  [![Flutter Version](https://img.shields.io/badge/Flutter-3.7.0--209.1.beta-blue.svg)](https://flutter.dev/)
  [![Dart SDK](https://img.shields.io/badge/Dart-SDK-0175C2.svg)](https://dart.dev/)
  [![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
</div>

---

## 📥 Download e Teste

### 🚀 Teste o App Agora!

Quer experimentar o TechTaste sem precisar compilar? Baixe o APK pronto:

<div align="center">

**📱 Android APK**

[![Download APK](https://img.shields.io/badge/Download-APK-success?style=for-the-badge&logo=android)](https://github.com/MarieleRibeiro/app-techTaste/releases/download/v1.0.0/app-debug.apk)

**ou encontre o arquivo em:**  
`build/app/outputs/flutter-apk/app-debug.apk`

</div>

### 📋 Como instalar:

1. Baixe o arquivo **app-debug.apk**
2. No seu Android, vá em **Configurações → Segurança**
3. Habilite **"Instalar apps de fontes desconhecidas"**
4. Abra o arquivo APK baixado
5. Toque em **Instalar**
6. Pronto! 🎉

> **Nota:** Este é um APK de debug para testes. Para uso em produção, recomenda-se gerar uma versão release assinada.

---

## 📱 Sobre o Projeto

**TechTaste** é um aplicativo móvel de delivery de comida que permite aos usuários explorar restaurantes, navegar por categorias de pratos e fazer pedidos de forma intuitiva e rápida. O app oferece uma experiência moderna e fluida, com uma interface amigável e recursos completos de carrinho de compras.

### ✨ Funcionalidades Principais

- 🏪 **Exploração de Restaurantes**: Visualize restaurantes bem avaliados com informações detalhadas
- 📂 **Categorias**: Navegue por diferentes categorias (Principais, Petiscos, Bebidas, Sobremesas, Massas)
- 🍕 **Cardápio Detalhado**: Veja os pratos de cada restaurante com descrições e preços
- 🛒 **Carrinho de Compras**: Adicione, remova e gerencie seus pedidos
- ⭐ **Avaliações**: Confira as avaliações e distância de cada restaurante
- 🎨 **Interface Moderna**: Design clean e intuitivo para melhor experiência do usuário

---

## 🏪 Restaurantes Disponíveis

O aplicativo conta com 5 restaurantes parceiros:

1. **🍔 Monstro Burguer** 
   - Hambúrgueres para quem curte a madrugada
   - ⭐ 4.3 | 📍 2 km
   - Categorias: Principais, Petiscos

2. **🌮 Cabrón Mexicano**
   - Autêntica comida mexicana, cheia de sabor e tradição
   - ⭐ 4.7 | 📍 3 km
   - Categorias: Petiscos, Bebidas

3. **🥗 Foodcourt Natural**
   - Alimentação saudável e saborosa
   - ⭐ 5.0 | 📍 1 km
   - Categorias: Principais, Bebidas

4. **🍩 Donutz**
   - Os melhores donuts da cidade!
   - ⭐ 4.8 | 📍 4 km
   - Categorias: Sobremesas, Massas

5. **🍣 Panda Sushi**
   - Sushis e pratos orientais fresquinhos
   - ⭐ 4.9 | 📍 1 km
   - Categorias: Principais, Petiscos, Bebidas

---

## 🏗️ Arquitetura do Projeto

```
lib/
├── data/               # Camada de dados
│   ├── categories_data.dart
│   └── restaurant_data.dart
├── model/              # Modelos de dados
│   ├── dish.dart
│   └── restaurant.dart
├── ui/                 # Interface do usuário
│   ├── _core/          # Componentes compartilhados
│   │   ├── app_colors.dart
│   │   ├── app_theme.dart
│   │   ├── bag_provider.dart
│   │   └── widgets/
│   ├── splash/         # Tela de splash
│   ├── home/           # Tela principal
│   ├── restaurant/     # Tela de restaurante
│   └── checkout/       # Tela de checkout
└── main.dart           # Ponto de entrada da aplicação
```

### 🎯 Padrões Utilizados

- **Provider Pattern**: Gerenciamento de estado reativo
- **Repository Pattern**: Separação da camada de dados
- **Widget Composition**: Componentes reutilizáveis
- **Clean Architecture**: Separação de responsabilidades

---

## 🛠️ Tecnologias e Dependências

### Principais Dependências

```yaml
dependencies:
  flutter: sdk
  provider: ^6.1.2      # Gerenciamento de estado
  badges: ^3.1.2        # Badges para notificações
  cupertino_icons: ^1.0.8
```

### DevDependencies

```yaml
dev_dependencies:
  flutter_test: sdk
  flutter_lints: ^5.0.0
```

---

## 🚀 Como Executar o Projeto

### Pré-requisitos

- Flutter SDK 3.7.0 ou superior
- Dart SDK 3.7.0 ou superior
- Android Studio / VS Code com Flutter plugin
- Emulador Android/iOS ou dispositivo físico

### Instalação

1. **Clone o repositório**
```bash
git clone <url-do-repositório>
cd flutter_techtaste-main
```

2. **Instale as dependências**
```bash
flutter pub get
```

3. **Verifique se há dispositivos disponíveis**
```bash
flutter devices
```

4. **Execute o aplicativo**
```bash
flutter run
```

### Executar em plataformas específicas

```bash
# Android
flutter run -d android

# iOS (apenas em macOS)
flutter run -d ios

# Web
flutter run -d chrome

# Desktop
flutter run -d windows  # Windows
flutter run -d macos    # macOS
flutter run -d linux    # Linux
```

---

## 📂 Estrutura de Dados

### Modelo de Restaurante

```dart
class Restaurant {
  String id;
  String imagePath;
  String name;
  String description;
  double stars;
  int distance;
  List<String> categories;
  List<Dish> dishes;
}
```

### Modelo de Prato

```dart
class Dish {
  String id;
  String name;
  String description;
  int price;
  String imagePath;
}
```

---

## 🎨 Assets

O projeto inclui diversos assets organizados:

```
assets/
├── banners/         # Banners promocionais
├── categories/      # Ícones de categorias
├── dishes/          # Imagens dos pratos
├── restaurants/     # Logos dos restaurantes
├── others/          # Ícones diversos
├── logo.png         # Logo do aplicativo
└── data.json        # Dados dos restaurantes
```

---

## 🔄 Gerenciamento de Estado

O aplicativo utiliza o **Provider** para gerenciamento de estado:

### BagProvider
Gerencia o carrinho de compras com funcionalidades:
- ✅ Adicionar pratos ao carrinho
- ❌ Remover pratos do carrinho
- 🗑️ Limpar carrinho
- 📊 Calcular quantidade de itens

### RestaurantData
Gerencia os dados dos restaurantes:
- 📥 Carregamento de dados do JSON
- 🔄 Notificação de mudanças
- 📋 Lista de restaurantes disponíveis

---

## 🧪 Testes

Execute os testes com:

```bash
# Todos os testes
flutter test

# Testes com cobertura
flutter test --coverage
```

---

## 📱 Telas do Aplicativo

### 1. Splash Screen
Tela inicial de carregamento com logo e animações.

### 2. Home Screen
- Campo de busca
- Categorias navegáveis horizontalmente
- Banner promocional
- Lista de restaurantes bem avaliados

### 3. Restaurant Screen
- Informações do restaurante
- Lista de pratos mais pedidos
- Preços e opção de adicionar ao carrinho

### 4. Checkout Screen
- Lista de itens no carrinho
- Quantidade de cada item
- Botões para adicionar/remover itens
- Opção de limpar carrinho

---

## 🎯 Próximas Funcionalidades

- [ ] Integração com API backend
- [ ] Sistema de autenticação
- [ ] Histórico de pedidos
- [ ] Sistema de pagamento
- [ ] Rastreamento de entrega em tempo real
- [ ] Sistema de avaliações e comentários
- [ ] Filtros avançados de busca
- [ ] Favoritos
- [ ] Notificações push
- [ ] Modo escuro

---

## 👨‍💻 Créditos

Este projeto foi desenvolvido pela **[Alura](https://www.alura.com.br/)** como parte de seus cursos de Flutter.

### 📚 Sobre a Alura
A Alura é a maior plataforma brasileira de cursos online de tecnologia, oferecendo formações completas em desenvolvimento, design, dados e muito mais.

---

<div align="center">
  
  ### ⭐ Se este projeto foi útil para você, considere dar uma estrela!
  
</div>
