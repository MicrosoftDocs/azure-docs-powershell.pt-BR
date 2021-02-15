---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114911"
---
# <span data-ttu-id="d101f-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="d101f-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="d101f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d101f-102">SYNOPSIS</span></span>
<span data-ttu-id="d101f-103">Obtém ou lista especificações de modelo</span><span class="sxs-lookup"><span data-stu-id="d101f-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="d101f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d101f-104">SYNTAX</span></span>

### <span data-ttu-id="d101f-105">ListTemplateSpecsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d101f-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d101f-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d101f-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d101f-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d101f-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d101f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d101f-108">DESCRIPTION</span></span>
<span data-ttu-id="d101f-109">Esse cmdlet pode ser usado para listar Especificações de Modelo em um grupo de recursos/assinatura ou obter uma Especificação de Modelo específica por nome ou id. Ao obter uma Especificação de Modelo específica por nome/id, opcionalmente, uma versão específica pode ser recuperada especificando um nome de versão por meio do parâmetro **-Version.**</span><span class="sxs-lookup"><span data-stu-id="d101f-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="d101f-110">Quando **a versão for** usada, somente os detalhes específicos da versão estarão presentes em \**. Versões* no objeto de Especificação de Modelo retornado.</span><span class="sxs-lookup"><span data-stu-id="d101f-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="d101f-111">Se nenhuma versão específica for especificada ao recuperar uma Especificação de Modelo por nome/id, todas as versões estarão presentes no \**. Propriedade* Versões do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="d101f-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="d101f-112">**Observação:** ao listar todas as Especificações de Modelo dentro de uma assinatura ou grupo de recursos, cada Especificação de Modelo retornada *". A propriedade Versões"* será *nula.*</span><span class="sxs-lookup"><span data-stu-id="d101f-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="d101f-113">As informações de versão só são incluídas quando os parâmetros -Name ou -ResourceId são fornecidos (por exemplo: você está solicitando uma especificação/versão de modelo específica).</span><span class="sxs-lookup"><span data-stu-id="d101f-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="d101f-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d101f-114">EXAMPLES</span></span>

### <span data-ttu-id="d101f-115">Exemplo 1: Especificações de Modelo de Lista na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="d101f-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="d101f-116">Lista todas as Especificações de Modelo na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d101f-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="d101f-117">Exemplo 2: Especificações de Modelo de Lista em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d101f-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="d101f-118">Lista todas as Especificações de Modelo no grupo de recursos "myRG" da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d101f-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="d101f-119">Exemplo 3: Obter Especificação de Modelo (com todas as versões) por nome</span><span class="sxs-lookup"><span data-stu-id="d101f-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="d101f-120">Obtém informações sobre a Especificação de Modelo chamada 'MyTemplateSpec' no grupo de recursos "meuRG".</span><span class="sxs-lookup"><span data-stu-id="d101f-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="d101f-121">**Observação:** todas as versões da Especificação de Modelo estarão presentes no "*. Propriedade* Versões " do objeto de devolução.</span><span class="sxs-lookup"><span data-stu-id="d101f-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="d101f-122">Exemplo 4: Obter Especificação de Modelo (versão específica) por nome</span><span class="sxs-lookup"><span data-stu-id="d101f-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="d101f-123">Obtém informações sobre a versão 'v1.0' da Especificação de Modelo chamada 'MyTemplateSpec' no grupo de recursos 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="d101f-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="d101f-124">**Observação:** *". A propriedade* "Versões" do objeto retornado conterá apenas a versão específica solicitada.</span><span class="sxs-lookup"><span data-stu-id="d101f-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="d101f-125">Exemplo 5: Obter Especificação do Modelo (com todas as versões) por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="d101f-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="d101f-126">Obtém informações sobre a Especificação de Modelo chamada 'MyTemplateSpec' no grupo de recursos "myRG" da \{ subId de \} assinatura.</span><span class="sxs-lookup"><span data-stu-id="d101f-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="d101f-127">**Observação:** todas as versões da Especificação de Modelo estarão presentes no "*. Propriedade* Versões " do objeto de devolução.</span><span class="sxs-lookup"><span data-stu-id="d101f-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="d101f-128">Exemplo 6: Obter Especificação do Modelo (versão específica) por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="d101f-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="d101f-129">Obtém informações sobre a versão 'v1.0' da Especificação de Modelo chamada 'MyTemplateSpec' no grupo de recursos "myRG" da subId de \{ \} assinatura.</span><span class="sxs-lookup"><span data-stu-id="d101f-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="d101f-130">**Observação:** *". A propriedade* "Versões" do objeto retornado conterá apenas a versão específica solicitada.</span><span class="sxs-lookup"><span data-stu-id="d101f-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="d101f-131">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d101f-131">PARAMETERS</span></span>

### <span data-ttu-id="d101f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d101f-132">-DefaultProfile</span></span>
<span data-ttu-id="d101f-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d101f-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d101f-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="d101f-134">-Name</span></span>
<span data-ttu-id="d101f-135">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="d101f-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="d101f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d101f-136">-ResourceGroupName</span></span>
<span data-ttu-id="d101f-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d101f-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="d101f-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d101f-138">-ResourceId</span></span>
<span data-ttu-id="d101f-139">A ID de recurso totalmente qualificada da especificação do modelo. Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="d101f-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="d101f-140">-Versão</span><span class="sxs-lookup"><span data-stu-id="d101f-140">-Version</span></span>
<span data-ttu-id="d101f-141">A versão da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="d101f-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="d101f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d101f-142">CommonParameters</span></span>
<span data-ttu-id="d101f-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d101f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d101f-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d101f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d101f-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="d101f-145">INPUTS</span></span>

### <span data-ttu-id="d101f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d101f-146">System.String</span></span>

## <span data-ttu-id="d101f-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="d101f-147">OUTPUTS</span></span>

### <span data-ttu-id="d101f-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="d101f-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="d101f-149">Notas</span><span class="sxs-lookup"><span data-stu-id="d101f-149">NOTES</span></span>

## <span data-ttu-id="d101f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d101f-150">RELATED LINKS</span></span>
