---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 7dccf9410ff4d03503763354aabbe6b02d0c0c6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597336"
---
# <span data-ttu-id="22c9d-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="22c9d-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="22c9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="22c9d-103">Remove um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="22c9d-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="22c9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22c9d-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22c9d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22c9d-105">DESCRIPTION</span></span>
<span data-ttu-id="22c9d-106">O cmdlet **Remove-AzAvailabilitySet** remove um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="22c9d-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="22c9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22c9d-107">EXAMPLES</span></span>

### <span data-ttu-id="22c9d-108">Exemplo 1: remover um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="22c9d-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="22c9d-109">Esse comando Remove um conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="22c9d-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="22c9d-110">OS</span><span class="sxs-lookup"><span data-stu-id="22c9d-110">PARAMETERS</span></span>

### <span data-ttu-id="22c9d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22c9d-111">-AsJob</span></span>
<span data-ttu-id="22c9d-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="22c9d-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="22c9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c9d-113">-DefaultProfile</span></span>
<span data-ttu-id="22c9d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22c9d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22c9d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="22c9d-115">-Force</span></span>
<span data-ttu-id="22c9d-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="22c9d-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c9d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="22c9d-117">-Name</span></span>
<span data-ttu-id="22c9d-118">O nome do conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="22c9d-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22c9d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c9d-119">-ResourceGroupName</span></span>
<span data-ttu-id="22c9d-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22c9d-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="22c9d-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="22c9d-121">-Confirm</span></span>
<span data-ttu-id="22c9d-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22c9d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c9d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c9d-123">-WhatIf</span></span>
<span data-ttu-id="22c9d-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22c9d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22c9d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22c9d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c9d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c9d-126">CommonParameters</span></span>
<span data-ttu-id="22c9d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c9d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c9d-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22c9d-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c9d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22c9d-129">INPUTS</span></span>

### <span data-ttu-id="22c9d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="22c9d-130">System.String</span></span>

## <span data-ttu-id="22c9d-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22c9d-131">OUTPUTS</span></span>

### <span data-ttu-id="22c9d-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="22c9d-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="22c9d-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22c9d-133">NOTES</span></span>

## <span data-ttu-id="22c9d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22c9d-134">RELATED LINKS</span></span>

[<span data-ttu-id="22c9d-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="22c9d-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="22c9d-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="22c9d-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


