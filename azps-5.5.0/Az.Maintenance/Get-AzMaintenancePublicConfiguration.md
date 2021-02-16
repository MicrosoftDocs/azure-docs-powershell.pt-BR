---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118441"
---
# <span data-ttu-id="7b8d1-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b8d1-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="7b8d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b8d1-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8d1-103">Obter registro de Configuração de Manutenção Pública</span><span class="sxs-lookup"><span data-stu-id="7b8d1-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="7b8d1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b8d1-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b8d1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b8d1-105">DESCRIPTION</span></span>
<span data-ttu-id="7b8d1-106">Obter registro de Configuração de Manutenção Pública</span><span class="sxs-lookup"><span data-stu-id="7b8d1-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="7b8d1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7b8d1-107">EXAMPLES</span></span>

### <span data-ttu-id="7b8d1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b8d1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="7b8d1-109">Obter registro de configuração de Manutenção Pública</span><span class="sxs-lookup"><span data-stu-id="7b8d1-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="7b8d1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b8d1-110">PARAMETERS</span></span>

### <span data-ttu-id="7b8d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8d1-111">-DefaultProfile</span></span>
<span data-ttu-id="7b8d1-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b8d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8d1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b8d1-113">-Name</span></span>
<span data-ttu-id="7b8d1-114">Nome da configuração de manutenção pública.</span><span class="sxs-lookup"><span data-stu-id="7b8d1-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b8d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="7b8d1-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b8d1-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8d1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8d1-117">CommonParameters</span></span>
<span data-ttu-id="7b8d1-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b8d1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8d1-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b8d1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8d1-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="7b8d1-120">INPUTS</span></span>

### <span data-ttu-id="7b8d1-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7b8d1-121">System.String</span></span>

## <span data-ttu-id="7b8d1-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="7b8d1-122">OUTPUTS</span></span>

### <span data-ttu-id="7b8d1-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b8d1-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="7b8d1-124">Notas</span><span class="sxs-lookup"><span data-stu-id="7b8d1-124">NOTES</span></span>

## <span data-ttu-id="7b8d1-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b8d1-125">RELATED LINKS</span></span>
