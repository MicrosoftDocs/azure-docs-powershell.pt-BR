---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112577"
---
# <span data-ttu-id="bb889-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="bb889-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="bb889-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb889-102">SYNOPSIS</span></span>
<span data-ttu-id="bb889-103">Remover um tipo de nó completo de um cluster.</span><span class="sxs-lookup"><span data-stu-id="bb889-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="bb889-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb889-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb889-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb889-105">DESCRIPTION</span></span>
<span data-ttu-id="bb889-106">Use o **Remove-AzServiceFabricNodeType** para remover todos os nós de um tipo de nó específico e o tipo de nó de um cluster.</span><span class="sxs-lookup"><span data-stu-id="bb889-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="bb889-107">Esse comando não pode ser usado para excluir o tipo de nó principal.</span><span class="sxs-lookup"><span data-stu-id="bb889-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="bb889-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb889-108">EXAMPLES</span></span>

### <span data-ttu-id="bb889-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb889-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="bb889-110">Esse comando removerá NodeType 'nt1' do cluster.</span><span class="sxs-lookup"><span data-stu-id="bb889-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="bb889-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb889-111">PARAMETERS</span></span>

### <span data-ttu-id="bb889-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb889-112">-DefaultProfile</span></span>
<span data-ttu-id="bb889-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb889-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb889-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb889-114">-Name</span></span>
<span data-ttu-id="bb889-115">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="bb889-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="bb889-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="bb889-116">-NodeType</span></span>
<span data-ttu-id="bb889-117">O nome do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="bb889-117">The node type name</span></span>

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

### <span data-ttu-id="bb889-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb889-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb889-119">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb889-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bb889-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bb889-120">-Confirm</span></span>
<span data-ttu-id="bb889-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb889-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb889-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb889-122">-WhatIf</span></span>
<span data-ttu-id="bb889-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bb889-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb889-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb889-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb889-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb889-125">CommonParameters</span></span>
<span data-ttu-id="bb889-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb889-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb889-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb889-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb889-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="bb889-128">INPUTS</span></span>

### <span data-ttu-id="bb889-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bb889-129">System.String</span></span>

## <span data-ttu-id="bb889-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="bb889-130">OUTPUTS</span></span>

### <span data-ttu-id="bb889-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="bb889-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bb889-132">Notas</span><span class="sxs-lookup"><span data-stu-id="bb889-132">NOTES</span></span>

## <span data-ttu-id="bb889-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb889-133">RELATED LINKS</span></span>
