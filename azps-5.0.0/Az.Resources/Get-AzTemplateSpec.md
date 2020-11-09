---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281906"
---
# <span data-ttu-id="9c9fe-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="9c9fe-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="9c9fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c9fe-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9fe-103">Obtém ou lista as especificações do modelo</span><span class="sxs-lookup"><span data-stu-id="9c9fe-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="9c9fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c9fe-104">SYNTAX</span></span>

### <span data-ttu-id="9c9fe-105">ListTemplateSpecsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c9fe-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c9fe-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c9fe-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c9fe-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c9fe-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c9fe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c9fe-108">DESCRIPTION</span></span>
<span data-ttu-id="9c9fe-109">Esse cmdlet pode ser usado para listar as especificações de modelo em um grupo de assinaturas/recursos ou obter uma especificação de modelo específica por nome ou ID. Ao obter uma especificação de modelo específica por nome/ID, uma versão específica pode ser recuperada opcionalmente especificando um nome de versão por meio do parâmetro **-version** .</span><span class="sxs-lookup"><span data-stu-id="9c9fe-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="9c9fe-110">Quando **-a versão** for usada, somente os detalhes da versão específica serão apresentados dentro \* *. Versões* no objeto de especificação de modelo retornado.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-110">When **-Version** is used, only the specific version details will be present within \* *.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="9c9fe-111">Se nenhuma versão específica for especificada ao recuperar uma especificação de modelo por nome/ID, todas as versões serão apresentadas dentro do \* *. Propriedade Versions* do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \* *.Versions* property of the returned object.</span></span>

<span data-ttu-id="9c9fe-112">**Observação** : ao listar todas as especificações de modelo em uma assinatura ou grupo de recursos, cada uma das especificações de modelo retornadas *". Versions "* será *nulo*.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-112">**Note** : When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="9c9fe-113">As informações de versão são incluídas apenas quando os parâmetros-Name ou-ResourceId são fornecidos (ou seja: você está solicitando uma versão/espec de modelo específica).</span><span class="sxs-lookup"><span data-stu-id="9c9fe-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="9c9fe-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c9fe-114">EXAMPLES</span></span>

### <span data-ttu-id="9c9fe-115">Exemplo 1: listar especificações de modelo na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="9c9fe-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="9c9fe-116">Lista todas as especificações de modelo na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="9c9fe-117">Exemplo 2: especificações do modelo de lista em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9c9fe-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="9c9fe-118">Lista todas as especificações de modelo no grupo de recursos "myRG" da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="9c9fe-119">Exemplo 3: obter especificação de modelo (com todas as versões) por nome</span><span class="sxs-lookup"><span data-stu-id="9c9fe-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="9c9fe-120">Obtém informações sobre a especificação de modelo chamada "MyTemplateSpec" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="9c9fe-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="9c9fe-121">**Observação** : todas as versões da especificação do modelo serão apresentadas dentro do " *. Versions* "do objeto Return.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-121">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="9c9fe-122">Exemplo 4: obter especificação de modelo (versão específica) pelo nome</span><span class="sxs-lookup"><span data-stu-id="9c9fe-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="9c9fe-123">Obtém informações sobre a versão "v 1.0" da especificação do modelo chamada "MyTemplateSpec" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="9c9fe-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="9c9fe-124">**Observação** : o *". Versions "* do objeto retornado conterá apenas a versão específica solicitada.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-124">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="9c9fe-125">Exemplo 5: obter a especificação do modelo (com todas as versões) por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="9c9fe-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="9c9fe-126">Obtém informações sobre a especificação de modelo chamada "MyTemplateSpec" no grupo de recursos "myRG" da \{ subId de assinatura \} .</span><span class="sxs-lookup"><span data-stu-id="9c9fe-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="9c9fe-127">**Observação** : todas as versões da especificação do modelo serão apresentadas dentro do " *. Versions* "do objeto Return.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-127">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="9c9fe-128">Exemplo 6: obter especificação do modelo (versão específica) por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="9c9fe-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="9c9fe-129">Obtém informações sobre a versão "v 1.0" da especificação de modelo chamada "MyTemplateSpec" no grupo de recursos "myRG" da assinatura \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="9c9fe-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="9c9fe-130">**Observação** : o *". Versions "* do objeto retornado conterá apenas a versão específica solicitada.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-130">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="9c9fe-131">OS</span><span class="sxs-lookup"><span data-stu-id="9c9fe-131">PARAMETERS</span></span>

### <span data-ttu-id="9c9fe-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c9fe-132">-DefaultProfile</span></span>
<span data-ttu-id="9c9fe-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c9fe-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c9fe-134">-Name</span></span>
<span data-ttu-id="9c9fe-135">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="9c9fe-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c9fe-136">-ResourceGroupName</span></span>
<span data-ttu-id="9c9fe-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="9c9fe-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c9fe-138">-ResourceId</span></span>
<span data-ttu-id="9c9fe-139">A ID de recurso totalmente qualificado da especificação do modelo. exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="9c9fe-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="9c9fe-140">-Versão</span><span class="sxs-lookup"><span data-stu-id="9c9fe-140">-Version</span></span>
<span data-ttu-id="9c9fe-141">A versão da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="9c9fe-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9fe-142">CommonParameters</span></span>
<span data-ttu-id="9c9fe-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c9fe-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9fe-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c9fe-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9fe-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c9fe-145">INPUTS</span></span>

### <span data-ttu-id="9c9fe-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9c9fe-146">System.String</span></span>

## <span data-ttu-id="9c9fe-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c9fe-147">OUTPUTS</span></span>

### <span data-ttu-id="9c9fe-148">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="9c9fe-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="9c9fe-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c9fe-149">NOTES</span></span>

## <span data-ttu-id="9c9fe-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c9fe-150">RELATED LINKS</span></span>
