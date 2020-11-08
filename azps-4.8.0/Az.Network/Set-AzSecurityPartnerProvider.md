---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110419"
---
# <span data-ttu-id="c3376-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c3376-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="c3376-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3376-102">SYNOPSIS</span></span>
<span data-ttu-id="c3376-103">Salva uma SecurityPartnerProvider do Azure modificada.</span><span class="sxs-lookup"><span data-stu-id="c3376-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="c3376-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3376-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3376-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3376-105">DESCRIPTION</span></span>
<span data-ttu-id="c3376-106">O cmdlet **set-AzSecurityPartnerProvider** atualiza um Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c3376-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="c3376-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3376-107">EXAMPLES</span></span>

### <span data-ttu-id="c3376-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3376-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="c3376-109">OS</span><span class="sxs-lookup"><span data-stu-id="c3376-109">PARAMETERS</span></span>

### <span data-ttu-id="c3376-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3376-110">-AsJob</span></span>
<span data-ttu-id="c3376-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c3376-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3376-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3376-112">-DefaultProfile</span></span>
<span data-ttu-id="c3376-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3376-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3376-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c3376-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="c3376-115">O SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c3376-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="c3376-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3376-116">-Confirm</span></span>
<span data-ttu-id="c3376-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3376-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3376-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3376-118">-WhatIf</span></span>
<span data-ttu-id="c3376-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3376-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3376-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3376-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3376-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3376-121">CommonParameters</span></span>
<span data-ttu-id="c3376-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3376-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3376-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3376-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3376-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3376-124">INPUTS</span></span>

### <span data-ttu-id="c3376-125">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c3376-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="c3376-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3376-126">OUTPUTS</span></span>

### <span data-ttu-id="c3376-127">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c3376-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="c3376-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3376-128">NOTES</span></span>

## <span data-ttu-id="c3376-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3376-129">RELATED LINKS</span></span>
