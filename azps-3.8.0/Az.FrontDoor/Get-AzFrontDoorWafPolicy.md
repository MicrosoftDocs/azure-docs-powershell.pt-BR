---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: daf4631041093b10a1bf712649de8b5c3ad3b6d9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404013"
---
# <span data-ttu-id="7f1fe-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="7f1fe-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="7f1fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1fe-103">Obter política WAF</span><span class="sxs-lookup"><span data-stu-id="7f1fe-103">Get WAF policy</span></span>

## <span data-ttu-id="7f1fe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f1fe-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f1fe-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f1fe-105">DESCRIPTION</span></span>
<span data-ttu-id="7f1fe-106">O **cmdlet Get-AzFrontDoorWafPolicy** Obtém a política WAF em um grupo de recursos sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="7f1fe-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="7f1fe-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f1fe-107">EXAMPLES</span></span>

### <span data-ttu-id="7f1fe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7f1fe-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="7f1fe-109">Obter uma política WAF chamada $policyName no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f1fe-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="7f1fe-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7f1fe-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="7f1fe-111">Obter todas as políticas WAF no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f1fe-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="7f1fe-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f1fe-112">PARAMETERS</span></span>

### <span data-ttu-id="7f1fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1fe-113">-DefaultProfile</span></span>
<span data-ttu-id="7f1fe-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f1fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f1fe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f1fe-115">-Name</span></span>
<span data-ttu-id="7f1fe-116">Nome FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="7f1fe-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="7f1fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f1fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f1fe-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f1fe-118">The resource group name.</span></span>

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

### <span data-ttu-id="7f1fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1fe-119">CommonParameters</span></span>
<span data-ttu-id="7f1fe-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f1fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1fe-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f1fe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1fe-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="7f1fe-122">INPUTS</span></span>

### <span data-ttu-id="7f1fe-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7f1fe-123">None</span></span>

## <span data-ttu-id="7f1fe-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="7f1fe-124">OUTPUTS</span></span>

### <span data-ttu-id="7f1fe-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="7f1fe-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="7f1fe-126">Notas</span><span class="sxs-lookup"><span data-stu-id="7f1fe-126">NOTES</span></span>

## <span data-ttu-id="7f1fe-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f1fe-127">RELATED LINKS</span></span>

<span data-ttu-id="7f1fe-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="7f1fe-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
