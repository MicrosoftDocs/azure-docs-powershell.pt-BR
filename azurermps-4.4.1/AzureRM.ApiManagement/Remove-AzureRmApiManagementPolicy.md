---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 5f7fa78cb368afe3e277661122682f43f885f7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427031"
---
# Remove-AzureRmApiManagementPolicy

## Sinopse
Remove a política de gerenciamento de API de um escopo especificado.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Nível do locatário (padrão)
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Nível do produto
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Nível de API
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Nível de operação
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmApiManagementPolicy** remove a política de gerenciamento de API do escopo especificado.

## EXEMPLOS

### Exemplo 1: remover a política de nível de locatário
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext
```

Esse comando Remove a política de nível de locatário do gerenciamento de API.

### Exemplo 2: remover a política de escopo de produto
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

Esse comando Remove a política de escopo de produto do gerenciamento de API.

### Exemplo 3: remover a política de escopo de API
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

Esse comando Remove a política de escopo de API do gerenciamento de API.

### Exemplo 4: remover a política de escopo de operação
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

Esse comando Remove a política de escopo de operação do gerenciamento de API.

## OS

### -ApiId
Especifica o identificador de uma API existente.
Se você especificar esse parâmetro, o cmdlet removerá a política de escopo de API.

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Contexto
Especifica a instância do objeto **PsApiManagementContext** .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationId
Especifica o identificador de uma operação existente.
Se você especificar esse parâmetro com o parâmetro *ApiId* , esse cmdlet removerá a política de escopo de operação.

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Indica que esse cmdlet retorna um valor de $True, se tiver êxito, ou um valor de $False, caso contrário.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductId
Especifica o identificador do produto existente.
Se você especificar esse parâmetro, o cmdlet removerá a política de escopo do produto.

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Booliana

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmApiManagementPolicy](./Get-AzureRmApiManagementPolicy.md)

[Set-AzureRmApiManagementPolicy](./Set-AzureRmApiManagementPolicy.md)


