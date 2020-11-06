---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: af8f5d38777674d761b8b55c649b048c933f2c66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429676"
---
# <span data-ttu-id="a8bf3-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a8bf3-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="a8bf3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bf3-103">Adicione nós ao tipo de nó específico no cluster.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8bf3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8bf3-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8bf3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="a8bf3-106">Use **Add-AzureRmServiceFabricNode** para adicionar nós ao tipo de nó específico.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="a8bf3-107">Você só precisa especificar o número de nós que deseja adicionar a um tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="a8bf3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8bf3-108">EXAMPLES</span></span>

### <span data-ttu-id="a8bf3-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8bf3-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="a8bf3-110">Esse comando adicionará 2 nós ao tipo de nó ' N1 '.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="a8bf3-111">OS</span><span class="sxs-lookup"><span data-stu-id="a8bf3-111">PARAMETERS</span></span>

### <span data-ttu-id="a8bf3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bf3-112">-DefaultProfile</span></span>
<span data-ttu-id="a8bf3-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8bf3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8bf3-114">-Name</span></span>
<span data-ttu-id="a8bf3-115">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a8bf3-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a8bf3-116">-NodeType</span></span>
<span data-ttu-id="a8bf3-117">Nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-117">Node type name.</span></span>

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

### <span data-ttu-id="a8bf3-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="a8bf3-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="a8bf3-119">Número da instância da VM.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-119">VM instance number.</span></span>

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

### <span data-ttu-id="a8bf3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8bf3-120">-ResourceGroupName</span></span>
<span data-ttu-id="a8bf3-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a8bf3-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a8bf3-122">-Confirm</span></span>
<span data-ttu-id="a8bf3-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8bf3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8bf3-124">-WhatIf</span></span>
<span data-ttu-id="a8bf3-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8bf3-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8bf3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bf3-127">CommonParameters</span></span>
<span data-ttu-id="a8bf3-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8bf3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bf3-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8bf3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bf3-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8bf3-130">INPUTS</span></span>

### <span data-ttu-id="a8bf3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a8bf3-131">System.String</span></span>

## <span data-ttu-id="a8bf3-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8bf3-132">OUTPUTS</span></span>

### <span data-ttu-id="a8bf3-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="a8bf3-133">System.Object</span></span>

## <span data-ttu-id="a8bf3-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8bf3-134">NOTES</span></span>

## <span data-ttu-id="a8bf3-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8bf3-135">RELATED LINKS</span></span>

[<span data-ttu-id="a8bf3-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a8bf3-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
