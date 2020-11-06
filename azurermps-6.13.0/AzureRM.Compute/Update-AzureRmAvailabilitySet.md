---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 3e28cacc8dc6a27f20a93beb3e48ddcc0d0697cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432031"
---
# <span data-ttu-id="8da60-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8da60-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="8da60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8da60-102">SYNOPSIS</span></span>
<span data-ttu-id="8da60-103">Atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="8da60-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8da60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8da60-104">SYNTAX</span></span>

### <span data-ttu-id="8da60-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da60-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da60-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="8da60-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da60-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8da60-107">DESCRIPTION</span></span>
<span data-ttu-id="8da60-108">O cmdlet **Update-AzureRmAvailabilitySet** atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="8da60-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="8da60-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8da60-109">EXAMPLES</span></span>

### <span data-ttu-id="8da60-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8da60-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="8da60-111">Esse comando atualiza o conjunto de disponibilidade chamado ' AvSet01 ' no grupo de recursos chamado ' ResourceGroup01 ' para um conjunto de disponibilidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="8da60-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="8da60-112">OS</span><span class="sxs-lookup"><span data-stu-id="8da60-112">PARAMETERS</span></span>

### <span data-ttu-id="8da60-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8da60-113">-AsJob</span></span>
<span data-ttu-id="8da60-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="8da60-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8da60-115">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="8da60-115">-AvailabilitySet</span></span>
<span data-ttu-id="8da60-116">Especifica o objeto do conjunto de disponibilidade a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="8da60-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="8da60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da60-117">-DefaultProfile</span></span>
<span data-ttu-id="8da60-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8da60-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8da60-119">Gerenciados por</span><span class="sxs-lookup"><span data-stu-id="8da60-119">-Managed</span></span>
<span data-ttu-id="8da60-120">Conjunto de disponibilidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="8da60-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="8da60-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="8da60-121">-Sku</span></span>
<span data-ttu-id="8da60-122">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="8da60-122">The Name of Sku</span></span>

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

### <span data-ttu-id="8da60-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="8da60-123">-Tag</span></span>
<span data-ttu-id="8da60-124">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8da60-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="8da60-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8da60-125">-Confirm</span></span>
<span data-ttu-id="8da60-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da60-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da60-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da60-127">-WhatIf</span></span>
<span data-ttu-id="8da60-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8da60-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8da60-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8da60-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da60-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da60-130">CommonParameters</span></span>
<span data-ttu-id="8da60-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da60-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da60-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da60-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da60-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8da60-133">INPUTS</span></span>

### <span data-ttu-id="8da60-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8da60-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="8da60-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8da60-135">OUTPUTS</span></span>

### <span data-ttu-id="8da60-136">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8da60-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="8da60-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8da60-137">NOTES</span></span>

## <span data-ttu-id="8da60-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8da60-138">RELATED LINKS</span></span>
