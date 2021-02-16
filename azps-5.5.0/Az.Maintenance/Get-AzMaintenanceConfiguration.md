---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118443"
---
# <span data-ttu-id="33c8a-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="33c8a-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="33c8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="33c8a-103">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="33c8a-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="33c8a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33c8a-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33c8a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="33c8a-105">DESCRIPTION</span></span>
<span data-ttu-id="33c8a-106">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="33c8a-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="33c8a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="33c8a-107">EXAMPLES</span></span>

### <span data-ttu-id="33c8a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33c8a-108">Example 1</span></span>
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

<span data-ttu-id="33c8a-109">Obter registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="33c8a-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="33c8a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33c8a-110">PARAMETERS</span></span>

### <span data-ttu-id="33c8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c8a-111">-DefaultProfile</span></span>
<span data-ttu-id="33c8a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33c8a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33c8a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="33c8a-113">-Name</span></span>
<span data-ttu-id="33c8a-114">Nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="33c8a-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="33c8a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c8a-115">-ResourceGroupName</span></span>
<span data-ttu-id="33c8a-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="33c8a-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="33c8a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c8a-117">CommonParameters</span></span>
<span data-ttu-id="33c8a-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c8a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c8a-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33c8a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c8a-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="33c8a-120">INPUTS</span></span>

### <span data-ttu-id="33c8a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="33c8a-121">System.String</span></span>

## <span data-ttu-id="33c8a-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="33c8a-122">OUTPUTS</span></span>

### <span data-ttu-id="33c8a-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="33c8a-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="33c8a-124">Notas</span><span class="sxs-lookup"><span data-stu-id="33c8a-124">NOTES</span></span>

## <span data-ttu-id="33c8a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33c8a-125">RELATED LINKS</span></span>
