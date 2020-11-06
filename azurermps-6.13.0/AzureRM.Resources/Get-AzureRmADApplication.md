---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: d36bca60f722498beaa831c2a630b23d8a709019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430062"
---
# Get-AzureRmADApplication

## Sinopse
Lista os aplicativos existentes do Azure Active Directory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### EmptyParameterSet (padrão)
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### ApplicationObjectIdParameterSet
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdentifierUriParameterSet
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## DESCRITIVO
Lista os aplicativos existentes do Azure Active Directory.
A pesquisa do aplicativo pode ser feita por ObjectId, ApplicationId, IdentifierUri ou DisplayName.
Se nenhum parâmetro for fornecido, ele buscará todos os aplicativos sob o locatário.

## EXEMPLOS

### Exemplo 1-listar todos os aplicativos

```
PS C:\> Get-AzureRmADApplication
```

Lista todos os aplicativos em um locatário.

### Exemplo 2 aplicativos de lista usando paginação

```
PS C:\> Get-AzureRmADApplication -First 100
```

Lista os primeiros aplicativos do 100 em um locatário.

### Exemplo 3-obter aplicativo por URI identificador

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

Obtém o aplicativo com URI de identificador como " http://mySecretApp1 ".

### Exemplo 4-obter aplicativo por ID do objeto

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

Obtém o aplicativo com a ID de objeto ' 39e64ec6-569B-4030-8e1c-c3c519a05d69 '.

## OS

### -ApplicationId
A ID do aplicativo do aplicativo a ser buscado.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DisplayName
O nome de exibição do aplicativo.

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayNameStartWith
Busque todos os aplicativos que começam com o nome para exibição.

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Primeiro
O número máximo de objetos a serem retornados.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentifierUri
URI do identificador exclusivo do aplicativo a ser buscado.

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeTotalCount
Informa o número de objetos no conjunto de dados. Atualmente, esse parâmetro não faz nada.

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

### -ObjectId
A ID do objeto do aplicativo a ser buscado.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. GUID

### System. String

## EXIBE

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)

[New-AzureRmADAppCredential](./New-AzureRmADAppCredential.md)

[Get-AzureRmADAppCredential](./Get-AzureRmADAppCredential.md)

[Remove-AzureRmADApplication](./Remove-AzureRmADApplication.md)

[Set-AzureRmADApplication](./Set-AzureRmADApplication.md)

[New-AzureRmADApplication](./New-AzureRmADApplication.md)

