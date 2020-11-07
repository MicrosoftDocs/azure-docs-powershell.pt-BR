---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f7d9181b5ec79434928fc8d291025aea9480b8e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786542"
---
# <span data-ttu-id="f2272-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2272-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="f2272-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2272-102">SYNOPSIS</span></span>
<span data-ttu-id="f2272-103">Atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="f2272-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2272-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2272-104">SYNTAX</span></span>

### <span data-ttu-id="f2272-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2272-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2272-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="f2272-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2272-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2272-107">DESCRIPTION</span></span>
<span data-ttu-id="f2272-108">O cmdlet **Update-AzureRmAvailabilitySet** atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="f2272-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="f2272-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2272-109">EXAMPLES</span></span>

### <span data-ttu-id="f2272-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2272-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="f2272-111">Esse comando atualiza o conjunto de disponibilidade chamado ' AvSet01 ' no grupo de recursos chamado ' ResourceGroup01 ' para um conjunto de disponibilidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="f2272-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="f2272-112">OS</span><span class="sxs-lookup"><span data-stu-id="f2272-112">PARAMETERS</span></span>

### <span data-ttu-id="f2272-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2272-113">-AsJob</span></span>
<span data-ttu-id="f2272-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="f2272-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2272-115">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="f2272-115">-AvailabilitySet</span></span>
<span data-ttu-id="f2272-116">Especifica o objeto do conjunto de disponibilidade a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="f2272-116">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2272-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2272-117">-DefaultProfile</span></span>
<span data-ttu-id="f2272-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2272-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2272-119">Gerenciados por</span><span class="sxs-lookup"><span data-stu-id="f2272-119">-Managed</span></span>
<span data-ttu-id="f2272-120">Conjunto de disponibilidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="f2272-120">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2272-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="f2272-121">-Sku</span></span>
<span data-ttu-id="f2272-122">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="f2272-122">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2272-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2272-123">-Confirm</span></span>
<span data-ttu-id="f2272-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2272-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2272-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2272-125">-WhatIf</span></span>
<span data-ttu-id="f2272-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2272-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2272-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2272-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2272-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2272-128">CommonParameters</span></span>
<span data-ttu-id="f2272-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2272-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2272-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2272-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2272-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2272-131">INPUTS</span></span>

### <span data-ttu-id="f2272-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2272-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f2272-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2272-133">OUTPUTS</span></span>

### <span data-ttu-id="f2272-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2272-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f2272-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2272-135">NOTES</span></span>

## <span data-ttu-id="f2272-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2272-136">RELATED LINKS</span></span>

