---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: 6939cde26695cb4273d776437c3697c03d426db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889465"
---
# <span data-ttu-id="ddc3a-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc3a-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="ddc3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc3a-103">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="ddc3a-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="ddc3a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ddc3a-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddc3a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddc3a-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc3a-106">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="ddc3a-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="ddc3a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddc3a-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc3a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ddc3a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="ddc3a-109">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="ddc3a-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="ddc3a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ddc3a-110">PARAMETERS</span></span>

### <span data-ttu-id="ddc3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc3a-111">-DefaultProfile</span></span>
<span data-ttu-id="ddc3a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc3a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc3a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ddc3a-113">-Name</span></span>
<span data-ttu-id="ddc3a-114">Nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="ddc3a-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc3a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc3a-115">-ResourceGroupName</span></span>
<span data-ttu-id="ddc3a-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ddc3a-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc3a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc3a-117">CommonParameters</span></span>
<span data-ttu-id="ddc3a-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc3a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc3a-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddc3a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc3a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddc3a-120">INPUTS</span></span>

### <span data-ttu-id="ddc3a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ddc3a-121">System.String</span></span>

## <span data-ttu-id="ddc3a-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ddc3a-122">OUTPUTS</span></span>

### <span data-ttu-id="ddc3a-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddc3a-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="ddc3a-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="ddc3a-124">NOTES</span></span>

## <span data-ttu-id="ddc3a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddc3a-125">RELATED LINKS</span></span>
