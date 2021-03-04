---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 9507271fe283277c212e4ed8d4117483a2797857
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887593"
---
# <span data-ttu-id="7cddc-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7cddc-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="7cddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cddc-102">SYNOPSIS</span></span>
<span data-ttu-id="7cddc-103">Para verificar se um nome de recurso está disponível.</span><span class="sxs-lookup"><span data-stu-id="7cddc-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="7cddc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7cddc-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7cddc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7cddc-105">DESCRIPTION</span></span>
<span data-ttu-id="7cddc-106">Para verificar se um nome de recurso está disponível.</span><span class="sxs-lookup"><span data-stu-id="7cddc-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="7cddc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cddc-107">EXAMPLES</span></span>

### <span data-ttu-id="7cddc-108">Exemplo 1: Verificar se um nome de recurso está disponível</span><span class="sxs-lookup"><span data-stu-id="7cddc-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="7cddc-109">O comando verifica se um nome de recurso está disponível.</span><span class="sxs-lookup"><span data-stu-id="7cddc-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="7cddc-110">Exemplo 2: Verificar se um nome de recurso está disponível</span><span class="sxs-lookup"><span data-stu-id="7cddc-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="7cddc-111">O comando verifica se um nome de recurso está disponível.</span><span class="sxs-lookup"><span data-stu-id="7cddc-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="7cddc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7cddc-112">PARAMETERS</span></span>

### <span data-ttu-id="7cddc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cddc-113">-DefaultProfile</span></span>
<span data-ttu-id="7cddc-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7cddc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cddc-115">-Location</span><span class="sxs-lookup"><span data-stu-id="7cddc-115">-Location</span></span>
<span data-ttu-id="7cddc-116">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="7cddc-116">Location Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cddc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7cddc-117">-Name</span></span>
<span data-ttu-id="7cddc-118">Obtém ou define o nome a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="7cddc-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="7cddc-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cddc-119">-SubscriptionId</span></span>
<span data-ttu-id="7cddc-120">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7cddc-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7cddc-121">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7cddc-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cddc-122">-Type</span><span class="sxs-lookup"><span data-stu-id="7cddc-122">-Type</span></span>
<span data-ttu-id="7cddc-123">Obtém ou define o tipo do recurso a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="7cddc-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="7cddc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cddc-124">-Confirm</span></span>
<span data-ttu-id="7cddc-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cddc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cddc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cddc-126">-WhatIf</span></span>
<span data-ttu-id="7cddc-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7cddc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cddc-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7cddc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cddc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cddc-129">CommonParameters</span></span>
<span data-ttu-id="7cddc-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cddc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cddc-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cddc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cddc-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cddc-132">INPUTS</span></span>

## <span data-ttu-id="7cddc-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7cddc-133">OUTPUTS</span></span>

### <span data-ttu-id="7cddc-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="7cddc-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="7cddc-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="7cddc-135">NOTES</span></span>

<span data-ttu-id="7cddc-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7cddc-136">ALIASES</span></span>

## <span data-ttu-id="7cddc-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cddc-137">RELATED LINKS</span></span>

