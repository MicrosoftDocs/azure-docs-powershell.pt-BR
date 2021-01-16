---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271968"
---
# Get-AzMariaDbConnectionString

## Sinopse
Obtenha a cadeia de conexão de um MariaDB em uma determinada estrutura.

## SYNTAX

### ServerName (padrão)
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ServerObject
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## DESCRITIVO
Obtenha a cadeia de conexão de um MariaDB em uma determinada estrutura.

## EXEMPLOS

### Exemplo 1: obter uma cadeia de conexão de MariaDB
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

Esse comando obtém uma cadeia de conexão de MariaDB.

### Exemplo 2: obter uma cadeia de conexão de MariaDB
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

Esse comando obtém uma cadeia de conexão de MariaDB.

## OS

### -Cliente
Conectar o tipo de cliente

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
Region Defaultparameters as credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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
Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
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
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos que contém o recurso.

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da assinatura faz parte do URI para cada chamada de serviço

```yaml
Type: System.String
Parameter Sets: ServerName
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

### Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer

## EXIBE

### System. String

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTobject <IServer> : parâmetro de identidade
  - `Location <String>`: O local em que o recurso reside.
  - `[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valor chave.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor. Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).
  - `[EarliestRestoreDate <DateTime?>]`: Hora de criação do ponto de restauração mais antiga (formato ISO8601)
  - `[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.
  - `[IdentityType <IdentityType?>]`: O tipo de identidade. Defina como "SystemAssigned" para criar e atribuir automaticamente uma entidade de segurança do Azure Active Directory para o recurso.
  - `[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.
  - `[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.
  - `[ReplicationRole <String>]`: A função de replicação do servidor.
  - `[SkuCapacity <Int32?>]`: A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.
  - `[SkuFamily <String>]`: A família de hardware.
  - `[SkuName <String>]`: O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.
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

