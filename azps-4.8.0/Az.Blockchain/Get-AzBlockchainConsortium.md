---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954428"
---
# <span data-ttu-id="92a02-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="92a02-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="92a02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92a02-102">SYNOPSIS</span></span>
<span data-ttu-id="92a02-103">Lista os consórcio disponíveis para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="92a02-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="92a02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92a02-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92a02-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92a02-105">DESCRIPTION</span></span>
<span data-ttu-id="92a02-106">Lista os consórcio disponíveis para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="92a02-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="92a02-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92a02-107">EXAMPLES</span></span>

### <span data-ttu-id="92a02-108">Exemplo 1: obter consórcios Blockchain.</span><span class="sxs-lookup"><span data-stu-id="92a02-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="92a02-109">Esse comando lista os Consortiums em uma assinatura para um local específico.</span><span class="sxs-lookup"><span data-stu-id="92a02-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="92a02-110">OS</span><span class="sxs-lookup"><span data-stu-id="92a02-110">PARAMETERS</span></span>

### <span data-ttu-id="92a02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a02-111">-DefaultProfile</span></span>
<span data-ttu-id="92a02-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92a02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92a02-113">-Local</span><span class="sxs-lookup"><span data-stu-id="92a02-113">-Location</span></span>
<span data-ttu-id="92a02-114">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="92a02-114">Location Name.</span></span>

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

### <span data-ttu-id="92a02-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92a02-115">-SubscriptionId</span></span>
<span data-ttu-id="92a02-116">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="92a02-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="92a02-117">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="92a02-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="92a02-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="92a02-118">-Confirm</span></span>
<span data-ttu-id="92a02-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a02-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a02-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a02-120">-WhatIf</span></span>
<span data-ttu-id="92a02-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92a02-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92a02-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92a02-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a02-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a02-123">CommonParameters</span></span>
<span data-ttu-id="92a02-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a02-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a02-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92a02-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a02-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92a02-126">INPUTS</span></span>

## <span data-ttu-id="92a02-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92a02-127">OUTPUTS</span></span>

### <span data-ttu-id="92a02-128">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="92a02-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="92a02-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92a02-129">NOTES</span></span>

<span data-ttu-id="92a02-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="92a02-130">ALIASES</span></span>

## <span data-ttu-id="92a02-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92a02-131">RELATED LINKS</span></span>

