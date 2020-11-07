---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: bc21812003ca7e71b9f7fa726aea766e924d2519
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941671"
---
# <span data-ttu-id="da71b-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="da71b-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="da71b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da71b-102">SYNOPSIS</span></span>
<span data-ttu-id="da71b-103">Remover um tipo de nó completo de um cluster.</span><span class="sxs-lookup"><span data-stu-id="da71b-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="da71b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da71b-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da71b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da71b-105">DESCRIPTION</span></span>
<span data-ttu-id="da71b-106">Use **Remove-AzServiceFabricNodeType** para remover todos os nós de um tipo de nó específico e o tipo de nó de um cluster.</span><span class="sxs-lookup"><span data-stu-id="da71b-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="da71b-107">Este comando não pode ser usado para excluir o tipo de nó primário.</span><span class="sxs-lookup"><span data-stu-id="da71b-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="da71b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da71b-108">EXAMPLES</span></span>

### <span data-ttu-id="da71b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da71b-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="da71b-110">Esse comando removerá o NodeType ' NT1 ' do cluster.</span><span class="sxs-lookup"><span data-stu-id="da71b-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="da71b-111">OS</span><span class="sxs-lookup"><span data-stu-id="da71b-111">PARAMETERS</span></span>

### <span data-ttu-id="da71b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da71b-112">-DefaultProfile</span></span>
<span data-ttu-id="da71b-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da71b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da71b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="da71b-114">-Name</span></span>
<span data-ttu-id="da71b-115">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="da71b-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="da71b-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="da71b-116">-NodeType</span></span>
<span data-ttu-id="da71b-117">O nome do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="da71b-117">The node type name</span></span>

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

### <span data-ttu-id="da71b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da71b-118">-ResourceGroupName</span></span>
<span data-ttu-id="da71b-119">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="da71b-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="da71b-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da71b-120">-Confirm</span></span>
<span data-ttu-id="da71b-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da71b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da71b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da71b-122">-WhatIf</span></span>
<span data-ttu-id="da71b-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da71b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da71b-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da71b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da71b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da71b-125">CommonParameters</span></span>
<span data-ttu-id="da71b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da71b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da71b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da71b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da71b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da71b-128">INPUTS</span></span>

### <span data-ttu-id="da71b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="da71b-129">System.String</span></span>

## <span data-ttu-id="da71b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da71b-130">OUTPUTS</span></span>

### <span data-ttu-id="da71b-131">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="da71b-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="da71b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da71b-132">NOTES</span></span>

## <span data-ttu-id="da71b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da71b-133">RELATED LINKS</span></span>
