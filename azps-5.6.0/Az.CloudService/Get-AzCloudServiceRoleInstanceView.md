---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: 3d3d8e5cd7855e03d5f02ddaee6b38c98aeacb0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892660"
---
# <span data-ttu-id="1e921-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="1e921-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="1e921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e921-102">SYNOPSIS</span></span>
<span data-ttu-id="1e921-103">Recupera informações sobre o estado de tempo de executar de uma instância de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="1e921-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="1e921-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1e921-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1e921-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1e921-105">DESCRIPTION</span></span>
<span data-ttu-id="1e921-106">Recupera informações sobre o estado de tempo de executar de uma instância de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="1e921-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="1e921-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e921-107">EXAMPLES</span></span>

### <span data-ttu-id="1e921-108">Exemplo 1: Obter detalhes de exibição de instância para instância de função de serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="1e921-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="1e921-109">Este cmdlet obtém a exibição de instância da instância de função chamada ContosoFrontEnd_IN_0 de serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="1e921-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="1e921-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1e921-110">PARAMETERS</span></span>

### <span data-ttu-id="1e921-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="1e921-111">-CloudServiceName</span></span>
<span data-ttu-id="1e921-112">.</span><span class="sxs-lookup"><span data-stu-id="1e921-112">.</span></span>

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

### <span data-ttu-id="1e921-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e921-113">-DefaultProfile</span></span>
<span data-ttu-id="1e921-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e921-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e921-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e921-115">-ResourceGroupName</span></span>
<span data-ttu-id="1e921-116">.</span><span class="sxs-lookup"><span data-stu-id="1e921-116">.</span></span>

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

### <span data-ttu-id="1e921-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="1e921-117">-RoleInstanceName</span></span>
<span data-ttu-id="1e921-118">Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="1e921-118">Name of the role instance.</span></span>

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

### <span data-ttu-id="1e921-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e921-119">-SubscriptionId</span></span>
<span data-ttu-id="1e921-120">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1e921-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1e921-121">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1e921-121">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e921-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e921-122">CommonParameters</span></span>
<span data-ttu-id="1e921-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e921-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e921-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e921-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e921-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e921-125">INPUTS</span></span>

## <span data-ttu-id="1e921-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1e921-126">OUTPUTS</span></span>

### <span data-ttu-id="1e921-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="1e921-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="1e921-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="1e921-128">NOTES</span></span>

<span data-ttu-id="1e921-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1e921-129">ALIASES</span></span>

## <span data-ttu-id="1e921-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e921-130">RELATED LINKS</span></span>

