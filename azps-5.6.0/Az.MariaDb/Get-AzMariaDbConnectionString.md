---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 6b0aad7829dc337869c26656135d039b5f74974f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889263"
---
# Get-AzMariaDbConnectionString

## SYNOPSIS
Obter cadeia de conexão de um MariaDB em uma determinada estrutura.

## SINTAXE

### ServerName (Padrão)
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ServerObject
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## DESCRIPTION
Obter cadeia de conexão de um MariaDB em uma determinada estrutura.

## EXEMPLOS

### Exemplo 1: Obter uma cadeia de caracteres de conexão de MariaDB
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

Este comando obtém uma cadeia de caracteres de conexão de MariaDB.

### Exemplo 2: Obter uma cadeia de caracteres de conexão de MariaDB
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

Este comando obtém uma cadeia de caracteres de conexão de MariaDB.

## PARÂMETROS

### -Client
Tipo de cliente Connect

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
região DefaultParameters As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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
Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.

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

### -Name
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer

## SAÍDAS

### System.String

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT <IServer> : Parâmetro Identity
  - `Location <String>`: O local em que o recurso reside.
  - `[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valores-chave.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor. Só pode ser especificado quando o servidor está sendo criado (e é necessário para a criação).
  - `[EarliestRestoreDate <DateTime?>]`: Tempo de criação de ponto de restauração mais antigo (formato ISO8601)
  - `[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.
  - `[IdentityType <IdentityType?>]`: O tipo de identidade. De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.
  - `[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.
  - `[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.
  - `[ReplicationRole <String>]`: A função de replicação do servidor.
  - `[SkuCapacity <Int32?>]`: A capacidade de dimensionar/sair, representando as unidades de computação do servidor.
  - `[SkuFamily <String>]`: A família de hardware.
  - `[SkuName <String>]`: O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: O código de tamanho, a ser interpretado pelo recurso conforme apropriado.
  - `[SkuTier <SkuTier?>]`: A camada da SKU específica, por exemplo, Basic.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não quando se conectar ao servidor.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar geo redundante ou não para backup do servidor.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o Crescimento Automático de Armazenamento.
  - `[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.
  - `[UserVisibleState <ServerState?>]`: Um estado de um servidor que está visível para o usuário.
  - `[Version <ServerVersion?>]`: Versão do servidor.

## LINKS RELACIONADOS

