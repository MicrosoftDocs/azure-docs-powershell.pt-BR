---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775944"
---
# <span data-ttu-id="c060e-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c060e-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="c060e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c060e-102">SYNOPSIS</span></span>
<span data-ttu-id="c060e-103">Atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="c060e-103">Updates an availability set.</span></span>

## <span data-ttu-id="c060e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c060e-104">SYNTAX</span></span>

### <span data-ttu-id="c060e-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="c060e-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c060e-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="c060e-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c060e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c060e-107">DESCRIPTION</span></span>
<span data-ttu-id="c060e-108">O cmdlet **Update-AzAvailabilitySet** atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="c060e-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="c060e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c060e-109">EXAMPLES</span></span>

### <span data-ttu-id="c060e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c060e-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="c060e-111">Esse comando atualiza o conjunto de disponibilidade chamado ' AvSet01 ' no grupo de recursos chamado ' ResourceGroup01 ' para um conjunto de disponibilidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="c060e-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="c060e-112">OS</span><span class="sxs-lookup"><span data-stu-id="c060e-112">PARAMETERS</span></span>

### <span data-ttu-id="c060e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c060e-113">-AsJob</span></span>
<span data-ttu-id="c060e-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="c060e-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c060e-115">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="c060e-115">-AvailabilitySet</span></span>
<span data-ttu-id="c060e-116">Especifica o objeto do conjunto de disponibilidade a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c060e-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="c060e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c060e-117">-DefaultProfile</span></span>
<span data-ttu-id="c060e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c060e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c060e-119">Gerenciados por</span><span class="sxs-lookup"><span data-stu-id="c060e-119">-Managed</span></span>
<span data-ttu-id="c060e-120">Conjunto de disponibilidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="c060e-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="c060e-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="c060e-121">-Sku</span></span>
<span data-ttu-id="c060e-122">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="c060e-122">The Name of Sku</span></span>

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

### <span data-ttu-id="c060e-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c060e-123">-Confirm</span></span>
<span data-ttu-id="c060e-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c060e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c060e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c060e-125">-WhatIf</span></span>
<span data-ttu-id="c060e-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c060e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c060e-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c060e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c060e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c060e-128">CommonParameters</span></span>
<span data-ttu-id="c060e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c060e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c060e-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c060e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c060e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c060e-131">INPUTS</span></span>

### <span data-ttu-id="c060e-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c060e-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c060e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c060e-133">OUTPUTS</span></span>

### <span data-ttu-id="c060e-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c060e-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c060e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c060e-135">NOTES</span></span>

## <span data-ttu-id="c060e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c060e-136">RELATED LINKS</span></span>

