---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: e8fe8fb59ee56e457c49d959c07db08cad62bb5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770875"
---
# <span data-ttu-id="d24e6-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="d24e6-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="d24e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d24e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d24e6-103">Obter política de WAF</span><span class="sxs-lookup"><span data-stu-id="d24e6-103">Get WAF policy</span></span>

## <span data-ttu-id="d24e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d24e6-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d24e6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d24e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d24e6-106">A política **Get-AzFrontDoorFireWallPolicy** CMDLETGET Obtém WAF em um grupo de recursos sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="d24e6-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="d24e6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d24e6-107">EXAMPLES</span></span>

### <span data-ttu-id="d24e6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d24e6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="d24e6-109">Obter uma política do WAF chamada $policyName $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24e6-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="d24e6-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d24e6-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="d24e6-111">Obter toda a política WAF no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24e6-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="d24e6-112">OS</span><span class="sxs-lookup"><span data-stu-id="d24e6-112">PARAMETERS</span></span>

### <span data-ttu-id="d24e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24e6-113">-DefaultProfile</span></span>
<span data-ttu-id="d24e6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d24e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d24e6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d24e6-115">-Name</span></span>
<span data-ttu-id="d24e6-116">Nome do FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="d24e6-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="d24e6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24e6-117">-ResourceGroupName</span></span>
<span data-ttu-id="d24e6-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d24e6-118">The resource group name.</span></span>

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

### <span data-ttu-id="d24e6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24e6-119">CommonParameters</span></span>
<span data-ttu-id="d24e6-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24e6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24e6-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d24e6-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24e6-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d24e6-122">INPUTS</span></span>

### <span data-ttu-id="d24e6-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d24e6-123">None</span></span>

## <span data-ttu-id="d24e6-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d24e6-124">OUTPUTS</span></span>

### <span data-ttu-id="d24e6-125">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d24e6-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="d24e6-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d24e6-126">NOTES</span></span>

## <span data-ttu-id="d24e6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d24e6-127">RELATED LINKS</span></span>

<span data-ttu-id="d24e6-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="d24e6-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span></span>
