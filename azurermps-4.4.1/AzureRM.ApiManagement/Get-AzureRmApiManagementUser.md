---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427040"
---
# Get-AzureRmApiManagementUser

## Sinopse
Obtém um ou mais usuários.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Obter todos os usuários (padrão)
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Obter usuário por ID
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Localizar usuários
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApiManagementUser** Obtém um usuário especificado ou todos os usuários, se nenhum usuário for especificado.

## EXEMPLOS

### Exemplo 1: obter todos os usuários
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

Esse comando obtém todos os usuários.

### Exemplo 2: obter um usuário por ID
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

Este comando obtém um usuário por ID.

### Exemplo: obter usuários pelo sobrenome
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

Esse comando obtém os usuários que têm um sobrenome especificado, o mais completo.

### Exemplo 4: obter um usuário por endereço de email
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

Esse comando obtém o usuário que tem o endereço de email especificado.

### Exemplo 5: obter todos os usuários de um grupo
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

Esse comando obtém todos os usuários dentro do grupo especificado.

## OS

### -Contexto
Especifica uma instância de **PsApiManagementContext**.

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

### -Email
Especifica o endereço de email do usuário.
Se esse parâmetro for especificado, esse cmdlet localizará um usuário por email.
Este parâmetro é opcional.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o primeiro nome do usuário.
Se esse parâmetro for especificado, esse cmdlet localizará um usuário por nome.
Este parâmetro é opcional.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GroupId
Especifica o identificador do grupo.
Se especificado, esse cmdlet localiza todos os usuários dentro do grupo especificado.
Este parâmetro é opcional.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LastName
Especifica o último nome de um usuário.
Se especificado, esse cmdlet localiza os usuários por sobrenome.
Este parâmetro é opcional.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Estado
Especifica o estado do usuário.
Se especificado, esse cmdlet localiza os usuários nesse estado.
Este parâmetro é opcional.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserId
Especifica uma ID de usuário.
Se especificado, esse cmdlet localiza o usuário por esse identificador.
Este parâmetro é opcional.

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
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

### IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementUser>

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmApiManagementUser](./New-AzureRmApiManagementUser.md)

[Remove-AzureRmApiManagementUser](./Remove-AzureRmApiManagementUser.md)

[Set-AzureRmApiManagementUser](./Set-AzureRmApiManagementUser.md)


