---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126959"
---
# <span data-ttu-id="722c1-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="722c1-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="722c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="722c1-102">SYNOPSIS</span></span>
<span data-ttu-id="722c1-103">Obter política WAF</span><span class="sxs-lookup"><span data-stu-id="722c1-103">Get WAF policy</span></span>

## <span data-ttu-id="722c1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="722c1-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="722c1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="722c1-105">DESCRIPTION</span></span>
<span data-ttu-id="722c1-106">O **cmdlet Get-AzFrontDoorWafPolicy** obtém a política WAF em um grupo de recursos sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="722c1-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="722c1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="722c1-107">EXAMPLES</span></span>

### <span data-ttu-id="722c1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="722c1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="722c1-109">Obter uma política WAF chamada $policyName no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="722c1-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="722c1-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="722c1-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="722c1-111">Obter todas as políticas WAF no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="722c1-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="722c1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="722c1-112">PARAMETERS</span></span>

### <span data-ttu-id="722c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722c1-113">-DefaultProfile</span></span>
<span data-ttu-id="722c1-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="722c1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="722c1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="722c1-115">-Name</span></span>
<span data-ttu-id="722c1-116">Nome FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="722c1-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="722c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="722c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="722c1-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="722c1-118">The resource group name.</span></span>

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

### <span data-ttu-id="722c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722c1-119">CommonParameters</span></span>
<span data-ttu-id="722c1-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="722c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722c1-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="722c1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722c1-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="722c1-122">INPUTS</span></span>

### <span data-ttu-id="722c1-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="722c1-123">None</span></span>

## <span data-ttu-id="722c1-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="722c1-124">OUTPUTS</span></span>

### <span data-ttu-id="722c1-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="722c1-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="722c1-126">Notas</span><span class="sxs-lookup"><span data-stu-id="722c1-126">NOTES</span></span>

## <span data-ttu-id="722c1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="722c1-127">RELATED LINKS</span></span>

<span data-ttu-id="722c1-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="722c1-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
