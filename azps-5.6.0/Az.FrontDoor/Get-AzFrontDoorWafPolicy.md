---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 83f2c49eb696ac4e3fef0f411b79af24ae95f56c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885722"
---
# <span data-ttu-id="41121-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="41121-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="41121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41121-102">SYNOPSIS</span></span>
<span data-ttu-id="41121-103">Obter política WAF</span><span class="sxs-lookup"><span data-stu-id="41121-103">Get WAF policy</span></span>

## <span data-ttu-id="41121-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="41121-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41121-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="41121-105">DESCRIPTION</span></span>
<span data-ttu-id="41121-106">O cmdlet **Get-AzFrontDoorWafPolicyGet** obtém política WAF em um grupo de recursos sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="41121-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="41121-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41121-107">EXAMPLES</span></span>

### <span data-ttu-id="41121-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41121-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="41121-109">Obter uma política WAF chamada $policyName no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41121-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="41121-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="41121-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="41121-111">Obter toda a política WAF no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41121-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="41121-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="41121-112">PARAMETERS</span></span>

### <span data-ttu-id="41121-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41121-113">-DefaultProfile</span></span>
<span data-ttu-id="41121-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41121-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41121-115">-Name</span><span class="sxs-lookup"><span data-stu-id="41121-115">-Name</span></span>
<span data-ttu-id="41121-116">Nome fireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="41121-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41121-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41121-117">-ResourceGroupName</span></span>
<span data-ttu-id="41121-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41121-118">The resource group name.</span></span>

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

### <span data-ttu-id="41121-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41121-119">CommonParameters</span></span>
<span data-ttu-id="41121-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41121-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41121-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41121-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41121-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41121-122">INPUTS</span></span>

### <span data-ttu-id="41121-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="41121-123">None</span></span>

## <span data-ttu-id="41121-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="41121-124">OUTPUTS</span></span>

### <span data-ttu-id="41121-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="41121-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="41121-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="41121-126">NOTES</span></span>

## <span data-ttu-id="41121-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41121-127">RELATED LINKS</span></span>

<span data-ttu-id="41121-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="41121-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
