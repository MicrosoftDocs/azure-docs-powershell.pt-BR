---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: 56410e48bedbe7af616ffd1dcada4e99f1668cdc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598648"
---
# Get-AzStorageShare

## Sinopse
Obtém uma lista de compartilhamentos de arquivos.

## SYNTAX

### MatchingPrefix (padrão)
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Especifica
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzStorageShare** Obtém uma lista de compartilhamentos de arquivos para uma conta de armazenamento.

## EXEMPLOS

### Exemplo 1: obter um compartilhamento de arquivos
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

Esse comando obtém o compartilhamento de arquivos chamado ContosoShare06.

### Exemplo 2: obter todos os compartilhamentos de arquivos que começam com uma cadeia de caracteres
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

Esse comando obtém todos os compartilhamentos de arquivos que têm nomes que começam com contoso.

### Exemplo 3: obter todos os compartilhamentos de arquivos em um contexto especificado
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

O primeiro comando usa o cmdlet **New-AzStorageContext** para criar um contexto usando o parâmetro *local* e, em seguida, armazena esse objeto Context na variável $Context.
O segundo comando obtém os compartilhamentos de arquivos para o objeto de contexto armazenado em $Context.

### Exemplo 4: obter um instantâneo de compartilhamento de arquivos com um nome de compartilhamento específico e Instantâneotime
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

Esse comando obtém um instantâneo do compartilhamento de arquivos com um nome de compartilhamento específico e Instantâneotime.

## OS

### -ClientTimeoutPerRequest
Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.
Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.
Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Especifica o número máximo de chamadas de rede simultâneas.
Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.
O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.
Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.
O valor padrão é 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contexto
Especifica um contexto de armazenamento do Azure.
Para obter um contexto, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do compartilhamento de arquivos.
Esse cmdlet obtém o compartilhamento de arquivo que esse parâmetro especifica ou nada se você especificar o nome de um compartilhamento de arquivos que não existe.

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prefix
Especifica o prefixo dos compartilhamentos de arquivos.
Esse cmdlet obtém os compartilhamentos de arquivos que correspondem ao prefixo que esse parâmetro especifica, ou nenhum compartilhamento de arquivos se nenhum compartilhamento de arquivos corresponder ao prefixo especificado.

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Instantâneotime
Instantâneotime do instantâneo de compartilhamento de arquivos a ser recebido.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext

## EXIBE

### Microsoft. WindowsAzure. Storage. File. CloudFileShare

## INFORMA

## LINKS RELACIONADOS

[New-AzStorageShare](./New-AzStorageShare.md)

[Remove-AzStorageShare](./Remove-AzStorageShare.md)
