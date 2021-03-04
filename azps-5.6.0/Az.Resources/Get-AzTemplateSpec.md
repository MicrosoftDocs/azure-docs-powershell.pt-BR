---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886400"
---
# Get-AzTemplateSpec

## SYNOPSIS
Obtém ou lista Especificações do Modelo

## SINTAXE

### ListTemplateSpecsParameterSet (Padrão)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
Esse cmdlet pode ser usado para listar Especificações de Modelo em um grupo de assinatura/recurso ou obter uma Especificação de Modelo específica por nome ou id. Ao obter uma Especificação de Modelo específica por nome/id, opcionalmente, uma versão específica pode ser recuperada especificando um nome de versão por meio do **parâmetro -Version.** Quando **-Version** for usado, somente os detalhes específicos da versão estarão presentes em **. Versões* no objeto Template Spec retornado. Se nenhuma versão específica for especificada ao recuperar uma Especificação de Modelo pelo nome/id, todas as versões estarão presentes no **. Propriedade Versions* do objeto retornado.

**Observação**: ao listar todas as Especificações de Modelo em uma assinatura ou grupo de recursos, cada Especificação de Modelo *retornada ". A propriedade Versions"* será *nula*. As informações de versão só são incluídas quando os parâmetros -Name ou -ResourceId são fornecidos (por exemplo: você está solicitando uma especificação/versão de modelo específica).

## EXEMPLOS

### Exemplo 1: Especificações do Modelo de Lista na assinatura atual
```powershell
PS C:\> Get-AzTemplateSpec
```

Lista todas as Especificações de Modelo na assinatura atual.

### Exemplo 2: Especificações do Modelo de Lista em um grupo de recursos
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Lista todas as Especificações de Modelo no grupo de recursos "myRG" da assinatura atual.

### Exemplo 3: Obter a Especificação do Modelo (com todas as versões) pelo nome
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Obtém informações sobre a Especificação de Modelo chamada 'MyTemplateSpec' dentro do grupo de recursos 'myRG'.

**Observação**: todas as versões do Template Spec estarão presentes no "*. Propriedade* Versions " do objeto de retorno.

### Exemplo 4: Obter Especificação do Modelo (versão específica) pelo nome
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Obtém informações sobre a versão 'v1.0' da Especificação de Modelo chamada 'MyTemplateSpec' no grupo de recursos 'myRG'.

**Observação**: *". Propriedade Versions"* do objeto retornado conterá apenas a versão específica solicitada.

### Exemplo 5: Obter a Especificação do Modelo (com todas as versões) por id de recurso
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Obtém informações sobre a Especificação de Modelo chamada 'MyTemplateSpec' dentro do grupo de recursos 'myRG' de subId de \{ assinatura \} .

**Observação**: todas as versões do Template Spec estarão presentes no "*. Propriedade* Versions " do objeto de retorno.

### Exemplo 6: Obter Especificação do Modelo (versão específica) por id de recurso
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Obtém informações sobre a versão 'v1.0' da Especificação de Modelo denominada 'MyTemplateSpec' dentro do grupo de recursos 'myRG' de \{ subId de assinatura \} .

**Observação**: *". Propriedade Versions"* do objeto retornado conterá apenas a versão específica solicitada.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
O nome da especificação do modelo.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A ID de recurso totalmente qualificada da especificação do modelo. Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
A versão da especificação do modelo.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec

## NOTES

## LINKS RELACIONADOS
