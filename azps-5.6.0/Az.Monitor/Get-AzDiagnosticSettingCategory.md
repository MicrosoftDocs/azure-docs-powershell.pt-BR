---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: df263698a913faf361e5f23bb12d0267be314106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888893"
---
# <span data-ttu-id="ea3ae-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="ea3ae-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="ea3ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea3ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3ae-103">Obter ou listar categoria de configuração de diagnóstico com suporte para o recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea3ae-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="ea3ae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ea3ae-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea3ae-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ea3ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ea3ae-106">Obter ou listar categoria de configuração de diagnóstico com suporte para o recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea3ae-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="ea3ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea3ae-107">EXAMPLES</span></span>

### <span data-ttu-id="ea3ae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea3ae-108">Example 1</span></span>
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

<span data-ttu-id="ea3ae-109">Obter categorias de configuração de diagnóstico com suporte para rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ea3ae-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="ea3ae-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ea3ae-110">PARAMETERS</span></span>

### <span data-ttu-id="ea3ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3ae-111">-DefaultProfile</span></span>
<span data-ttu-id="ea3ae-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea3ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea3ae-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ea3ae-113">-Name</span></span>
<span data-ttu-id="ea3ae-114">Nome da categoria de configuração de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ea3ae-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="ea3ae-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ea3ae-115">-TargetResourceId</span></span>
<span data-ttu-id="ea3ae-116">ID do recurso de destino</span><span class="sxs-lookup"><span data-stu-id="ea3ae-116">Target resource Id</span></span>

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

### <span data-ttu-id="ea3ae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3ae-117">CommonParameters</span></span>
<span data-ttu-id="ea3ae-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea3ae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3ae-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea3ae-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3ae-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea3ae-120">INPUTS</span></span>

### <span data-ttu-id="ea3ae-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ea3ae-121">System.String</span></span>

## <span data-ttu-id="ea3ae-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ea3ae-122">OUTPUTS</span></span>

### <span data-ttu-id="ea3ae-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="ea3ae-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="ea3ae-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="ea3ae-124">NOTES</span></span>

## <span data-ttu-id="ea3ae-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea3ae-125">RELATED LINKS</span></span>
