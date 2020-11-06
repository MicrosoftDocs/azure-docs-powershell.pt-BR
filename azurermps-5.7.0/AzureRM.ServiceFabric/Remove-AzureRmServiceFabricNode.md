---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 6df403d432d212e1d0f8d074b9ac57caad438f83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431595"
---
# <span data-ttu-id="376f6-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="376f6-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="376f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="376f6-102">SYNOPSIS</span></span>
<span data-ttu-id="376f6-103">Remover nós do tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="376f6-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="376f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="376f6-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="376f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="376f6-105">DESCRIPTION</span></span>
<span data-ttu-id="376f6-106">Use **Remove-AzureRmServiceFabricNode** para remover nós de um tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="376f6-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="376f6-107">A remoção continuará somente se atender as métricas de integridade do cluster.</span><span class="sxs-lookup"><span data-stu-id="376f6-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="376f6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="376f6-108">EXAMPLES</span></span>

### <span data-ttu-id="376f6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="376f6-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="376f6-110">Esse comando removerá 2 nós do NodeType ' NT1 '.</span><span class="sxs-lookup"><span data-stu-id="376f6-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="376f6-111">OS</span><span class="sxs-lookup"><span data-stu-id="376f6-111">PARAMETERS</span></span>

### <span data-ttu-id="376f6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376f6-112">-DefaultProfile</span></span>
<span data-ttu-id="376f6-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="376f6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376f6-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="376f6-114">-Name</span></span>
<span data-ttu-id="376f6-115">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="376f6-115">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376f6-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="376f6-116">-NodeType</span></span>
<span data-ttu-id="376f6-117">Nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="376f6-117">Node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="376f6-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="376f6-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="376f6-119">Número de nós a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="376f6-119">Number of nodes to remove.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="376f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="376f6-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="376f6-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376f6-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="376f6-122">-Confirm</span></span>
<span data-ttu-id="376f6-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376f6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="376f6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="376f6-124">-WhatIf</span></span>
<span data-ttu-id="376f6-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="376f6-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="376f6-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="376f6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="376f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376f6-127">CommonParameters</span></span>
<span data-ttu-id="376f6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="376f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376f6-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376f6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376f6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="376f6-130">INPUTS</span></span>

### <span data-ttu-id="376f6-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="376f6-131">System.Int32</span></span>
<span data-ttu-id="376f6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="376f6-132">System.String</span></span>

## <span data-ttu-id="376f6-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="376f6-133">OUTPUTS</span></span>

### <span data-ttu-id="376f6-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="376f6-134">System.Object</span></span>

## <span data-ttu-id="376f6-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="376f6-135">NOTES</span></span>

## <span data-ttu-id="376f6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="376f6-136">RELATED LINKS</span></span>

[<span data-ttu-id="376f6-137">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="376f6-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
