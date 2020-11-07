---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942508"
---
# <span data-ttu-id="1c510-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1c510-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="1c510-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c510-102">SYNOPSIS</span></span>
<span data-ttu-id="1c510-103">Salva um firewall modificado.</span><span class="sxs-lookup"><span data-stu-id="1c510-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="1c510-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c510-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c510-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c510-105">DESCRIPTION</span></span>
<span data-ttu-id="1c510-106">O cmdlet **set-AzIpGroup** atualiza um Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="1c510-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="1c510-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c510-107">EXAMPLES</span></span>

### <span data-ttu-id="1c510-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c510-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="1c510-109">OS</span><span class="sxs-lookup"><span data-stu-id="1c510-109">PARAMETERS</span></span>

### <span data-ttu-id="1c510-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c510-110">-AsJob</span></span>
<span data-ttu-id="1c510-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1c510-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c510-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c510-112">-DefaultProfile</span></span>
<span data-ttu-id="1c510-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c510-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c510-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="1c510-114">-IpGroup</span></span>
<span data-ttu-id="1c510-115">O IpGroup</span><span class="sxs-lookup"><span data-stu-id="1c510-115">The IpGroup</span></span>

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

### <span data-ttu-id="1c510-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c510-116">-Confirm</span></span>
<span data-ttu-id="1c510-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c510-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c510-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c510-118">-WhatIf</span></span>
<span data-ttu-id="1c510-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c510-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c510-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c510-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c510-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c510-121">CommonParameters</span></span>
<span data-ttu-id="1c510-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c510-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c510-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c510-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c510-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c510-124">INPUTS</span></span>

### <span data-ttu-id="1c510-125">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="1c510-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="1c510-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c510-126">OUTPUTS</span></span>

### <span data-ttu-id="1c510-127">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="1c510-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="1c510-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c510-128">NOTES</span></span>

## <span data-ttu-id="1c510-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c510-129">RELATED LINKS</span></span>
