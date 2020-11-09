---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282197"
---
# <span data-ttu-id="183a1-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="183a1-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="183a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="183a1-102">SYNOPSIS</span></span>
<span data-ttu-id="183a1-103">Crie um objeto de política de debates do tráfego do Office 365.</span><span class="sxs-lookup"><span data-stu-id="183a1-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="183a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="183a1-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="183a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="183a1-105">DESCRIPTION</span></span>
<span data-ttu-id="183a1-106">Crie uma política de debates do Office 365 para ser usada com cmdlets New-AzVpnSite e Update-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="183a1-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="183a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="183a1-107">EXAMPLES</span></span>

### <span data-ttu-id="183a1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="183a1-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="183a1-109">Crie uma política de debates de tráfego do Office 365 com o debate permitido para permitir e otimizar a categoria de tráfego.</span><span class="sxs-lookup"><span data-stu-id="183a1-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="183a1-110">OS</span><span class="sxs-lookup"><span data-stu-id="183a1-110">PARAMETERS</span></span>

### <span data-ttu-id="183a1-111">-Permitir</span><span class="sxs-lookup"><span data-stu-id="183a1-111">-Allow</span></span>
<span data-ttu-id="183a1-112">Debate o tráfego permitir categoria.</span><span class="sxs-lookup"><span data-stu-id="183a1-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="183a1-113">-Padrão</span><span class="sxs-lookup"><span data-stu-id="183a1-113">-Default</span></span>
<span data-ttu-id="183a1-114">Debate do tráfego de categoria padrão.</span><span class="sxs-lookup"><span data-stu-id="183a1-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="183a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183a1-115">-DefaultProfile</span></span>
<span data-ttu-id="183a1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="183a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="183a1-117">-Otimizar</span><span class="sxs-lookup"><span data-stu-id="183a1-117">-Optimize</span></span>
<span data-ttu-id="183a1-118">Debates sobre o tráfego de otimização da categoria.</span><span class="sxs-lookup"><span data-stu-id="183a1-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="183a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183a1-119">CommonParameters</span></span>
<span data-ttu-id="183a1-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="183a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183a1-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="183a1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183a1-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="183a1-122">INPUTS</span></span>

### <span data-ttu-id="183a1-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="183a1-123">None</span></span>

## <span data-ttu-id="183a1-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="183a1-124">OUTPUTS</span></span>

### <span data-ttu-id="183a1-125">Microsoft. Azure. Commands. Network. Models. PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="183a1-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="183a1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="183a1-126">NOTES</span></span>

## <span data-ttu-id="183a1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="183a1-127">RELATED LINKS</span></span>
