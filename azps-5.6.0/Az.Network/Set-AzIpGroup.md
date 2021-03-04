---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 8f8e40f5b2209b75c52376c08b69dff8946add77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888452"
---
# <span data-ttu-id="a8810-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a8810-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="a8810-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8810-102">SYNOPSIS</span></span>
<span data-ttu-id="a8810-103">Salva um Firewall modificado.</span><span class="sxs-lookup"><span data-stu-id="a8810-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="a8810-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a8810-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8810-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a8810-105">DESCRIPTION</span></span>
<span data-ttu-id="a8810-106">O cmdlet **Set-AzIpGroup** atualiza um IpGroup do Azure</span><span class="sxs-lookup"><span data-stu-id="a8810-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="a8810-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8810-107">EXAMPLES</span></span>

### <span data-ttu-id="a8810-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8810-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="a8810-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a8810-109">PARAMETERS</span></span>

### <span data-ttu-id="a8810-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8810-110">-AsJob</span></span>
<span data-ttu-id="a8810-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a8810-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8810-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8810-112">-DefaultProfile</span></span>
<span data-ttu-id="a8810-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8810-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8810-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="a8810-114">-IpGroup</span></span>
<span data-ttu-id="a8810-115">O IpGroup</span><span class="sxs-lookup"><span data-stu-id="a8810-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8810-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8810-116">-Confirm</span></span>
<span data-ttu-id="a8810-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8810-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8810-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8810-118">-WhatIf</span></span>
<span data-ttu-id="a8810-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8810-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8810-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8810-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8810-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8810-121">CommonParameters</span></span>
<span data-ttu-id="a8810-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8810-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8810-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8810-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8810-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8810-124">INPUTS</span></span>

### <span data-ttu-id="a8810-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="a8810-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="a8810-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a8810-126">OUTPUTS</span></span>

### <span data-ttu-id="a8810-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="a8810-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="a8810-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="a8810-128">NOTES</span></span>

## <span data-ttu-id="a8810-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8810-129">RELATED LINKS</span></span>
