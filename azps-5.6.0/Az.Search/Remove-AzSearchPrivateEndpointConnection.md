---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 98b5f30bfe3a829d276c435c9beef71cf8a2f7de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889755"
---
# <span data-ttu-id="37963-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37963-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="37963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37963-102">SYNOPSIS</span></span>
<span data-ttu-id="37963-103">Remova a conexão de ponto de extremidade privada do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="37963-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="37963-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37963-104">SYNTAX</span></span>

### <span data-ttu-id="37963-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="37963-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37963-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37963-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37963-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37963-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37963-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37963-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37963-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37963-109">DESCRIPTION</span></span>
<span data-ttu-id="37963-110">O **Remove-AzSearchPrivateEndpointConnection** remove a conexão de ponto de extremidade privada do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="37963-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="37963-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37963-111">EXAMPLES</span></span>

### <span data-ttu-id="37963-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37963-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="37963-113">Este exemplo remove uma conexão de ponto de extremidade privada do serviço de pesquisa pelo nome.</span><span class="sxs-lookup"><span data-stu-id="37963-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="37963-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37963-114">PARAMETERS</span></span>

### <span data-ttu-id="37963-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37963-115">-DefaultProfile</span></span>
<span data-ttu-id="37963-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37963-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37963-117">-Force</span><span class="sxs-lookup"><span data-stu-id="37963-117">-Force</span></span>
<span data-ttu-id="37963-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="37963-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="37963-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37963-119">-InputObject</span></span>
<span data-ttu-id="37963-120">Objeto de entrada de conexão de ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="37963-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37963-121">-Name</span><span class="sxs-lookup"><span data-stu-id="37963-121">-Name</span></span>
<span data-ttu-id="37963-122">Nome da conexão de ponto de extremidade privada do Serviço de Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="37963-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37963-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="37963-123">-ParentObject</span></span>
<span data-ttu-id="37963-124">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="37963-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37963-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37963-125">-PassThru</span></span>
<span data-ttu-id="37963-126">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="37963-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="37963-127">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="37963-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="37963-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37963-128">-ResourceGroupName</span></span>
<span data-ttu-id="37963-129">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="37963-129">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37963-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37963-130">-ResourceId</span></span>
<span data-ttu-id="37963-131">ID do recurso de serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="37963-131">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37963-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="37963-132">-ServiceName</span></span>
<span data-ttu-id="37963-133">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="37963-133">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37963-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37963-134">-Confirm</span></span>
<span data-ttu-id="37963-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37963-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37963-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37963-136">-WhatIf</span></span>
<span data-ttu-id="37963-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37963-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37963-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37963-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37963-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37963-139">CommonParameters</span></span>
<span data-ttu-id="37963-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37963-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37963-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37963-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37963-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37963-142">INPUTS</span></span>

### <span data-ttu-id="37963-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="37963-143">None</span></span>

## <span data-ttu-id="37963-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37963-144">OUTPUTS</span></span>

### <span data-ttu-id="37963-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37963-145">System.Boolean</span></span>

## <span data-ttu-id="37963-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="37963-146">NOTES</span></span>

## <span data-ttu-id="37963-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37963-147">RELATED LINKS</span></span>

[<span data-ttu-id="37963-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="37963-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="37963-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="37963-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)