---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: aca27be11fde78df8abad1d7cdcfeff4232b60d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609557"
---
# <span data-ttu-id="728c5-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="728c5-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="728c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="728c5-102">SYNOPSIS</span></span>
<span data-ttu-id="728c5-103">Adicione nós ao tipo de nó específico no cluster.</span><span class="sxs-lookup"><span data-stu-id="728c5-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="728c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="728c5-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToAdd <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="728c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="728c5-105">DESCRIPTION</span></span>
<span data-ttu-id="728c5-106">Use **Add-AzureRmServiceFabricNode** para adicionar nós ao tipo de nó específico.</span><span class="sxs-lookup"><span data-stu-id="728c5-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="728c5-107">Você só precisa especificar o número de nós que deseja adicionar a um tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="728c5-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="728c5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="728c5-108">EXAMPLES</span></span>

### <span data-ttu-id="728c5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="728c5-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="728c5-110">Esse comando adicionará 2 nós ao tipo de nó ' N1 '.</span><span class="sxs-lookup"><span data-stu-id="728c5-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="728c5-111">OS</span><span class="sxs-lookup"><span data-stu-id="728c5-111">PARAMETERS</span></span>

### <span data-ttu-id="728c5-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="728c5-112">-Name</span></span>
<span data-ttu-id="728c5-113">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="728c5-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="728c5-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="728c5-114">-NodeType</span></span>
<span data-ttu-id="728c5-115">Nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="728c5-115">Node type name.</span></span>

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

### <span data-ttu-id="728c5-116">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="728c5-116">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="728c5-117">Número da instância da VM.</span><span class="sxs-lookup"><span data-stu-id="728c5-117">VM instance number.</span></span>

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

### <span data-ttu-id="728c5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728c5-118">-ResourceGroupName</span></span>
<span data-ttu-id="728c5-119">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="728c5-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="728c5-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="728c5-120">-Confirm</span></span>
<span data-ttu-id="728c5-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="728c5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728c5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728c5-122">-WhatIf</span></span>
<span data-ttu-id="728c5-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="728c5-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="728c5-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="728c5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="728c5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728c5-125">-DefaultProfile</span></span>
<span data-ttu-id="728c5-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="728c5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="728c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728c5-127">CommonParameters</span></span>
<span data-ttu-id="728c5-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728c5-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728c5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728c5-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="728c5-130">INPUTS</span></span>

### <span data-ttu-id="728c5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="728c5-131">System.String</span></span>

## <span data-ttu-id="728c5-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="728c5-132">OUTPUTS</span></span>

### <span data-ttu-id="728c5-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="728c5-133">System.Object</span></span>

## <span data-ttu-id="728c5-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="728c5-134">NOTES</span></span>

## <span data-ttu-id="728c5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="728c5-135">RELATED LINKS</span></span>

[<span data-ttu-id="728c5-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="728c5-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
