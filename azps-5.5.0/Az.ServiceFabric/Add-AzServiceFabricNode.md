---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 41c78b659a39d3df52185eeb2b67e4c921f22b45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118657"
---
# <span data-ttu-id="e3271-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e3271-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="e3271-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3271-102">SYNOPSIS</span></span>
<span data-ttu-id="e3271-103">Adicione nós ao tipo de nó específico no cluster.</span><span class="sxs-lookup"><span data-stu-id="e3271-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="e3271-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3271-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3271-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3271-105">DESCRIPTION</span></span>
<span data-ttu-id="e3271-106">Use **Add-AzServiceFabricNode** para adicionar nós ao tipo de nó específico.</span><span class="sxs-lookup"><span data-stu-id="e3271-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="e3271-107">Você só precisa especificar o número de nós que deseja adicionar a um tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="e3271-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="e3271-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3271-108">EXAMPLES</span></span>

### <span data-ttu-id="e3271-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3271-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="e3271-110">Esse comando adicionará 2 nós ao tipo de nó 'n1'.</span><span class="sxs-lookup"><span data-stu-id="e3271-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="e3271-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3271-111">PARAMETERS</span></span>

### <span data-ttu-id="e3271-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3271-112">-DefaultProfile</span></span>
<span data-ttu-id="e3271-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3271-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3271-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3271-114">-Name</span></span>
<span data-ttu-id="e3271-115">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="e3271-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="e3271-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="e3271-116">-NodeType</span></span>
<span data-ttu-id="e3271-117">Nome do tipo nó</span><span class="sxs-lookup"><span data-stu-id="e3271-117">Node type name</span></span>

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

### <span data-ttu-id="e3271-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="e3271-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="e3271-119">O número de nós a adicionar</span><span class="sxs-lookup"><span data-stu-id="e3271-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="e3271-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3271-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3271-121">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3271-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e3271-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e3271-122">-Confirm</span></span>
<span data-ttu-id="e3271-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3271-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3271-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3271-124">-WhatIf</span></span>
<span data-ttu-id="e3271-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e3271-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3271-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3271-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3271-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3271-127">CommonParameters</span></span>
<span data-ttu-id="e3271-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3271-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3271-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3271-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3271-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="e3271-130">INPUTS</span></span>

### <span data-ttu-id="e3271-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e3271-131">System.Int32</span></span>

### <span data-ttu-id="e3271-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e3271-132">System.String</span></span>

## <span data-ttu-id="e3271-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="e3271-133">OUTPUTS</span></span>

### <span data-ttu-id="e3271-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="e3271-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e3271-135">Notas</span><span class="sxs-lookup"><span data-stu-id="e3271-135">NOTES</span></span>

## <span data-ttu-id="e3271-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3271-136">RELATED LINKS</span></span>

[<span data-ttu-id="e3271-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e3271-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
