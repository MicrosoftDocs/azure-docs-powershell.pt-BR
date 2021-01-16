---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271666"
---
# <span data-ttu-id="5fae7-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="5fae7-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="5fae7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fae7-102">SYNOPSIS</span></span>
<span data-ttu-id="5fae7-103">serviço de link para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5fae7-103">link service for workspace</span></span>

## <span data-ttu-id="5fae7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fae7-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fae7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fae7-105">DESCRIPTION</span></span>
<span data-ttu-id="5fae7-106">serviço de link para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5fae7-106">link service for workspace</span></span>

## <span data-ttu-id="5fae7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fae7-107">EXAMPLES</span></span>

### <span data-ttu-id="5fae7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5fae7-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="5fae7-109">cluster de links para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5fae7-109">link cluster for workspace</span></span>

## <span data-ttu-id="5fae7-110">OS</span><span class="sxs-lookup"><span data-stu-id="5fae7-110">PARAMETERS</span></span>

### <span data-ttu-id="5fae7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fae7-111">-AsJob</span></span>
<span data-ttu-id="5fae7-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5fae7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fae7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fae7-113">-DefaultProfile</span></span>
<span data-ttu-id="5fae7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fae7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fae7-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="5fae7-115">-LinkedServiceName</span></span>
<span data-ttu-id="5fae7-116">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5fae7-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fae7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fae7-117">-ResourceGroupName</span></span>
<span data-ttu-id="5fae7-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5fae7-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fae7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fae7-119">-ResourceId</span></span>
<span data-ttu-id="5fae7-120">A ID do recurso que será vinculado ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5fae7-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="5fae7-121">Isso deve ser usado para vincular recursos que exigem acesso de leitura</span><span class="sxs-lookup"><span data-stu-id="5fae7-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="5fae7-122">-Marcas</span><span class="sxs-lookup"><span data-stu-id="5fae7-122">-Tags</span></span>
<span data-ttu-id="5fae7-123">Marcas.</span><span class="sxs-lookup"><span data-stu-id="5fae7-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fae7-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5fae7-124">-WorkspaceName</span></span>
<span data-ttu-id="5fae7-125">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5fae7-125">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fae7-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="5fae7-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="5fae7-127">A ID do recurso que será vinculado ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5fae7-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="5fae7-128">Isso deve ser usado para vincular recursos que exigem acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="5fae7-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="5fae7-129">O cluster deve ter o estado de provisionamento "bem-sucedido" e as propriedades válidas do keyvault.</span><span class="sxs-lookup"><span data-stu-id="5fae7-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="5fae7-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5fae7-130">-Confirm</span></span>
<span data-ttu-id="5fae7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fae7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fae7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fae7-132">-WhatIf</span></span>
<span data-ttu-id="5fae7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5fae7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fae7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fae7-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fae7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fae7-135">CommonParameters</span></span>
<span data-ttu-id="5fae7-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fae7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fae7-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fae7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fae7-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fae7-138">INPUTS</span></span>

### <span data-ttu-id="5fae7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5fae7-139">System.String</span></span>

## <span data-ttu-id="5fae7-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fae7-140">OUTPUTS</span></span>

### <span data-ttu-id="5fae7-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="5fae7-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="5fae7-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fae7-142">NOTES</span></span>

## <span data-ttu-id="5fae7-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fae7-143">RELATED LINKS</span></span>
