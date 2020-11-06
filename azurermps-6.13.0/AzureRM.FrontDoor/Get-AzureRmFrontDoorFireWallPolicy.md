---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431953"
---
# <span data-ttu-id="2dee1-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="2dee1-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="2dee1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dee1-102">SYNOPSIS</span></span>
<span data-ttu-id="2dee1-103">Obter política de WAF</span><span class="sxs-lookup"><span data-stu-id="2dee1-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dee1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dee1-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dee1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2dee1-105">DESCRIPTION</span></span>
<span data-ttu-id="2dee1-106">A política **Get-AzureRmFrontDoorFireWallPolicy** CMDLETGET Obtém WAF em um grupo de recursos sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="2dee1-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="2dee1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dee1-107">EXAMPLES</span></span>

### <span data-ttu-id="2dee1-108">Exemplo 1: Obtenha uma política WAF chamada $Name em $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="2dee1-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="2dee1-109">Obter uma política do WAF chamada $Name $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="2dee1-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="2dee1-110">Exemplo 2: obter toda a política WAF no $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="2dee1-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="2dee1-111">Obter toda a política WAF no $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="2dee1-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="2dee1-112">OS</span><span class="sxs-lookup"><span data-stu-id="2dee1-112">PARAMETERS</span></span>

### <span data-ttu-id="2dee1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dee1-113">-DefaultProfile</span></span>
<span data-ttu-id="2dee1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2dee1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dee1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dee1-115">-Name</span></span>
<span data-ttu-id="2dee1-116">Nome do FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="2dee1-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="2dee1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dee1-117">-ResourceGroupName</span></span>
<span data-ttu-id="2dee1-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2dee1-118">The resource group name.</span></span>

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

### <span data-ttu-id="2dee1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dee1-119">CommonParameters</span></span>
<span data-ttu-id="2dee1-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dee1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dee1-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dee1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dee1-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2dee1-122">INPUTS</span></span>

### <span data-ttu-id="2dee1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2dee1-123">System.String</span></span>

## <span data-ttu-id="2dee1-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2dee1-124">OUTPUTS</span></span>

### <span data-ttu-id="2dee1-125">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="2dee1-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="2dee1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2dee1-126">NOTES</span></span>

## <span data-ttu-id="2dee1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dee1-127">RELATED LINKS</span></span>

<span data-ttu-id="2dee1-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="2dee1-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>
