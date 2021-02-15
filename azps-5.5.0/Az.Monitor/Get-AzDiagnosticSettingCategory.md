---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 29c65ef5f5ec3b2b54fb883da706ddc9a38e1d4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111761"
---
# <span data-ttu-id="2a578-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="2a578-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="2a578-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a578-102">SYNOPSIS</span></span>
<span data-ttu-id="2a578-103">Obter ou listar categoria de configuração de diagnóstico com suporte para o recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a578-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="2a578-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a578-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a578-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a578-105">DESCRIPTION</span></span>
<span data-ttu-id="2a578-106">Obter ou listar categoria de configuração de diagnóstico com suporte para o recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a578-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="2a578-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2a578-107">EXAMPLES</span></span>

### <span data-ttu-id="2a578-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a578-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSettingCategory -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="2a578-109">Receba categorias de configuração de diagnóstico com suporte para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2a578-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="2a578-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a578-110">PARAMETERS</span></span>

### <span data-ttu-id="2a578-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a578-111">-DefaultProfile</span></span>
<span data-ttu-id="2a578-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a578-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a578-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a578-113">-Name</span></span>
<span data-ttu-id="2a578-114">Nome da categoria de configuração de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="2a578-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="2a578-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2a578-115">-TargetResourceId</span></span>
<span data-ttu-id="2a578-116">ID do recurso de destino</span><span class="sxs-lookup"><span data-stu-id="2a578-116">Target resource Id</span></span>

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

### <span data-ttu-id="2a578-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a578-117">CommonParameters</span></span>
<span data-ttu-id="2a578-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a578-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a578-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a578-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a578-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="2a578-120">INPUTS</span></span>

### <span data-ttu-id="2a578-121">System.String</span><span class="sxs-lookup"><span data-stu-id="2a578-121">System.String</span></span>

## <span data-ttu-id="2a578-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="2a578-122">OUTPUTS</span></span>

### <span data-ttu-id="2a578-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="2a578-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="2a578-124">Notas</span><span class="sxs-lookup"><span data-stu-id="2a578-124">NOTES</span></span>

## <span data-ttu-id="2a578-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a578-125">RELATED LINKS</span></span>
