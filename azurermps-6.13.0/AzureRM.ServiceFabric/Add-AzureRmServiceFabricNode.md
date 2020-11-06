---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: 687be1ddd20c431e5226fe7f0516cc480e79fce8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602444"
---
# <span data-ttu-id="1d9e9-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="1d9e9-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="1d9e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9e9-103">Adicione nós ao tipo de nó específico no cluster.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d9e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d9e9-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d9e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d9e9-105">DESCRIPTION</span></span>
<span data-ttu-id="1d9e9-106">Use **Add-AzureRmServiceFabricNode** para adicionar nós ao tipo de nó específico.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="1d9e9-107">Você só precisa especificar o número de nós que deseja adicionar a um tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="1d9e9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d9e9-108">EXAMPLES</span></span>

### <span data-ttu-id="1d9e9-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d9e9-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="1d9e9-110">Esse comando adicionará 2 nós ao tipo de nó ' N1 '.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="1d9e9-111">OS</span><span class="sxs-lookup"><span data-stu-id="1d9e9-111">PARAMETERS</span></span>

### <span data-ttu-id="1d9e9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9e9-112">-DefaultProfile</span></span>
<span data-ttu-id="1d9e9-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d9e9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d9e9-114">-Name</span></span>
<span data-ttu-id="1d9e9-115">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1d9e9-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="1d9e9-116">-NodeType</span></span>
<span data-ttu-id="1d9e9-117">Nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-117">Node type name.</span></span>

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

### <span data-ttu-id="1d9e9-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="1d9e9-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="1d9e9-119">Número da instância da VM.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-119">VM instance number.</span></span>

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

### <span data-ttu-id="1d9e9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d9e9-120">-ResourceGroupName</span></span>
<span data-ttu-id="1d9e9-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1d9e9-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1d9e9-122">-Confirm</span></span>
<span data-ttu-id="1d9e9-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d9e9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d9e9-124">-WhatIf</span></span>
<span data-ttu-id="1d9e9-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d9e9-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d9e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9e9-127">CommonParameters</span></span>
<span data-ttu-id="1d9e9-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d9e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9e9-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d9e9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9e9-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d9e9-130">INPUTS</span></span>

### <span data-ttu-id="1d9e9-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1d9e9-131">System.Int32</span></span>
<span data-ttu-id="1d9e9-132">Parâmetros: NumberOfNodesToAdd (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d9e9-132">Parameters: NumberOfNodesToAdd (ByValue)</span></span>

### <span data-ttu-id="1d9e9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1d9e9-133">System.String</span></span>
<span data-ttu-id="1d9e9-134">Parâmetros: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d9e9-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="1d9e9-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d9e9-135">OUTPUTS</span></span>

### <span data-ttu-id="1d9e9-136">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="1d9e9-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1d9e9-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d9e9-137">NOTES</span></span>

## <span data-ttu-id="1d9e9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d9e9-138">RELATED LINKS</span></span>

[<span data-ttu-id="1d9e9-139">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="1d9e9-139">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
