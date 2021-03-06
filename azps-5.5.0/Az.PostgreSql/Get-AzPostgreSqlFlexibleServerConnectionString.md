---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConnectionString.md
ms.openlocfilehash: 3f8750892fd0c23c57fb9343b07a2829cb9706e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117267"
---
# Get-AzPostgreSqlFlexibleServerConnectionString

## Sinopse
Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.

## Sintaxe

### Obter (Padrão)
```
Get-AzPostgreSqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlFlexibleServerConnectionString -Client <String> -InputObject <IServerAutoGenerated>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Descrição
Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.

## Exemplos

### Exemplo 1: Obter cadeia de conexão por nome
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnectionString -Client ADO.NET -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

Server=postgresql-test.postgres.database.azure.com;Database={your_database};Port=5432;User Id=adminuser;Password={your_password};
```

Este cmdlet mostra a cadeia de conexão de um cliente pelo nome do servidor.

### Exemplo 2: Obter cadeia de conexão do servidor PostgreSql por identidade
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlFlexibleServerConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh password={your_password} sslmode=require
```

Este cmdlet obtém cadeia de conexão do servidor PostgreSql por identidade.

## Parâmetros

### -Cliente
Provedor de conexão de cliente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
O servidor para a cadeia de conexão Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
O nome do servidor.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da assinatura que identifica uma assinatura do Azure.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated

## Saídas

### System.String

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT: <IServerAutoGenerated> o servidor para a cadeia de conexão
  - `Location <String>`: a localização geográfica onde o recurso reside
  - `[Tag <ITrackedResourceTags>]`: Marcas de recurso.
    - `[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.
  - `[AdministratorLogin <String>]`: o nome de logon do administrador de um servidor. Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).
  - `[AdministratorLoginPassword <String>]`: a senha de logon do administrador (necessária para a criação do servidor).
  - `[AvailabilityZone <String>]`: informações de zona de disponibilidade do servidor.
  - `[CreateMode <CreateMode?>]`: o modo para criar um novo servidor PostgreSQL.
  - `[DelegatedSubnetArgumentSubnetArmResourceId <String>]`: ID de recurso de arm da sub-rede delegada.
  - `[DisplayName <String>]`: o nome de exibição de um servidor.
  - `[HaEnabled <HaEnabledEnum?>]`: o valor da contagem de stand by pode ser habilitado ou desabilitado
  - `[IdentityType <ResourceIdentityType?>]`: o tipo de identidade.
  - `[MaintenanceWindowCustomWindow <String>]`: indica se a janela personalizada está habilitada ou desabilitada
  - `[MaintenanceWindowDayOfWeek <Int32?>]`: dia da semana para janela de manutenção
  - `[MaintenanceWindowStartHour <Int32?>]`: hora de início da janela de manutenção
  - `[MaintenanceWindowStartMinute <Int32?>]`: minuto de início da janela de manutenção
  - `[PointInTimeUtc <DateTime?>]`: Restaure o tempo de criação de ponto (formato ISO8601), especificando o tempo de restauração.
  - `[PropertiesTag <IServerPropertiesTags>]`: Metadados específicos do aplicativo na forma de pares de valor-chave.
    - `[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.
  - `[SkuName <String>]`: O nome da sKU, normalmente, tier + família + cores, por exemplo, Standard_D4s_v3.
  - `[SkuTier <SkuTier?>]`: o nível da SKU específica, por exemplo, imbatível.
  - `[SourceServerName <String>]`: O nome do servidor PostgreSQL de origem a ser restaurado.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Backup de dias de retenção para o servidor.
  - `[StorageProfileStorageMb <Int32?>]`: armazenamento máximo permitido para um servidor.
  - `[Version <ServerVersion?>]`: Versão postgreSQL Server.

## LINKS RELACIONADOS

