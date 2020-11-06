---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 3da05194d74de1fe547beb66dea420a7f0e90155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429091"
---
# <span data-ttu-id="a6c26-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a6c26-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="a6c26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6c26-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c26-103">Remover um tipo de nó completo de um cluster.</span><span class="sxs-lookup"><span data-stu-id="a6c26-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6c26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6c26-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6c26-105">DESCRIPTION</span></span>
<span data-ttu-id="a6c26-106">Use **Remove-AzureRmServiceFabricNodeType** para remover todos os nós de um tipo de nó específico e o tipo de nó de um cluster.</span><span class="sxs-lookup"><span data-stu-id="a6c26-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="a6c26-107">Este comando não pode ser usado para excluir o tipo de nó primário.</span><span class="sxs-lookup"><span data-stu-id="a6c26-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="a6c26-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6c26-108">EXAMPLES</span></span>

### <span data-ttu-id="a6c26-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6c26-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="a6c26-110">Esse comando removerá o NodeType ' NT1 ' do cluster.</span><span class="sxs-lookup"><span data-stu-id="a6c26-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="a6c26-111">OS</span><span class="sxs-lookup"><span data-stu-id="a6c26-111">PARAMETERS</span></span>

### <span data-ttu-id="a6c26-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6c26-112">-Name</span></span>
<span data-ttu-id="a6c26-113">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a6c26-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a6c26-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a6c26-114">-NodeType</span></span>
<span data-ttu-id="a6c26-115">O nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a6c26-115">The node type name.</span></span>

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

### <span data-ttu-id="a6c26-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c26-116">-ResourceGroupName</span></span>
<span data-ttu-id="a6c26-117">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6c26-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a6c26-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6c26-118">-Confirm</span></span>
<span data-ttu-id="a6c26-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6c26-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c26-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c26-120">-WhatIf</span></span>
<span data-ttu-id="a6c26-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6c26-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6c26-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6c26-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c26-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c26-123">-DefaultProfile</span></span>
<span data-ttu-id="a6c26-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c26-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6c26-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c26-125">CommonParameters</span></span>
<span data-ttu-id="a6c26-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c26-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c26-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c26-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c26-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6c26-128">INPUTS</span></span>

### <span data-ttu-id="a6c26-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a6c26-129">System.String</span></span>

## <span data-ttu-id="a6c26-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6c26-130">OUTPUTS</span></span>

### <span data-ttu-id="a6c26-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="a6c26-131">System.Object</span></span>

## <span data-ttu-id="a6c26-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6c26-132">NOTES</span></span>

## <span data-ttu-id="a6c26-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6c26-133">RELATED LINKS</span></span>

