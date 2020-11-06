---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: ebb6635cd593e37eedf4a8e70230cbf0f42e0d92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597169"
---
# <span data-ttu-id="9dffd-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9dffd-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="9dffd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9dffd-102">SYNOPSIS</span></span>
<span data-ttu-id="9dffd-103">Atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="9dffd-103">Updates an availability set.</span></span>

## <span data-ttu-id="9dffd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dffd-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dffd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9dffd-105">DESCRIPTION</span></span>
<span data-ttu-id="9dffd-106">O cmdlet **Update-AzAvailabilitySet** atualiza um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="9dffd-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="9dffd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9dffd-107">EXAMPLES</span></span>

### <span data-ttu-id="9dffd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9dffd-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="9dffd-109">Esse comando atualiza o conjunto de disponibilidade chamado ' AvSet01 ' no grupo de recursos chamado ' ResourceGroup01 ' para um conjunto de disponibilidade gerenciada.</span><span class="sxs-lookup"><span data-stu-id="9dffd-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="9dffd-110">OS</span><span class="sxs-lookup"><span data-stu-id="9dffd-110">PARAMETERS</span></span>

### <span data-ttu-id="9dffd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dffd-111">-AsJob</span></span>
<span data-ttu-id="9dffd-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="9dffd-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9dffd-113">-Availabilityset</span><span class="sxs-lookup"><span data-stu-id="9dffd-113">-AvailabilitySet</span></span>
<span data-ttu-id="9dffd-114">Especifica o objeto do conjunto de disponibilidade a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9dffd-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="9dffd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dffd-115">-DefaultProfile</span></span>
<span data-ttu-id="9dffd-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9dffd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dffd-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="9dffd-117">-Sku</span></span>
<span data-ttu-id="9dffd-118">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="9dffd-118">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dffd-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="9dffd-119">-Tag</span></span>
<span data-ttu-id="9dffd-120">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9dffd-120">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="9dffd-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9dffd-121">-Confirm</span></span>
<span data-ttu-id="9dffd-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dffd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dffd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dffd-123">-WhatIf</span></span>
<span data-ttu-id="9dffd-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9dffd-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9dffd-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9dffd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dffd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dffd-126">CommonParameters</span></span>
<span data-ttu-id="9dffd-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dffd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dffd-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dffd-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dffd-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9dffd-129">INPUTS</span></span>

### <span data-ttu-id="9dffd-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9dffd-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9dffd-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9dffd-131">OUTPUTS</span></span>

### <span data-ttu-id="9dffd-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9dffd-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9dffd-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9dffd-133">NOTES</span></span>

## <span data-ttu-id="9dffd-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dffd-134">RELATED LINKS</span></span>
