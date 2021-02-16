---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113394"
---
# <span data-ttu-id="1312b-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="1312b-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="1312b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1312b-102">SYNOPSIS</span></span>
<span data-ttu-id="1312b-103">serviço de vinculação para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="1312b-103">link service for workspace</span></span>

## <span data-ttu-id="1312b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1312b-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1312b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1312b-105">DESCRIPTION</span></span>
<span data-ttu-id="1312b-106">serviço de vinculação para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="1312b-106">link service for workspace</span></span>

## <span data-ttu-id="1312b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1312b-107">EXAMPLES</span></span>

### <span data-ttu-id="1312b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1312b-108">Example 1</span></span>
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

<span data-ttu-id="1312b-109">cluster de vínculo para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="1312b-109">link cluster for workspace</span></span>

## <span data-ttu-id="1312b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1312b-110">PARAMETERS</span></span>

### <span data-ttu-id="1312b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1312b-111">-AsJob</span></span>
<span data-ttu-id="1312b-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1312b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1312b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1312b-113">-DefaultProfile</span></span>
<span data-ttu-id="1312b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1312b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1312b-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="1312b-115">-LinkedServiceName</span></span>
<span data-ttu-id="1312b-116">O nome do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="1312b-116">The Workspace name.</span></span>

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

### <span data-ttu-id="1312b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1312b-117">-ResourceGroupName</span></span>
<span data-ttu-id="1312b-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1312b-118">The resource group name.</span></span>

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

### <span data-ttu-id="1312b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1312b-119">-ResourceId</span></span>
<span data-ttu-id="1312b-120">A ID do recurso que será vinculada ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1312b-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="1312b-121">Isso deve ser usado para vincular recursos que exigem acesso de leitura</span><span class="sxs-lookup"><span data-stu-id="1312b-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="1312b-122">-Marcas</span><span class="sxs-lookup"><span data-stu-id="1312b-122">-Tags</span></span>
<span data-ttu-id="1312b-123">Tags.</span><span class="sxs-lookup"><span data-stu-id="1312b-123">Tags.</span></span>

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

### <span data-ttu-id="1312b-124">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="1312b-124">-WorkspaceName</span></span>
<span data-ttu-id="1312b-125">O nome do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="1312b-125">The Workspace name.</span></span>

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

### <span data-ttu-id="1312b-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="1312b-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="1312b-127">A ID do recurso que será vinculada ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1312b-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="1312b-128">Isso deve ser usado para vincular recursos que exigem acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="1312b-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="1312b-129">O cluster deve ter o estado de provisionamento "Bem-sucedido" e as propriedades de keyvault válidas.</span><span class="sxs-lookup"><span data-stu-id="1312b-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="1312b-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1312b-130">-Confirm</span></span>
<span data-ttu-id="1312b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1312b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1312b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1312b-132">-WhatIf</span></span>
<span data-ttu-id="1312b-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1312b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1312b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1312b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1312b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1312b-135">CommonParameters</span></span>
<span data-ttu-id="1312b-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1312b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1312b-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1312b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1312b-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="1312b-138">INPUTS</span></span>

### <span data-ttu-id="1312b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1312b-139">System.String</span></span>

## <span data-ttu-id="1312b-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="1312b-140">OUTPUTS</span></span>

### <span data-ttu-id="1312b-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="1312b-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="1312b-142">Notas</span><span class="sxs-lookup"><span data-stu-id="1312b-142">NOTES</span></span>

## <span data-ttu-id="1312b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1312b-143">RELATED LINKS</span></span>
