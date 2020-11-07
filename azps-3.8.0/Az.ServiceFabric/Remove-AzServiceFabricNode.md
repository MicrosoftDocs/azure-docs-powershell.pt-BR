---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 96706ef98a0b21bab06e2c6e8fae947dcd205271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941672"
---
# <span data-ttu-id="deaca-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="deaca-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="deaca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="deaca-102">SYNOPSIS</span></span>
<span data-ttu-id="deaca-103">Remover nós do tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="deaca-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="deaca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deaca-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deaca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="deaca-105">DESCRIPTION</span></span>
<span data-ttu-id="deaca-106">Use **Remove-AzServiceFabricNode** para remover nós de um tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="deaca-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="deaca-107">A remoção continuará somente se atender as métricas de integridade do cluster.</span><span class="sxs-lookup"><span data-stu-id="deaca-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="deaca-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="deaca-108">EXAMPLES</span></span>

### <span data-ttu-id="deaca-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="deaca-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="deaca-110">Esse comando removerá 2 nós do NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="deaca-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="deaca-111">OS</span><span class="sxs-lookup"><span data-stu-id="deaca-111">PARAMETERS</span></span>

### <span data-ttu-id="deaca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deaca-112">-DefaultProfile</span></span>
<span data-ttu-id="deaca-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="deaca-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deaca-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="deaca-114">-Name</span></span>
<span data-ttu-id="deaca-115">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="deaca-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="deaca-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="deaca-116">-NodeType</span></span>
<span data-ttu-id="deaca-117">Nome do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="deaca-117">Node type name</span></span>

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

### <span data-ttu-id="deaca-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="deaca-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="deaca-119">O número de nós a serem adicionados</span><span class="sxs-lookup"><span data-stu-id="deaca-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="deaca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deaca-120">-ResourceGroupName</span></span>
<span data-ttu-id="deaca-121">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="deaca-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="deaca-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="deaca-122">-Confirm</span></span>
<span data-ttu-id="deaca-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deaca-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deaca-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deaca-124">-WhatIf</span></span>
<span data-ttu-id="deaca-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="deaca-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deaca-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="deaca-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deaca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deaca-127">CommonParameters</span></span>
<span data-ttu-id="deaca-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deaca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deaca-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deaca-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deaca-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="deaca-130">INPUTS</span></span>

### <span data-ttu-id="deaca-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="deaca-131">System.Int32</span></span>

### <span data-ttu-id="deaca-132">System. String</span><span class="sxs-lookup"><span data-stu-id="deaca-132">System.String</span></span>

## <span data-ttu-id="deaca-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="deaca-133">OUTPUTS</span></span>

### <span data-ttu-id="deaca-134">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="deaca-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="deaca-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="deaca-135">NOTES</span></span>

## <span data-ttu-id="deaca-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="deaca-136">RELATED LINKS</span></span>

[<span data-ttu-id="deaca-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="deaca-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
