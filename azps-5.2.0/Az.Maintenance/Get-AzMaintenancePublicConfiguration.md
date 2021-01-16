---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259521"
---
# <span data-ttu-id="5791f-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="5791f-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="5791f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5791f-102">SYNOPSIS</span></span>
<span data-ttu-id="5791f-103">Obter registro de configuração de manutenção pública</span><span class="sxs-lookup"><span data-stu-id="5791f-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="5791f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5791f-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5791f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5791f-105">DESCRIPTION</span></span>
<span data-ttu-id="5791f-106">Obter registro de configuração de manutenção pública</span><span class="sxs-lookup"><span data-stu-id="5791f-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="5791f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5791f-107">EXAMPLES</span></span>

### <span data-ttu-id="5791f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5791f-108">Example 1</span></span>
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

<span data-ttu-id="5791f-109">Obter registro de configuração de manutenção pública</span><span class="sxs-lookup"><span data-stu-id="5791f-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="5791f-110">OS</span><span class="sxs-lookup"><span data-stu-id="5791f-110">PARAMETERS</span></span>

### <span data-ttu-id="5791f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5791f-111">-DefaultProfile</span></span>
<span data-ttu-id="5791f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5791f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5791f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5791f-113">-Name</span></span>
<span data-ttu-id="5791f-114">O nome da configuração de manutenção pública.</span><span class="sxs-lookup"><span data-stu-id="5791f-114">The public maintenance configuration Name.</span></span>

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

### <span data-ttu-id="5791f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5791f-115">-ResourceGroupName</span></span>
<span data-ttu-id="5791f-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5791f-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="5791f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5791f-117">CommonParameters</span></span>
<span data-ttu-id="5791f-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5791f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5791f-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5791f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5791f-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5791f-120">INPUTS</span></span>

### <span data-ttu-id="5791f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5791f-121">System.String</span></span>

## <span data-ttu-id="5791f-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5791f-122">OUTPUTS</span></span>

### <span data-ttu-id="5791f-123">Microsoft. Azure. Commands. maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5791f-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="5791f-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5791f-124">NOTES</span></span>

## <span data-ttu-id="5791f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5791f-125">RELATED LINKS</span></span>
