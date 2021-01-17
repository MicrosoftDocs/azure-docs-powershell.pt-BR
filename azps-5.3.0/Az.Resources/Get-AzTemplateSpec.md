---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427294"
---
# Get-AzTemplateSpec

## Sinopse
Obtém ou lista as especificações do modelo

## SYNTAX

### ListTemplateSpecsParameterSet (padrão)
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

## DESCRITIVO
Esse cmdlet pode ser usado para listar as especificações de modelo em um grupo de assinaturas/recursos ou obter uma especificação de modelo específica por nome ou ID. Ao obter uma especificação de modelo específica por nome/ID, uma versão específica pode ser recuperada opcionalmente especificando um nome de versão por meio do parâmetro **-version** . Quando **-a versão** for usada, somente os detalhes da versão específica serão apresentados dentro **. Versões* no objeto de especificação de modelo retornado. Se nenhuma versão específica for especificada ao recuperar uma especificação de modelo por nome/ID, todas as versões serão apresentadas dentro do **. Propriedade Versions* do objeto retornado.

**Observação**: ao listar todas as especificações de modelo em uma assinatura ou grupo de recursos, cada uma das especificações de modelo retornadas *". Versions "* será *nulo*. As informações de versão são incluídas apenas quando os parâmetros-Name ou-ResourceId são fornecidos (ou seja: você está solicitando uma versão/espec de modelo específica).

## EXEMPLOS

### Exemplo 1: listar especificações de modelo na assinatura atual
```powershell
PS C:\> Get-AzTemplateSpec
```

Lista todas as especificações de modelo na assinatura atual.

### Exemplo 2: especificações do modelo de lista em um grupo de recursos
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Lista todas as especificações de modelo no grupo de recursos "myRG" da assinatura atual.

### Exemplo 3: obter especificação de modelo (com todas as versões) por nome
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Obtém informações sobre a especificação de modelo chamada "MyTemplateSpec" no grupo de recursos "myRG".

**Observação**: todas as versões da especificação do modelo serão apresentadas dentro do "*. Versions*"do objeto Return.

### Exemplo 4: obter especificação de modelo (versão específica) pelo nome
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Obtém informações sobre a versão "v 1.0" da especificação do modelo chamada "MyTemplateSpec" no grupo de recursos "myRG".

**Observação**: o *". Versions "* do objeto retornado conterá apenas a versão específica solicitada.

### Exemplo 5: obter a especificação do modelo (com todas as versões) por ID do recurso
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Obtém informações sobre a especificação de modelo chamada "MyTemplateSpec" no grupo de recursos "myRG" da \{ subId de assinatura \} .

**Observação**: todas as versões da especificação do modelo serão apresentadas dentro do "*. Versions*"do objeto Return.

### Exemplo 6: obter especificação do modelo (versão específica) por ID do recurso
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Obtém informações sobre a versão "v 1.0" da especificação de modelo chamada "MyTemplateSpec" no grupo de recursos "myRG" da assinatura \{ subId \} .

**Observação**: o *". Versions "* do objeto retornado conterá apenas a versão específica solicitada.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Nome
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
A ID de recurso totalmente qualificado da especificação do modelo. exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

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

### -Versão
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSTemplateSpec

## INFORMA

## LINKS RELACIONADOS
