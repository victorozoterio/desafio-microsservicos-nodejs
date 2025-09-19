# Como rodar o projeto

- na pasta raiz do projeto, execute `docker-compose up -d`;
- na pasta app-orders, execute `npm install` e depois `npm run dev`;
- na pasta app-invoices, execute `npm install` e depois `npm run dev`;

# Como funciona o projeto

- o projeto é composto por dois microsserviços: orders e invoices;
- o microsserviço orders é responsável por receber as ordens de compra e persistir no banco de dados;
- o microsserviço invoices é responsável por gerar as faturas a partir das ordens de compra;
- o microsserviço orders expõe a rota `/orders` para receber as ordens de compra;
- o microsserviço invoices expõe a rota `/invoices` para gerar as faturas;
- acesse http://localhost:8002` para entrar na interface do Kong;
- acesse `http://localhost:8000/orders/health` para verificar se o serviço de orders está funcionando;
- acesse `http://localhost:8000/invoices/health` para verificar se o serviço de invoices está funcionando;
