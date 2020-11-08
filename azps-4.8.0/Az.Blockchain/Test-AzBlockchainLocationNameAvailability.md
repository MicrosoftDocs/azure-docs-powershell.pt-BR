---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113697"
---
# <span data-ttu-id="09c3a-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="09c3a-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="09c3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="09c3a-103">Para verificar se um nome de recurso está disponível.</span><span class="sxs-lookup"><span data-stu-id="09c3a-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="09c3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09c3a-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09c3a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="09c3a-106">Para verificar se um nome de recurso está disponível.</span><span class="sxs-lookup"><span data-stu-id="09c3a-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="09c3a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09c3a-107">EXAMPLES</span></span>

### <span data-ttu-id="09c3a-108">Exemplo 1: verificar se um nome de recurso está disponível</span><span class="sxs-lookup"><span data-stu-id="09c3a-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="09c3a-109">O comando verifica se um nome de recurso está disponível.</span><span class="sxs-lookup"><span data-stu-id="09c3a-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="09c3a-110">Exemplo 2: verificar se um nome de recurso está disponível</span><span class="sxs-lookup"><span data-stu-id="09c3a-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="09c3a-111">O comando verifica se um nome de recurso está disponível.</span><span class="sxs-lookup"><span data-stu-id="09c3a-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="09c3a-112">OS</span><span class="sxs-lookup"><span data-stu-id="09c3a-112">PARAMETERS</span></span>

### <span data-ttu-id="09c3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c3a-113">-DefaultProfile</span></span>
<span data-ttu-id="09c3a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09c3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09c3a-115">-Local</span><span class="sxs-lookup"><span data-stu-id="09c3a-115">-Location</span></span>
<span data-ttu-id="09c3a-116">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="09c3a-116">Location Name.</span></span>

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

### <span data-ttu-id="09c3a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="09c3a-117">-Name</span></span>
<span data-ttu-id="09c3a-118">Obtém ou define o nome a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="09c3a-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="09c3a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09c3a-119">-SubscriptionId</span></span>
<span data-ttu-id="09c3a-120">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="09c3a-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="09c3a-121">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="09c3a-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="09c3a-122">-Digite</span><span class="sxs-lookup"><span data-stu-id="09c3a-122">-Type</span></span>
<span data-ttu-id="09c3a-123">Obtém ou define o tipo do recurso a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="09c3a-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="09c3a-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09c3a-124">-Confirm</span></span>
<span data-ttu-id="09c3a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09c3a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09c3a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09c3a-126">-WhatIf</span></span>
<span data-ttu-id="09c3a-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09c3a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09c3a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09c3a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09c3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c3a-129">CommonParameters</span></span>
<span data-ttu-id="09c3a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c3a-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09c3a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c3a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09c3a-132">INPUTS</span></span>

## <span data-ttu-id="09c3a-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09c3a-133">OUTPUTS</span></span>

### <span data-ttu-id="09c3a-134">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. INameAvailability</span><span class="sxs-lookup"><span data-stu-id="09c3a-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="09c3a-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09c3a-135">NOTES</span></span>

<span data-ttu-id="09c3a-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="09c3a-136">ALIASES</span></span>

## <span data-ttu-id="09c3a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09c3a-137">RELATED LINKS</span></span>

