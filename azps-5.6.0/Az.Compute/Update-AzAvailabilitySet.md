---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4f268ae4278712e16e8efc126702d0130dc225cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887005"
---
# <span data-ttu-id="9daf8-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9daf8-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="9daf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9daf8-102">SYNOPSIS</span></span>
<span data-ttu-id="9daf8-103">Atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="9daf8-103">Updates an availability set.</span></span>

## <span data-ttu-id="9daf8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9daf8-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9daf8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9daf8-105">DESCRIPTION</span></span>
<span data-ttu-id="9daf8-106">O cmdlet **Update-AzAvailabilitySet** atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="9daf8-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="9daf8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9daf8-107">EXAMPLES</span></span>

### <span data-ttu-id="9daf8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9daf8-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="9daf8-109">Este comando atualiza o conjunto de disponibilidade chamado 'AvSet01' no grupo de recursos chamado 'ResourceGroup01' para um conjunto de disponibilidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="9daf8-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="9daf8-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9daf8-110">PARAMETERS</span></span>

### <span data-ttu-id="9daf8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9daf8-111">-AsJob</span></span>
<span data-ttu-id="9daf8-112">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="9daf8-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9daf8-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9daf8-113">-AvailabilitySet</span></span>
<span data-ttu-id="9daf8-114">Especifica o objeto de conjunto de disponibilidade a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9daf8-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9daf8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9daf8-115">-DefaultProfile</span></span>
<span data-ttu-id="9daf8-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9daf8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9daf8-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="9daf8-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="9daf8-118">A id de recurso do Grupo de Posicionamento de Proximidade a ser usado com esse conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="9daf8-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9daf8-119">-Sku</span><span class="sxs-lookup"><span data-stu-id="9daf8-119">-Sku</span></span>
<span data-ttu-id="9daf8-120">O nome de Sku</span><span class="sxs-lookup"><span data-stu-id="9daf8-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9daf8-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="9daf8-121">-Tag</span></span>
<span data-ttu-id="9daf8-122">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9daf8-122">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9daf8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9daf8-123">-Confirm</span></span>
<span data-ttu-id="9daf8-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9daf8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9daf8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9daf8-125">-WhatIf</span></span>
<span data-ttu-id="9daf8-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9daf8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9daf8-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9daf8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9daf8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9daf8-128">CommonParameters</span></span>
<span data-ttu-id="9daf8-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9daf8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9daf8-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9daf8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9daf8-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9daf8-131">INPUTS</span></span>

### <span data-ttu-id="9daf8-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9daf8-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9daf8-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9daf8-133">OUTPUTS</span></span>

### <span data-ttu-id="9daf8-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9daf8-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9daf8-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="9daf8-135">NOTES</span></span>

## <span data-ttu-id="9daf8-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9daf8-136">RELATED LINKS</span></span>
