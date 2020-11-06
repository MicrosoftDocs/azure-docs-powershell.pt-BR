---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432689"
---
# Get-AzureRmApiManagementLogger

## Sinopse
Obtém objetos de agente de gerenciamento de API.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Obter todos os registradores (padrão)
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Obter por ID do logger
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApiManagementLogger** Obtém um **agente** de gerenciamento de API do Azure ou todos os registradores.

## EXEMPLOS

### Exemplo 1: obter todos os registradores
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

Esse comando obtém todos os loggers do contexto especificado.

### Exemplo 2: obter um agente de log específico
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

Esse comando Remove um logger que tem a ID Logger123.

## OS

### -Contexto
Especifica um objeto **PsApiManagementContext** .

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

### -Loggerid
Especifica a ID do agente de log específico a obter.

```yaml
Type: System.String
Parameter Sets: Get by logger ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementLogger>

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmApiManagementLogger](./New-AzureRmApiManagementLogger.md)

[Remove-AzureRmApiManagementLogger](./Remove-AzureRmApiManagementLogger.md)

[Set-AzureRmApiManagementLogger](./Set-AzureRmApiManagementLogger.md)


