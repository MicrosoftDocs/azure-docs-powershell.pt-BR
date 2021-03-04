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
# <span data-ttu-id="78a1e-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="78a1e-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="78a1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="78a1e-103">Obtém ou lista Especificações do Modelo</span><span class="sxs-lookup"><span data-stu-id="78a1e-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="78a1e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="78a1e-104">SYNTAX</span></span>

### <span data-ttu-id="78a1e-105">ListTemplateSpecsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="78a1e-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78a1e-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a1e-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a1e-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a1e-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78a1e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="78a1e-108">DESCRIPTION</span></span>
<span data-ttu-id="78a1e-109">Esse cmdlet pode ser usado para listar Especificações de Modelo em um grupo de assinatura/recurso ou obter uma Especificação de Modelo específica por nome ou id. Ao obter uma Especificação de Modelo específica por nome/id, opcionalmente, uma versão específica pode ser recuperada especificando um nome de versão por meio do **parâmetro -Version.**</span><span class="sxs-lookup"><span data-stu-id="78a1e-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="78a1e-110">Quando **-Version** for usado, somente os detalhes específicos da versão estarão presentes em \**. Versões* no objeto Template Spec retornado.</span><span class="sxs-lookup"><span data-stu-id="78a1e-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="78a1e-111">Se nenhuma versão específica for especificada ao recuperar uma Especificação de Modelo pelo nome/id, todas as versões estarão presentes no \**. Propriedade Versions* do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="78a1e-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="78a1e-112">**Observação**: ao listar todas as Especificações de Modelo em uma assinatura ou grupo de recursos, cada Especificação de Modelo *retornada ". A propriedade Versions"* será *nula*.</span><span class="sxs-lookup"><span data-stu-id="78a1e-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="78a1e-113">As informações de versão só são incluídas quando os parâmetros -Name ou -ResourceId são fornecidos (por exemplo: você está solicitando uma especificação/versão de modelo específica).</span><span class="sxs-lookup"><span data-stu-id="78a1e-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="78a1e-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78a1e-114">EXAMPLES</span></span>

### <span data-ttu-id="78a1e-115">Exemplo 1: Especificações do Modelo de Lista na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="78a1e-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="78a1e-116">Lista todas as Especificações de Modelo na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="78a1e-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="78a1e-117">Exemplo 2: Especificações do Modelo de Lista em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="78a1e-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="78a1e-118">Lista todas as Especificações de Modelo no grupo de recursos "myRG" da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="78a1e-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="78a1e-119">Exemplo 3: Obter a Especificação do Modelo (com todas as versões) pelo nome</span><span class="sxs-lookup"><span data-stu-id="78a1e-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="78a1e-120">Obtém informações sobre a Especificação de Modelo chamada 'MyTemplateSpec' dentro do grupo de recursos 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="78a1e-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="78a1e-121">**Observação**: todas as versões do Template Spec estarão presentes no "*. Propriedade* Versions " do objeto de retorno.</span><span class="sxs-lookup"><span data-stu-id="78a1e-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="78a1e-122">Exemplo 4: Obter Especificação do Modelo (versão específica) pelo nome</span><span class="sxs-lookup"><span data-stu-id="78a1e-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="78a1e-123">Obtém informações sobre a versão 'v1.0' da Especificação de Modelo chamada 'MyTemplateSpec' no grupo de recursos 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="78a1e-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="78a1e-124">**Observação**: *". Propriedade Versions"* do objeto retornado conterá apenas a versão específica solicitada.</span><span class="sxs-lookup"><span data-stu-id="78a1e-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="78a1e-125">Exemplo 5: Obter a Especificação do Modelo (com todas as versões) por id de recurso</span><span class="sxs-lookup"><span data-stu-id="78a1e-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="78a1e-126">Obtém informações sobre a Especificação de Modelo chamada 'MyTemplateSpec' dentro do grupo de recursos 'myRG' de subId de \{ assinatura \} .</span><span class="sxs-lookup"><span data-stu-id="78a1e-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="78a1e-127">**Observação**: todas as versões do Template Spec estarão presentes no "*. Propriedade* Versions " do objeto de retorno.</span><span class="sxs-lookup"><span data-stu-id="78a1e-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="78a1e-128">Exemplo 6: Obter Especificação do Modelo (versão específica) por id de recurso</span><span class="sxs-lookup"><span data-stu-id="78a1e-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="78a1e-129">Obtém informações sobre a versão 'v1.0' da Especificação de Modelo denominada 'MyTemplateSpec' dentro do grupo de recursos 'myRG' de \{ subId de assinatura \} .</span><span class="sxs-lookup"><span data-stu-id="78a1e-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="78a1e-130">**Observação**: *". Propriedade Versions"* do objeto retornado conterá apenas a versão específica solicitada.</span><span class="sxs-lookup"><span data-stu-id="78a1e-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="78a1e-131">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="78a1e-131">PARAMETERS</span></span>

### <span data-ttu-id="78a1e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a1e-132">-DefaultProfile</span></span>
<span data-ttu-id="78a1e-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78a1e-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78a1e-134">-Name</span><span class="sxs-lookup"><span data-stu-id="78a1e-134">-Name</span></span>
<span data-ttu-id="78a1e-135">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="78a1e-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="78a1e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a1e-136">-ResourceGroupName</span></span>
<span data-ttu-id="78a1e-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78a1e-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="78a1e-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78a1e-138">-ResourceId</span></span>
<span data-ttu-id="78a1e-139">A ID de recurso totalmente qualificada da especificação do modelo. Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="78a1e-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="78a1e-140">-Version</span><span class="sxs-lookup"><span data-stu-id="78a1e-140">-Version</span></span>
<span data-ttu-id="78a1e-141">A versão da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="78a1e-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="78a1e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a1e-142">CommonParameters</span></span>
<span data-ttu-id="78a1e-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a1e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a1e-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78a1e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a1e-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78a1e-145">INPUTS</span></span>

### <span data-ttu-id="78a1e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="78a1e-146">System.String</span></span>

## <span data-ttu-id="78a1e-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="78a1e-147">OUTPUTS</span></span>

### <span data-ttu-id="78a1e-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="78a1e-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="78a1e-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="78a1e-149">NOTES</span></span>

## <span data-ttu-id="78a1e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78a1e-150">RELATED LINKS</span></span>
