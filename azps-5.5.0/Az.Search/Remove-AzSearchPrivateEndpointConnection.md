---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 341edce877666d56a78064f1e13dc7b7af9b26a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118120"
---
# <span data-ttu-id="d56e9-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d56e9-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="d56e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d56e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d56e9-103">Remova a conexão de ponto de extremidade particular do serviço pesquisa cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d56e9-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d56e9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d56e9-104">SYNTAX</span></span>

### <span data-ttu-id="d56e9-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d56e9-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d56e9-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d56e9-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d56e9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d56e9-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d56e9-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d56e9-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d56e9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d56e9-109">DESCRIPTION</span></span>
<span data-ttu-id="d56e9-110">A **Remove-AzSearchPrivateEndpointConnection** remove a conexão de ponto de extremidade particular do serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d56e9-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d56e9-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d56e9-111">EXAMPLES</span></span>

### <span data-ttu-id="d56e9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d56e9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="d56e9-113">Este exemplo remove uma conexão de ponto de extremidade particular do serviço de pesquisa por nome.</span><span class="sxs-lookup"><span data-stu-id="d56e9-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="d56e9-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d56e9-114">PARAMETERS</span></span>

### <span data-ttu-id="d56e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56e9-115">-DefaultProfile</span></span>
<span data-ttu-id="d56e9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d56e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d56e9-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="d56e9-117">-Force</span></span>
<span data-ttu-id="d56e9-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="d56e9-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d56e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d56e9-119">-InputObject</span></span>
<span data-ttu-id="d56e9-120">Objeto de entrada de conexão de ponto de extremidade particular</span><span class="sxs-lookup"><span data-stu-id="d56e9-120">Private endpoint connection input object</span></span>

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

### <span data-ttu-id="d56e9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d56e9-121">-Name</span></span>
<span data-ttu-id="d56e9-122">Nome de conexão privada do Serviço de Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="d56e9-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="d56e9-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d56e9-123">-ParentObject</span></span>
<span data-ttu-id="d56e9-124">Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d56e9-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="d56e9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d56e9-125">-PassThru</span></span>
<span data-ttu-id="d56e9-126">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="d56e9-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d56e9-127">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d56e9-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d56e9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56e9-128">-ResourceGroupName</span></span>
<span data-ttu-id="d56e9-129">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="d56e9-129">Resource Group name.</span></span>

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

### <span data-ttu-id="d56e9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d56e9-130">-ResourceId</span></span>
<span data-ttu-id="d56e9-131">ID do recurso de serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="d56e9-131">Private link service resource id</span></span>

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

### <span data-ttu-id="d56e9-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d56e9-132">-ServiceName</span></span>
<span data-ttu-id="d56e9-133">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="d56e9-133">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="d56e9-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d56e9-134">-Confirm</span></span>
<span data-ttu-id="d56e9-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d56e9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d56e9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d56e9-136">-WhatIf</span></span>
<span data-ttu-id="d56e9-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d56e9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d56e9-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d56e9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d56e9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56e9-139">CommonParameters</span></span>
<span data-ttu-id="d56e9-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d56e9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56e9-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d56e9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56e9-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="d56e9-142">INPUTS</span></span>

### <span data-ttu-id="d56e9-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d56e9-143">None</span></span>

## <span data-ttu-id="d56e9-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="d56e9-144">OUTPUTS</span></span>

### <span data-ttu-id="d56e9-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d56e9-145">System.Boolean</span></span>

## <span data-ttu-id="d56e9-146">Notas</span><span class="sxs-lookup"><span data-stu-id="d56e9-146">NOTES</span></span>

## <span data-ttu-id="d56e9-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d56e9-147">RELATED LINKS</span></span>

[<span data-ttu-id="d56e9-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="d56e9-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="d56e9-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="d56e9-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)