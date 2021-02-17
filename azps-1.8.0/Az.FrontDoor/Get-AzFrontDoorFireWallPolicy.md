---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 5933d860ca2badce2d9576409dd1553153bb1e84
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401497"
---
# <span data-ttu-id="ef6ab-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="ef6ab-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="ef6ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6ab-103">Obter política WAF</span><span class="sxs-lookup"><span data-stu-id="ef6ab-103">Get WAF policy</span></span>

## <span data-ttu-id="ef6ab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef6ab-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef6ab-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef6ab-105">DESCRIPTION</span></span>
<span data-ttu-id="ef6ab-106">O **cmdlet Get-AzFrontDoorFireWallPolicy** obtém a política WAF em um grupo de recursos sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="ef6ab-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="ef6ab-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ef6ab-107">EXAMPLES</span></span>

### <span data-ttu-id="ef6ab-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef6ab-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="ef6ab-109">Obter uma política WAF chamada $policyName no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6ab-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="ef6ab-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ef6ab-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="ef6ab-111">Obter todas as políticas WAF no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6ab-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="ef6ab-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef6ab-112">PARAMETERS</span></span>

### <span data-ttu-id="ef6ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6ab-113">-DefaultProfile</span></span>
<span data-ttu-id="ef6ab-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef6ab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef6ab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef6ab-115">-Name</span></span>
<span data-ttu-id="ef6ab-116">Nome FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="ef6ab-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="ef6ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef6ab-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ef6ab-118">The resource group name.</span></span>

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

### <span data-ttu-id="ef6ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6ab-119">CommonParameters</span></span>
<span data-ttu-id="ef6ab-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef6ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6ab-121">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef6ab-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6ab-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="ef6ab-122">INPUTS</span></span>

### <span data-ttu-id="ef6ab-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ef6ab-123">None</span></span>

## <span data-ttu-id="ef6ab-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="ef6ab-124">OUTPUTS</span></span>

### <span data-ttu-id="ef6ab-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ef6ab-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="ef6ab-126">Notas</span><span class="sxs-lookup"><span data-stu-id="ef6ab-126">NOTES</span></span>

## <span data-ttu-id="ef6ab-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef6ab-127">RELATED LINKS</span></span>

<span data-ttu-id="ef6ab-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="ef6ab-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
