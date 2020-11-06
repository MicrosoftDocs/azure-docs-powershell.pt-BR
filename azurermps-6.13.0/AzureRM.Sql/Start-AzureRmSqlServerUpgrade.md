---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429289"
---
# Start-AzureRmSqlServerUpgrade

## Sinopse
Inicia a atualização de um servidor de banco de dados SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Start-AzureRmSqlServerUpgrade** inicia a atualização de um servidor de banco de dados SQL do Azure versão 11 para a versão 12.
Você pode monitorar o andamento de uma atualização usando o cmdlet Get-AzureRmSqlServerUpgrade.

## EXEMPLOS

### Exemplo 1: atualizar um servidor
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

Esse comando atualiza o servidor chamado Server01 atribuído à TesourceGroup01 do grupo de recursos.

### Exemplo 2: atualizar um servidor usando o tempo de agendamento e a recomendação de banco de dados
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

O primeiro comando cria um tempo cinco minutos no futuro usando o cmdlet Get-Date.
O comando armazena a data na variável $ScheduleTime.
Para obter mais informações, digite `Get-Help Get-Date` .
O segundo comando cria um objeto **RecommendedDatabaseProperties** e armazena esse objeto na variável $DatabaseMap.
Os próximos três comandos atribuem valores às propriedades do objeto armazenadas em $DatabaseMap.
O comando final atualiza o servidor existente chamado Server01 para a versão 12,0.
O mais cedo para atualizar é cinco minutos após você executar o comando, conforme especificado pela variável $ScheduleTime.
Após a atualização, o banco de dados ContosoDB será executando a edição padrão e terá o objetivo de nível de serviço S0.

## OS

### -DatabaseCollection
Especifica uma matriz de objetos **RecommendedDatabaseProperties** que este cmdlet usa para a atualização do servidor.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolCollection
Especifica uma matriz de objetos **UpgradeRecommendedElasticPoolProperties** a serem usados para a atualização do servidor.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o servidor está atribuído.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleUpgradeAfterUtcDateTime
Especifica a primeira vez, como um objeto **DateTime** , para atualizar o servidor.
Especifique um valor no formato ISO8601, no tempo universal coordenado (UTC).
Para obter mais informações, digite `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomedoservidor
Especifica o nome do servidor que este cmdlet atualiza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerVersion
Especifica a versão para a qual esse cmdlet atualiza o servidor.
O único valor válido é 12,0.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Sql. ServerUpgrade. Model. AzureSqlServerUpgradeStartModel

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[Parar-AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)


