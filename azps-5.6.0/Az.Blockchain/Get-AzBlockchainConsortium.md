---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: 077b1f18e18fbf47d8c89d02c44722c0a1561dac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885747"
---
# <span data-ttu-id="cc93a-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="cc93a-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="cc93a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc93a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc93a-103">Lista os consorciados disponíveis para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="cc93a-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="cc93a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cc93a-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc93a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cc93a-105">DESCRIPTION</span></span>
<span data-ttu-id="cc93a-106">Lista os consorciados disponíveis para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="cc93a-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="cc93a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc93a-107">EXAMPLES</span></span>

### <span data-ttu-id="cc93a-108">Exemplo 1: Obter os consorciados de Blockchain.</span><span class="sxs-lookup"><span data-stu-id="cc93a-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="cc93a-109">Este comando lista os consorciados sob uma assinatura para um local específico.</span><span class="sxs-lookup"><span data-stu-id="cc93a-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="cc93a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cc93a-110">PARAMETERS</span></span>

### <span data-ttu-id="cc93a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc93a-111">-DefaultProfile</span></span>
<span data-ttu-id="cc93a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc93a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc93a-113">-Location</span><span class="sxs-lookup"><span data-stu-id="cc93a-113">-Location</span></span>
<span data-ttu-id="cc93a-114">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="cc93a-114">Location Name.</span></span>

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

### <span data-ttu-id="cc93a-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc93a-115">-SubscriptionId</span></span>
<span data-ttu-id="cc93a-116">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc93a-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cc93a-117">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cc93a-117">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc93a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc93a-118">-Confirm</span></span>
<span data-ttu-id="cc93a-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc93a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc93a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc93a-120">-WhatIf</span></span>
<span data-ttu-id="cc93a-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc93a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc93a-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc93a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc93a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc93a-123">CommonParameters</span></span>
<span data-ttu-id="cc93a-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc93a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc93a-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc93a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc93a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc93a-126">INPUTS</span></span>

## <span data-ttu-id="cc93a-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cc93a-127">OUTPUTS</span></span>

### <span data-ttu-id="cc93a-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="cc93a-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="cc93a-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="cc93a-129">NOTES</span></span>

<span data-ttu-id="cc93a-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cc93a-130">ALIASES</span></span>

## <span data-ttu-id="cc93a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc93a-131">RELATED LINKS</span></span>

