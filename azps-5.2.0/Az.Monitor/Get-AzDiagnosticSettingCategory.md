---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 2d1c4b2f272516af31fba17db50d33991dd1db50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263718"
---
# <span data-ttu-id="9ba48-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="9ba48-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="9ba48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ba48-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba48-103">Obter ou listar a categoria de configuração de diagnóstico com suporte para o recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba48-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="9ba48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ba48-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ba48-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ba48-105">DESCRIPTION</span></span>
<span data-ttu-id="9ba48-106">Obter ou listar a categoria de configuração de diagnóstico com suporte para o recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba48-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="9ba48-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ba48-107">EXAMPLES</span></span>

### <span data-ttu-id="9ba48-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ba48-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSetting -TargetResourceId -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="9ba48-109">Obtenha categorias de configuração de diagnóstico com suporte para a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9ba48-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="9ba48-110">OS</span><span class="sxs-lookup"><span data-stu-id="9ba48-110">PARAMETERS</span></span>

### <span data-ttu-id="9ba48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba48-111">-DefaultProfile</span></span>
<span data-ttu-id="9ba48-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba48-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ba48-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ba48-113">-Name</span></span>
<span data-ttu-id="9ba48-114">Nome da categoria de configuração de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="9ba48-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="9ba48-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9ba48-115">-TargetResourceId</span></span>
<span data-ttu-id="9ba48-116">ID do recurso de destino</span><span class="sxs-lookup"><span data-stu-id="9ba48-116">Target resource Id</span></span>

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

### <span data-ttu-id="9ba48-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba48-117">CommonParameters</span></span>
<span data-ttu-id="9ba48-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ba48-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba48-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ba48-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba48-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ba48-120">INPUTS</span></span>

### <span data-ttu-id="9ba48-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9ba48-121">System.String</span></span>

## <span data-ttu-id="9ba48-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ba48-122">OUTPUTS</span></span>

### <span data-ttu-id="9ba48-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="9ba48-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="9ba48-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ba48-124">NOTES</span></span>

## <span data-ttu-id="9ba48-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ba48-125">RELATED LINKS</span></span>
