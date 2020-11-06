---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: c7b33e3f2afd013b6fd54f6d425c0aa1d0d08bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441148"
---
# <span data-ttu-id="7a220-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7a220-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="7a220-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a220-102">SYNOPSIS</span></span>
<span data-ttu-id="7a220-103">Atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7a220-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a220-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a220-104">SYNTAX</span></span>

### <span data-ttu-id="7a220-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a220-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a220-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="7a220-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a220-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a220-107">DESCRIPTION</span></span>
<span data-ttu-id="7a220-108">O cmdlet **Update-AzureRmAvailabilitySet** atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7a220-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="7a220-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a220-109">EXAMPLES</span></span>

### <span data-ttu-id="7a220-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a220-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="7a220-111">Esse comando atualiza o conjunto de disponibilidade chamado ' AvSet01 ' no grupo de recursos chamado ' ResourceGroup01 ' para um conjunto de disponibilidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="7a220-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="7a220-112">OS</span><span class="sxs-lookup"><span data-stu-id="7a220-112">PARAMETERS</span></span>

### <span data-ttu-id="7a220-113">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="7a220-113">-AvailabilitySet</span></span>
<span data-ttu-id="7a220-114">Especifica o objeto do conjunto de disponibilidade a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="7a220-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="7a220-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a220-115">-DefaultProfile</span></span>
<span data-ttu-id="7a220-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a220-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a220-117">Gerenciados por</span><span class="sxs-lookup"><span data-stu-id="7a220-117">-Managed</span></span>
<span data-ttu-id="7a220-118">Conjunto de disponibilidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="7a220-118">Managed Availability Set</span></span>

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

### <span data-ttu-id="7a220-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="7a220-119">-Sku</span></span>
<span data-ttu-id="7a220-120">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="7a220-120">The Name of Sku</span></span>

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

### <span data-ttu-id="7a220-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a220-121">-Confirm</span></span>
<span data-ttu-id="7a220-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a220-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a220-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a220-123">-WhatIf</span></span>
<span data-ttu-id="7a220-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a220-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a220-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a220-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a220-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a220-126">CommonParameters</span></span>
<span data-ttu-id="7a220-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a220-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a220-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a220-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a220-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a220-129">INPUTS</span></span>

### <span data-ttu-id="7a220-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7a220-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="7a220-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a220-131">OUTPUTS</span></span>

### <span data-ttu-id="7a220-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7a220-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="7a220-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a220-133">NOTES</span></span>

## <span data-ttu-id="7a220-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a220-134">RELATED LINKS</span></span>

