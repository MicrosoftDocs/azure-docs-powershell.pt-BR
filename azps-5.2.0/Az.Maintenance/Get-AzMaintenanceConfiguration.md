---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258460"
---
# <span data-ttu-id="70e08-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="70e08-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="70e08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70e08-102">SYNOPSIS</span></span>
<span data-ttu-id="70e08-103">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="70e08-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="70e08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70e08-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70e08-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70e08-105">DESCRIPTION</span></span>
<span data-ttu-id="70e08-106">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="70e08-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="70e08-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70e08-107">EXAMPLES</span></span>

### <span data-ttu-id="70e08-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70e08-108">Example 1</span></span>
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

<span data-ttu-id="70e08-109">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="70e08-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="70e08-110">OS</span><span class="sxs-lookup"><span data-stu-id="70e08-110">PARAMETERS</span></span>

### <span data-ttu-id="70e08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e08-111">-DefaultProfile</span></span>
<span data-ttu-id="70e08-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70e08-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70e08-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="70e08-113">-Name</span></span>
<span data-ttu-id="70e08-114">O nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="70e08-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="70e08-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e08-115">-ResourceGroupName</span></span>
<span data-ttu-id="70e08-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70e08-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="70e08-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e08-117">CommonParameters</span></span>
<span data-ttu-id="70e08-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e08-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e08-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70e08-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e08-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70e08-120">INPUTS</span></span>

### <span data-ttu-id="70e08-121">System. String</span><span class="sxs-lookup"><span data-stu-id="70e08-121">System.String</span></span>

## <span data-ttu-id="70e08-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70e08-122">OUTPUTS</span></span>

### <span data-ttu-id="70e08-123">Microsoft. Azure. Commands. maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="70e08-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="70e08-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70e08-124">NOTES</span></span>

## <span data-ttu-id="70e08-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70e08-125">RELATED LINKS</span></span>
