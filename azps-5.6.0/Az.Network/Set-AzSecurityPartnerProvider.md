---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 0a9ed100121c0f6610bcb019571fd1779f28dff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892940"
---
# <span data-ttu-id="9374d-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="9374d-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="9374d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9374d-102">SYNOPSIS</span></span>
<span data-ttu-id="9374d-103">Salva um Azure SecurityPartnerProvider modificado.</span><span class="sxs-lookup"><span data-stu-id="9374d-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="9374d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9374d-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9374d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9374d-105">DESCRIPTION</span></span>
<span data-ttu-id="9374d-106">O cmdlet **Set-AzSecurityPartnerProvider** atualiza um SecurityPartnerProvider do Azure</span><span class="sxs-lookup"><span data-stu-id="9374d-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="9374d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9374d-107">EXAMPLES</span></span>

### <span data-ttu-id="9374d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9374d-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="9374d-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9374d-109">PARAMETERS</span></span>

### <span data-ttu-id="9374d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9374d-110">-AsJob</span></span>
<span data-ttu-id="9374d-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9374d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9374d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9374d-112">-DefaultProfile</span></span>
<span data-ttu-id="9374d-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9374d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9374d-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="9374d-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="9374d-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="9374d-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9374d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9374d-116">-Confirm</span></span>
<span data-ttu-id="9374d-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9374d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9374d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9374d-118">-WhatIf</span></span>
<span data-ttu-id="9374d-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9374d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9374d-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9374d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9374d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9374d-121">CommonParameters</span></span>
<span data-ttu-id="9374d-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9374d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9374d-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9374d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9374d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9374d-124">INPUTS</span></span>

### <span data-ttu-id="9374d-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="9374d-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="9374d-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9374d-126">OUTPUTS</span></span>

### <span data-ttu-id="9374d-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="9374d-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="9374d-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="9374d-128">NOTES</span></span>

## <span data-ttu-id="9374d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9374d-129">RELATED LINKS</span></span>
