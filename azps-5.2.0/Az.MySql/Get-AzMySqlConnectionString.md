---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: d6dda5e26603c2276210e4bf00b8b9c040568f12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262485"
---
# Get-AzMySqlConnectionString

## Sinopse
Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.

## SYNTAX

### Get (padrão)
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## DESCRITIVO
Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.

## EXEMPLOS

### Exemplo 1: obter cadeia de conexão do servidor MySql por grupo de recursos e nome do servidor
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

Este cmdlet obtém a cadeia de conexão do servidor MySql por grupo de recursos e nome do servidor.

### Exemplo 2: obter a cadeia de conexão do servidor MySql por identidade
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

Esse cmdlet obtém a cadeia de conexão do servidor MySql por identidade.

## OS

### -Cliente
Provedor de conexão do cliente.

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
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
O objeto do servidor de origem do qual criar a réplica.
Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
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
O nome do grupo de recursos que contém o recurso, você pode obter esse valor da API do Azure Resource Manager ou do Portal.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer

## EXIBE

### System. String

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTobject <IServer> : o objeto do servidor de origem para o qual criar a réplica.
  - `Location <String>`: A localização geográfica onde reside o recurso
  - `SkuName <String>`: O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.
  - `[Tag <ITrackedResourceTags>]`: Marcas do recurso.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor. Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).
  - `[EarliestRestoreDate <DateTime?>]`: Hora de criação do ponto de restauração mais antiga (formato ISO8601)
  - `[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.
  - `[IdentityType <IdentityType?>]`: O tipo de identidade. Defina como "SystemAssigned" para criar e atribuir automaticamente uma entidade de segurança do Azure Active Directory para o recurso.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Status que mostra se o servidor habilitou a criptografia de infraestrutura.
  - `[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão do TLS mínima para o servidor.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é ou não permitido para este servidor. O valor é opcional, mas se transmitido, deve ser ' Enabled ' ou ' disabled '
  - `[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.
  - `[ReplicationRole <String>]`: A função de replicação do servidor.
  - `[SkuCapacity <Int32?>]`: A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.
  - `[SkuFamily <String>]`: A família de hardware.
  - `[SkuSize <String>]`: O código de tamanho a ser interpretado pelo recurso conforme apropriado.
  - `[SkuTier <SkuTier?>]`: A camada do SKU específico, por exemplo, básico.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Habilite a imposição de SSL ou não quando se conectar ao servidor.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilite a redundância geográfica ou não para o backup do servidor.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o aumento automático do armazenamento.
  - `[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.
  - `[UserVisibleState <ServerState?>]`: Um estado de um servidor que é visível para o usuário.
  - `[Version <ServerVersion?>]`: Versão do servidor.

## LINKS RELACIONADOS

