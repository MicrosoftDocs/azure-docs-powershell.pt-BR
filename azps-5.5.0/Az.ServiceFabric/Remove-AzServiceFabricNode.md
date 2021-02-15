---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: fd38b68c8133cbc498bbc50ffea84b48e58198a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112580"
---
# <span data-ttu-id="d6ad9-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d6ad9-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="d6ad9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ad9-103">Remover nós do tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="d6ad9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6ad9-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6ad9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6ad9-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ad9-106">Use **Remove-AzServiceFabricNode** para remover nós de um tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="d6ad9-107">A remoção só será possível se atender às métricas de saúde do cluster.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="d6ad9-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6ad9-108">EXAMPLES</span></span>

### <span data-ttu-id="d6ad9-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6ad9-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="d6ad9-110">Esse comando removerá dois nós do NodeType 'nt1'.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="d6ad9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6ad9-111">PARAMETERS</span></span>

### <span data-ttu-id="d6ad9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ad9-112">-DefaultProfile</span></span>
<span data-ttu-id="d6ad9-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ad9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6ad9-114">-Name</span></span>
<span data-ttu-id="d6ad9-115">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="d6ad9-115">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ad9-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="d6ad9-116">-NodeType</span></span>
<span data-ttu-id="d6ad9-117">Nome do tipo nó</span><span class="sxs-lookup"><span data-stu-id="d6ad9-117">Node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ad9-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="d6ad9-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="d6ad9-119">O número de nós a adicionar</span><span class="sxs-lookup"><span data-stu-id="d6ad9-119">The number of nodes to add</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ad9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ad9-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6ad9-121">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-121">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ad9-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d6ad9-122">-Confirm</span></span>
<span data-ttu-id="d6ad9-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ad9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ad9-124">-WhatIf</span></span>
<span data-ttu-id="d6ad9-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6ad9-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ad9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ad9-127">CommonParameters</span></span>
<span data-ttu-id="d6ad9-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ad9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ad9-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6ad9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ad9-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="d6ad9-130">INPUTS</span></span>

### <span data-ttu-id="d6ad9-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d6ad9-131">System.Int32</span></span>

### <span data-ttu-id="d6ad9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d6ad9-132">System.String</span></span>

## <span data-ttu-id="d6ad9-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="d6ad9-133">OUTPUTS</span></span>

### <span data-ttu-id="d6ad9-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="d6ad9-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d6ad9-135">Notas</span><span class="sxs-lookup"><span data-stu-id="d6ad9-135">NOTES</span></span>

## <span data-ttu-id="d6ad9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6ad9-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6ad9-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d6ad9-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
