---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944224"
---
# <span data-ttu-id="0edb9-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0edb9-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="0edb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0edb9-102">SYNOPSIS</span></span>
<span data-ttu-id="0edb9-103">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="0edb9-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="0edb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0edb9-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0edb9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0edb9-105">DESCRIPTION</span></span>
<span data-ttu-id="0edb9-106">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="0edb9-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="0edb9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0edb9-107">EXAMPLES</span></span>

### <span data-ttu-id="0edb9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0edb9-108">Example 1</span></span>
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

<span data-ttu-id="0edb9-109">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="0edb9-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="0edb9-110">OS</span><span class="sxs-lookup"><span data-stu-id="0edb9-110">PARAMETERS</span></span>

### <span data-ttu-id="0edb9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0edb9-111">-DefaultProfile</span></span>
<span data-ttu-id="0edb9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0edb9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0edb9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0edb9-113">-Name</span></span>
<span data-ttu-id="0edb9-114">O nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="0edb9-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="0edb9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0edb9-115">-ResourceGroupName</span></span>
<span data-ttu-id="0edb9-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0edb9-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="0edb9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0edb9-117">CommonParameters</span></span>
<span data-ttu-id="0edb9-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0edb9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0edb9-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0edb9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0edb9-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0edb9-120">INPUTS</span></span>

### <span data-ttu-id="0edb9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0edb9-121">System.String</span></span>

## <span data-ttu-id="0edb9-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0edb9-122">OUTPUTS</span></span>

### <span data-ttu-id="0edb9-123">Microsoft. Azure. Commands. maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0edb9-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="0edb9-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0edb9-124">NOTES</span></span>

## <span data-ttu-id="0edb9-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0edb9-125">RELATED LINKS</span></span>
