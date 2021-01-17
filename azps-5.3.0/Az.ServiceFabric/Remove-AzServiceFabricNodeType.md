---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433016"
---
# <span data-ttu-id="981e5-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="981e5-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="981e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="981e5-102">SYNOPSIS</span></span>
<span data-ttu-id="981e5-103">Remover um tipo de nó completo de um cluster.</span><span class="sxs-lookup"><span data-stu-id="981e5-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="981e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="981e5-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="981e5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="981e5-105">DESCRIPTION</span></span>
<span data-ttu-id="981e5-106">Use **Remove-AzServiceFabricNodeType** para remover todos os nós de um tipo de nó específico e o tipo de nó de um cluster.</span><span class="sxs-lookup"><span data-stu-id="981e5-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="981e5-107">Este comando não pode ser usado para excluir o tipo de nó primário.</span><span class="sxs-lookup"><span data-stu-id="981e5-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="981e5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="981e5-108">EXAMPLES</span></span>

### <span data-ttu-id="981e5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="981e5-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="981e5-110">Esse comando removerá o NodeType ' NT1 ' do cluster.</span><span class="sxs-lookup"><span data-stu-id="981e5-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="981e5-111">OS</span><span class="sxs-lookup"><span data-stu-id="981e5-111">PARAMETERS</span></span>

### <span data-ttu-id="981e5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981e5-112">-DefaultProfile</span></span>
<span data-ttu-id="981e5-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="981e5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="981e5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="981e5-114">-Name</span></span>
<span data-ttu-id="981e5-115">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="981e5-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="981e5-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="981e5-116">-NodeType</span></span>
<span data-ttu-id="981e5-117">O nome do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="981e5-117">The node type name</span></span>

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

### <span data-ttu-id="981e5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="981e5-118">-ResourceGroupName</span></span>
<span data-ttu-id="981e5-119">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="981e5-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="981e5-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="981e5-120">-Confirm</span></span>
<span data-ttu-id="981e5-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="981e5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="981e5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="981e5-122">-WhatIf</span></span>
<span data-ttu-id="981e5-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="981e5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="981e5-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="981e5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="981e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981e5-125">CommonParameters</span></span>
<span data-ttu-id="981e5-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="981e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981e5-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="981e5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981e5-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="981e5-128">INPUTS</span></span>

### <span data-ttu-id="981e5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="981e5-129">System.String</span></span>

## <span data-ttu-id="981e5-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="981e5-130">OUTPUTS</span></span>

### <span data-ttu-id="981e5-131">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="981e5-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="981e5-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="981e5-132">NOTES</span></span>

## <span data-ttu-id="981e5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="981e5-133">RELATED LINKS</span></span>
