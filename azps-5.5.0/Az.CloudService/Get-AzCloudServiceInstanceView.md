---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: 4ad5b8a7b4369a5a0dd2b5ccc883ddc561a40af5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116905"
---
# <span data-ttu-id="6fa8a-101">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="6fa8a-101">Get-AzCloudServiceInstanceView</span></span>

## <span data-ttu-id="6fa8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fa8a-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa8a-103">Obtém o status de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-103">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="6fa8a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fa8a-104">SYNTAX</span></span>

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6fa8a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fa8a-105">DESCRIPTION</span></span>
<span data-ttu-id="6fa8a-106">Obtém o status de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-106">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="6fa8a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6fa8a-107">EXAMPLES</span></span>

### <span data-ttu-id="6fa8a-108">Exemplo 1: Obter o exibição de instância do serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="6fa8a-108">Example 1: Get cloud service instance view</span></span>
```powershell
PS C:\>$cloudServiceInstanceView = Get-AzCloudServiceInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

PS C:\>$cloudServiceInstanceView
RoleInstanceStatusesSummary                                   Statuses
---------------------------                                   --------
{{ProvisioningState/succeeded : 4}, {PowerState/started : 4}} {Provisioning succeeded, Started, Current Upgrade Domain of cloud service is -1., Max Upgrade Domain of cloud service is 1.}

PS C:\>$cloudServiceInstanceView.ToJsonString()
{
  "roleInstance": {
    "statusesSummary": [
      {
        "code": "ProvisioningState/succeeded",
        "count": 4
      },
      {
        "code": "PowerState/started",
        "count": 4
      }
    ]
  },
  "statuses": [
    {
      "code": "ProvisioningState/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "PowerState/started",
      "displayStatus": "Started",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "CurrentUpgradeDomain/-1",
      "displayStatus": "Current Upgrade Domain of cloud service is -1.",
      "level": "Info"
    },
    {
      "code": "MaxUpgradeDomain/1",
      "displayStatus": "Max Upgrade Domain of cloud service is 1.",
      "level": "Info"
    }
  ]
}
```

<span data-ttu-id="6fa8a-109">Este cmdlet obtém a exibição de instância do serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-109">This cmdlet gets the instance view of the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="6fa8a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fa8a-110">PARAMETERS</span></span>

### <span data-ttu-id="6fa8a-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="6fa8a-111">-CloudServiceName</span></span>
<span data-ttu-id="6fa8a-112">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-112">Name of the cloud service.</span></span>

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

### <span data-ttu-id="6fa8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa8a-113">-DefaultProfile</span></span>
<span data-ttu-id="6fa8a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fa8a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fa8a-115">-ResourceGroupName</span></span>
<span data-ttu-id="6fa8a-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-116">Name of the resource group.</span></span>

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

### <span data-ttu-id="6fa8a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6fa8a-117">-SubscriptionId</span></span>
<span data-ttu-id="6fa8a-118">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-118">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6fa8a-119">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6fa8a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa8a-120">CommonParameters</span></span>
<span data-ttu-id="6fa8a-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fa8a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa8a-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fa8a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa8a-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="6fa8a-123">INPUTS</span></span>

## <span data-ttu-id="6fa8a-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="6fa8a-124">OUTPUTS</span></span>

### <span data-ttu-id="6fa8a-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="6fa8a-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span></span>

## <span data-ttu-id="6fa8a-126">Notas</span><span class="sxs-lookup"><span data-stu-id="6fa8a-126">NOTES</span></span>

<span data-ttu-id="6fa8a-127">Aliases</span><span class="sxs-lookup"><span data-stu-id="6fa8a-127">ALIASES</span></span>

## <span data-ttu-id="6fa8a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fa8a-128">RELATED LINKS</span></span>

