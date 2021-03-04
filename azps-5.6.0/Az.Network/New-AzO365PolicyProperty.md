---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: a2b3a4878db022018bd0fae1d8e43e3700dd5e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886181"
---
# <span data-ttu-id="0da6c-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="0da6c-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="0da6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da6c-102">SYNOPSIS</span></span>
<span data-ttu-id="0da6c-103">Crie um objeto de política de quebra de tráfego do Office 365.</span><span class="sxs-lookup"><span data-stu-id="0da6c-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="0da6c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0da6c-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0da6c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0da6c-105">DESCRIPTION</span></span>
<span data-ttu-id="0da6c-106">Crie uma política de quebra do Office 365 a ser usada com New-AzVpnSite e Update-AzVpnSite cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0da6c-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="0da6c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0da6c-107">EXAMPLES</span></span>

### <span data-ttu-id="0da6c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0da6c-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="0da6c-109">Crie uma política de quebra de tráfego do office 365 com a quebra permitida para permitir e otimizar a categoria de tráfego.</span><span class="sxs-lookup"><span data-stu-id="0da6c-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="0da6c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0da6c-110">PARAMETERS</span></span>

### <span data-ttu-id="0da6c-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="0da6c-111">-Allow</span></span>
<span data-ttu-id="0da6c-112">Separar o tráfego de categoria de autorização.</span><span class="sxs-lookup"><span data-stu-id="0da6c-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="0da6c-113">-Default</span><span class="sxs-lookup"><span data-stu-id="0da6c-113">-Default</span></span>
<span data-ttu-id="0da6c-114">Separar o tráfego de categoria padrão.</span><span class="sxs-lookup"><span data-stu-id="0da6c-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="0da6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da6c-115">-DefaultProfile</span></span>
<span data-ttu-id="0da6c-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0da6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da6c-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="0da6c-117">-Optimize</span></span>
<span data-ttu-id="0da6c-118">Separar o tráfego de categoria otimizada.</span><span class="sxs-lookup"><span data-stu-id="0da6c-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="0da6c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da6c-119">CommonParameters</span></span>
<span data-ttu-id="0da6c-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da6c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da6c-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0da6c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da6c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0da6c-122">INPUTS</span></span>

### <span data-ttu-id="0da6c-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0da6c-123">None</span></span>

## <span data-ttu-id="0da6c-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0da6c-124">OUTPUTS</span></span>

### <span data-ttu-id="0da6c-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="0da6c-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="0da6c-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="0da6c-126">NOTES</span></span>

## <span data-ttu-id="0da6c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0da6c-127">RELATED LINKS</span></span>
