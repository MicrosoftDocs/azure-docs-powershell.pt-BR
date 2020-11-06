---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 578210490d92e272e3e4867fb7f96f40a1a39782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440032"
---
# <span data-ttu-id="c2fb8-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c2fb8-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="c2fb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fb8-103">Remover nós do tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2fb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2fb8-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2fb8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="c2fb8-106">Use **Remove-AzureRmServiceFabricNode** para remover nós de um tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="c2fb8-107">A remoção continuará somente se atender as métricas de integridade do cluster.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="c2fb8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2fb8-108">EXAMPLES</span></span>

### <span data-ttu-id="c2fb8-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2fb8-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="c2fb8-110">Esse comando removerá 2 nós do NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="c2fb8-111">OS</span><span class="sxs-lookup"><span data-stu-id="c2fb8-111">PARAMETERS</span></span>

### <span data-ttu-id="c2fb8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fb8-112">-DefaultProfile</span></span>
<span data-ttu-id="c2fb8-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2fb8-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2fb8-114">-Name</span></span>
<span data-ttu-id="c2fb8-115">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c2fb8-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c2fb8-116">-NodeType</span></span>
<span data-ttu-id="c2fb8-117">Nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-117">Node type name.</span></span>

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

### <span data-ttu-id="c2fb8-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="c2fb8-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="c2fb8-119">Número de nós a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-119">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="c2fb8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2fb8-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2fb8-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c2fb8-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c2fb8-122">-Confirm</span></span>
<span data-ttu-id="c2fb8-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2fb8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2fb8-124">-WhatIf</span></span>
<span data-ttu-id="c2fb8-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2fb8-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2fb8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fb8-127">CommonParameters</span></span>
<span data-ttu-id="c2fb8-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fb8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fb8-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2fb8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fb8-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2fb8-130">INPUTS</span></span>

### <span data-ttu-id="c2fb8-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c2fb8-131">System.Int32</span></span>
<span data-ttu-id="c2fb8-132">Parâmetros: NumberOfNodesToRemove (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c2fb8-132">Parameters: NumberOfNodesToRemove (ByValue)</span></span>

### <span data-ttu-id="c2fb8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c2fb8-133">System.String</span></span>
<span data-ttu-id="c2fb8-134">Parâmetros: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c2fb8-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="c2fb8-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2fb8-135">OUTPUTS</span></span>

### <span data-ttu-id="c2fb8-136">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c2fb8-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c2fb8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2fb8-137">NOTES</span></span>

## <span data-ttu-id="c2fb8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2fb8-138">RELATED LINKS</span></span>

[<span data-ttu-id="c2fb8-139">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c2fb8-139">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
