---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115116"
---
# <span data-ttu-id="f9288-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="f9288-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="f9288-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9288-102">SYNOPSIS</span></span>
<span data-ttu-id="f9288-103">Crie um objeto de política de quebra de tráfego do Office 365.</span><span class="sxs-lookup"><span data-stu-id="f9288-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="f9288-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9288-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9288-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9288-105">DESCRIPTION</span></span>
<span data-ttu-id="f9288-106">Crie uma política de saída do Office 365 a ser usada com cmdlets New-AzVpnSite e Update-AzVpnSite office 365.</span><span class="sxs-lookup"><span data-stu-id="f9288-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="f9288-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9288-107">EXAMPLES</span></span>

### <span data-ttu-id="f9288-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9288-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="f9288-109">Crie uma política de quebra de tráfego do Office 365 com a quebra permitida para permitir e otimizar a categoria de tráfego.</span><span class="sxs-lookup"><span data-stu-id="f9288-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="f9288-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9288-110">PARAMETERS</span></span>

### <span data-ttu-id="f9288-111">-Permitir</span><span class="sxs-lookup"><span data-stu-id="f9288-111">-Allow</span></span>
<span data-ttu-id="f9288-112">Desafore o tráfego de categoria de permitir.</span><span class="sxs-lookup"><span data-stu-id="f9288-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="f9288-113">-Padrão</span><span class="sxs-lookup"><span data-stu-id="f9288-113">-Default</span></span>
<span data-ttu-id="f9288-114">Separar o tráfego de categoria padrão.</span><span class="sxs-lookup"><span data-stu-id="f9288-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="f9288-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9288-115">-DefaultProfile</span></span>
<span data-ttu-id="f9288-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9288-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9288-117">-Otimizar</span><span class="sxs-lookup"><span data-stu-id="f9288-117">-Optimize</span></span>
<span data-ttu-id="f9288-118">Desembre o tráfego de categoria otimizado.</span><span class="sxs-lookup"><span data-stu-id="f9288-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="f9288-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9288-119">CommonParameters</span></span>
<span data-ttu-id="f9288-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9288-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9288-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9288-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9288-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9288-122">INPUTS</span></span>

### <span data-ttu-id="f9288-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f9288-123">None</span></span>

## <span data-ttu-id="f9288-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9288-124">OUTPUTS</span></span>

### <span data-ttu-id="f9288-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="f9288-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="f9288-126">Notas</span><span class="sxs-lookup"><span data-stu-id="f9288-126">NOTES</span></span>

## <span data-ttu-id="f9288-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9288-127">RELATED LINKS</span></span>
