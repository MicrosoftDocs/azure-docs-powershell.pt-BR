---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4051cbb697625f527afdf2e189953c4d6e776214
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771086"
---
# <span data-ttu-id="5d669-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5d669-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="5d669-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d669-102">SYNOPSIS</span></span>
<span data-ttu-id="5d669-103">Atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5d669-103">Updates an availability set.</span></span>

## <span data-ttu-id="5d669-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d669-104">SYNTAX</span></span>

### <span data-ttu-id="5d669-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d669-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d669-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="5d669-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d669-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d669-107">DESCRIPTION</span></span>
<span data-ttu-id="5d669-108">O cmdlet **Update-AzAvailabilitySet** atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5d669-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="5d669-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d669-109">EXAMPLES</span></span>

### <span data-ttu-id="5d669-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5d669-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="5d669-111">Esse comando atualiza o conjunto de disponibilidade chamado ' AvSet01 ' no grupo de recursos chamado ' ResourceGroup01 ' para um conjunto de disponibilidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="5d669-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="5d669-112">OS</span><span class="sxs-lookup"><span data-stu-id="5d669-112">PARAMETERS</span></span>

### <span data-ttu-id="5d669-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d669-113">-AsJob</span></span>
<span data-ttu-id="5d669-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="5d669-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5d669-115">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="5d669-115">-AvailabilitySet</span></span>
<span data-ttu-id="5d669-116">Especifica o objeto do conjunto de disponibilidade a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="5d669-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="5d669-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d669-117">-DefaultProfile</span></span>
<span data-ttu-id="5d669-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d669-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d669-119">Gerenciados por</span><span class="sxs-lookup"><span data-stu-id="5d669-119">-Managed</span></span>
<span data-ttu-id="5d669-120">Conjunto de disponibilidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="5d669-120">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d669-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="5d669-121">-Sku</span></span>
<span data-ttu-id="5d669-122">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="5d669-122">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d669-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="5d669-123">-Tag</span></span>
<span data-ttu-id="5d669-124">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5d669-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="5d669-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5d669-125">-Confirm</span></span>
<span data-ttu-id="5d669-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d669-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d669-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d669-127">-WhatIf</span></span>
<span data-ttu-id="5d669-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5d669-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d669-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d669-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d669-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d669-130">CommonParameters</span></span>
<span data-ttu-id="5d669-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d669-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d669-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d669-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d669-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d669-133">INPUTS</span></span>

### <span data-ttu-id="5d669-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5d669-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="5d669-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d669-135">OUTPUTS</span></span>

### <span data-ttu-id="5d669-136">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5d669-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="5d669-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d669-137">NOTES</span></span>

## <span data-ttu-id="5d669-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d669-138">RELATED LINKS</span></span>
