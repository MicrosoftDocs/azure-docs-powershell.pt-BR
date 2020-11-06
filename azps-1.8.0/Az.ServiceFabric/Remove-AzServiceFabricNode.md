---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 22aa963f772a87b97a0a64ccdaef5ad6ef004696
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599110"
---
# <span data-ttu-id="32e45-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="32e45-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="32e45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32e45-102">SYNOPSIS</span></span>
<span data-ttu-id="32e45-103">Remover nós do tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="32e45-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="32e45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32e45-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e45-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32e45-105">DESCRIPTION</span></span>
<span data-ttu-id="32e45-106">Use **Remove-AzServiceFabricNode** para remover nós de um tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="32e45-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="32e45-107">A remoção continuará somente se atender as métricas de integridade do cluster.</span><span class="sxs-lookup"><span data-stu-id="32e45-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="32e45-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32e45-108">EXAMPLES</span></span>

### <span data-ttu-id="32e45-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32e45-109">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="32e45-110">Esse comando removerá 2 nós do NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="32e45-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="32e45-111">OS</span><span class="sxs-lookup"><span data-stu-id="32e45-111">PARAMETERS</span></span>

### <span data-ttu-id="32e45-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e45-112">-DefaultProfile</span></span>
<span data-ttu-id="32e45-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32e45-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32e45-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="32e45-114">-Name</span></span>
<span data-ttu-id="32e45-115">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="32e45-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="32e45-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="32e45-116">-NodeType</span></span>
<span data-ttu-id="32e45-117">Nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="32e45-117">Node type name.</span></span>

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

### <span data-ttu-id="32e45-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="32e45-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="32e45-119">Número de nós a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="32e45-119">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="32e45-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e45-120">-ResourceGroupName</span></span>
<span data-ttu-id="32e45-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="32e45-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="32e45-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32e45-122">-Confirm</span></span>
<span data-ttu-id="32e45-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e45-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e45-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e45-124">-WhatIf</span></span>
<span data-ttu-id="32e45-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32e45-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32e45-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32e45-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e45-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e45-127">CommonParameters</span></span>
<span data-ttu-id="32e45-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e45-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e45-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e45-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e45-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32e45-130">INPUTS</span></span>

### <span data-ttu-id="32e45-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="32e45-131">System.Int32</span></span>

### <span data-ttu-id="32e45-132">System. String</span><span class="sxs-lookup"><span data-stu-id="32e45-132">System.String</span></span>

## <span data-ttu-id="32e45-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32e45-133">OUTPUTS</span></span>

### <span data-ttu-id="32e45-134">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="32e45-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="32e45-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32e45-135">NOTES</span></span>

## <span data-ttu-id="32e45-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32e45-136">RELATED LINKS</span></span>

[<span data-ttu-id="32e45-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="32e45-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md) 
