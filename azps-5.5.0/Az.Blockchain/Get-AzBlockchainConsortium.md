---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112209"
---
# <span data-ttu-id="715b0-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="715b0-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="715b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="715b0-102">SYNOPSIS</span></span>
<span data-ttu-id="715b0-103">Lista os consorciados disponíveis para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="715b0-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="715b0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="715b0-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="715b0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="715b0-105">DESCRIPTION</span></span>
<span data-ttu-id="715b0-106">Lista os consorciados disponíveis para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="715b0-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="715b0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="715b0-107">EXAMPLES</span></span>

### <span data-ttu-id="715b0-108">Exemplo 1: Obter os consorciados Dols.</span><span class="sxs-lookup"><span data-stu-id="715b0-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="715b0-109">Este comando lista os consorciados sob uma assinatura para um local específico.</span><span class="sxs-lookup"><span data-stu-id="715b0-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="715b0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="715b0-110">PARAMETERS</span></span>

### <span data-ttu-id="715b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715b0-111">-DefaultProfile</span></span>
<span data-ttu-id="715b0-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="715b0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="715b0-113">-Local</span><span class="sxs-lookup"><span data-stu-id="715b0-113">-Location</span></span>
<span data-ttu-id="715b0-114">Nome do local.</span><span class="sxs-lookup"><span data-stu-id="715b0-114">Location Name.</span></span>

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

### <span data-ttu-id="715b0-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="715b0-115">-SubscriptionId</span></span>
<span data-ttu-id="715b0-116">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="715b0-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="715b0-117">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="715b0-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="715b0-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="715b0-118">-Confirm</span></span>
<span data-ttu-id="715b0-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="715b0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="715b0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="715b0-120">-WhatIf</span></span>
<span data-ttu-id="715b0-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="715b0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="715b0-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="715b0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="715b0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715b0-123">CommonParameters</span></span>
<span data-ttu-id="715b0-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715b0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715b0-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="715b0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715b0-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="715b0-126">INPUTS</span></span>

## <span data-ttu-id="715b0-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="715b0-127">OUTPUTS</span></span>

### <span data-ttu-id="715b0-128">Microsoft.Azure.PowerShell.Cmdlets.Itor.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="715b0-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="715b0-129">Notas</span><span class="sxs-lookup"><span data-stu-id="715b0-129">NOTES</span></span>

<span data-ttu-id="715b0-130">Aliases</span><span class="sxs-lookup"><span data-stu-id="715b0-130">ALIASES</span></span>

## <span data-ttu-id="715b0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="715b0-131">RELATED LINKS</span></span>

