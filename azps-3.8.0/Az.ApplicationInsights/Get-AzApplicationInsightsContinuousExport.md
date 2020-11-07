---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944148"
---
# <span data-ttu-id="2f087-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="2f087-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="2f087-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f087-102">SYNOPSIS</span></span>
<span data-ttu-id="2f087-103">Obter configuração de exportação contínua do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="2f087-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="2f087-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f087-104">SYNTAX</span></span>

### <span data-ttu-id="2f087-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f087-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f087-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f087-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f087-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f087-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f087-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f087-108">DESCRIPTION</span></span>
<span data-ttu-id="2f087-109">Obter configuração de exportação contínua do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="2f087-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="2f087-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f087-110">EXAMPLES</span></span>

### <span data-ttu-id="2f087-111">Exemplo 1 obter uma exportação contínua para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="2f087-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="2f087-112">Obter configurações de exportação contínua do Application insights para o recurso chamado "Test" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="2f087-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="2f087-113">Exemplo 2 obter uma exportação contínua para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="2f087-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="2f087-114">Obter configuração de exportação contínua do Application insights com a ID de exportação "ZJrfffySPdtG3ESn3iRxVIEFuNY =" para o recurso chamado "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="2f087-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="2f087-115">OS</span><span class="sxs-lookup"><span data-stu-id="2f087-115">PARAMETERS</span></span>

### <span data-ttu-id="2f087-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2f087-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="2f087-117">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="2f087-117">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f087-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f087-118">-DefaultProfile</span></span>
<span data-ttu-id="2f087-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f087-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f087-120">-Exportid</span><span class="sxs-lookup"><span data-stu-id="2f087-120">-ExportId</span></span>
<span data-ttu-id="2f087-121">ID de exportação contínua do Application insights.</span><span class="sxs-lookup"><span data-stu-id="2f087-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f087-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f087-122">-Name</span></span>
<span data-ttu-id="2f087-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="2f087-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f087-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f087-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f087-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f087-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f087-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f087-126">-ResourceId</span></span>
<span data-ttu-id="2f087-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="2f087-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f087-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f087-128">CommonParameters</span></span>
<span data-ttu-id="2f087-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f087-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f087-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f087-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f087-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f087-131">INPUTS</span></span>

### <span data-ttu-id="2f087-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2f087-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="2f087-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2f087-133">System.String</span></span>

## <span data-ttu-id="2f087-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f087-134">OUTPUTS</span></span>

### <span data-ttu-id="2f087-135">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f087-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="2f087-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f087-136">NOTES</span></span>

## <span data-ttu-id="2f087-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f087-137">RELATED LINKS</span></span>
