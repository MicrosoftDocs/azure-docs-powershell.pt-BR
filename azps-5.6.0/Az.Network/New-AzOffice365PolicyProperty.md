---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9e48bfd243133052f526f2b9adcbef2072cdd2cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886180"
---
# <span data-ttu-id="76ce0-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="76ce0-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="76ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="76ce0-103">Defina uma nova política de quebra de tráfego do Office 365 a ser usada com um site de Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="76ce0-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="76ce0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="76ce0-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76ce0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="76ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="76ce0-106">O New-AzOffice365PolicyProperties define uma política de quebra do Office 365 que deve ser usada com um site de Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="76ce0-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="76ce0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76ce0-107">EXAMPLES</span></span>

### <span data-ttu-id="76ce0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76ce0-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="76ce0-109">Crie o objeto de política de quebra de tráfego do Office 365 a ser usado com comandos de site do Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="76ce0-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="76ce0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="76ce0-110">PARAMETERS</span></span>

### <span data-ttu-id="76ce0-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="76ce0-111">-Allow</span></span>
<span data-ttu-id="76ce0-112">Separar o tráfego de categoria de autorização.</span><span class="sxs-lookup"><span data-stu-id="76ce0-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="76ce0-113">-Default</span><span class="sxs-lookup"><span data-stu-id="76ce0-113">-Default</span></span>
<span data-ttu-id="76ce0-114">Separar o tráfego de categoria padrão.</span><span class="sxs-lookup"><span data-stu-id="76ce0-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="76ce0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ce0-115">-DefaultProfile</span></span>
<span data-ttu-id="76ce0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76ce0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76ce0-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="76ce0-117">-Optimize</span></span>
<span data-ttu-id="76ce0-118">Separar o tráfego de categoria otimizada.</span><span class="sxs-lookup"><span data-stu-id="76ce0-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="76ce0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ce0-119">CommonParameters</span></span>
<span data-ttu-id="76ce0-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ce0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ce0-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76ce0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ce0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76ce0-122">INPUTS</span></span>

### <span data-ttu-id="76ce0-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="76ce0-123">None</span></span>

## <span data-ttu-id="76ce0-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="76ce0-124">OUTPUTS</span></span>

### <span data-ttu-id="76ce0-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="76ce0-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="76ce0-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="76ce0-126">NOTES</span></span>

## <span data-ttu-id="76ce0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76ce0-127">RELATED LINKS</span></span>
