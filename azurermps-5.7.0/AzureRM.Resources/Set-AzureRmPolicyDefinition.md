---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: d7e01294836145b09844fa3bca49421df20f67d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432902"
---
# Set-AzureRmPolicyDefinition

## Sinopse
Modifica uma definição de política.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SetByPolicyDefinitionName (padrão)
```
Set-AzureRmPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GetByPolicyDefintionName
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GetByPolicyDefinitionId
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmPolicyDefinition** modifica uma definição de política.

## EXEMPLOS

### Exemplo 1: atualizar a descrição de uma definição de política
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzureRmPolicyDefinition.
O comando armazena esse objeto na variável $PolicyDefinition.

O segundo comando atualiza a descrição da definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.

## OS

### -ApiVersion
Especifica a versão da API do provedor de recursos a ser usada.
Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Descrição
Especifica uma nova descrição para a definição de política.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayName
Especifica um novo nome de exibição para a definição de política.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Especifica a ID de recurso totalmente qualificado para a definição de política que esse cmdlet modifica.

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadados
Os metadados da definição da política. Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da definição de política que este cmdlet modifica.

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parâmetro
A declaração Parameters para a definição da política. Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como cadeia de caracteres.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Política
Especifica a nova regra de política para a definição de política.
Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política no formato JSON (JavaScript Object Notation).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.

```yaml
Type: SwitchParameter
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

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### System. Management. Automation. PSObject

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmPolicyDefinition](./Get-AzureRmPolicyDefinition.md)

[New-AzureRmPolicyDefinition](./New-AzureRmPolicyDefinition.md)

[Remove-AzureRmPolicyDefinition](./Remove-AzureRmPolicyDefinition.md)


