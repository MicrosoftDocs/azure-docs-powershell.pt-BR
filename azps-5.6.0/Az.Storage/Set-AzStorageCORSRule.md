---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: 6a04b038a452d979394ab57d8f3d905a57428051
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888404"
---
# Set-AzStorageCORSRule

## SYNOPSIS
Define as regras do CORS para um tipo de serviço de Armazenamento.

## SINTAXE

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Set-AzStorageCORSRule** define as regras de Compartilhamento de Recursos entre Origens (CORS) para um tipo de serviço de Armazenamento do Azure.
Os tipos de serviços de armazenamento para este cmdlet são Blob, Table, Queue e File.
Esse cmdlet substitui as regras existentes.
Para ver as regras atuais, use Get-AzStorageCORSRule cmdlet.

## EXEMPLOS

### Exemplo 1: Atribuir regras CORS ao serviço blob
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

O primeiro comando atribui uma matriz de regras à variável $CorsRules.
Este comando usa o padrão se estende por várias linhas neste bloco de código.
O segundo comando atribui as regras em $CorsRules ao tipo de serviço Blob.

### Exemplo 2: Alterar propriedades de uma regra CORS para o serviço blob
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

O primeiro comando obtém as regras cors atuais do tipo Blob usando o cmdlet **Get-AzStorageCORSRule.**
O comando armazena as regras na variável $CorsRules matriz.
O segundo e o terceiro comandos modificam a primeira regra no $CorsRules.
O comando final atribui as regras em $CorsRules ao tipo de serviço Blob.
As regras revisadas sobrescrevem as regras atuais do CORS.

## PARÂMETROS

### -ClientTimeoutPerRequest
Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.
Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.
Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Especifica o máximo de chamadas de rede simultâneas.
Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.
O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.
Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.
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

### -Context
Especifica um contexto de Armazenamento do Azure.
Para obter um contexto, use o New-AzStorageContext cmdlet.

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

### -CorsRules
Especifica uma matriz de regras CORS.
Você pode recuperar as regras existentes usando o Get-AzStorageCORSRule cmdlet.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -PassThru
Indica que esse cmdlet retorna um Boolean que reflete o sucesso da operação.
Por padrão, esse cmdlet não retorna um valor.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Especifica o tipo de serviço de Armazenamento do Azure para o qual este cmdlet atribui regras.
Os valores aceitáveis para este parâmetro são:
- Blob 
- Tabela 
- Fila 
- Arquivo

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## SAÍDAS

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule

## NOTES

## LINKS RELACIONADOS

[Get-AzStorageCORSRule](./Get-AzStorageCORSRule.md)

[New-AzStorageContext](./New-AzStorageContext.md)

[Remove-AzStorageCORSRule](./Remove-AzStorageCORSRule.md)


