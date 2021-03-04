---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 63c31e07313f7e6ad3e1eea25977e85f3e4c6b53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887041"
---
# <span data-ttu-id="c6a91-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="c6a91-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="c6a91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6a91-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a91-103">Obter configuração de exportação contínua de insights de aplicativos para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c6a91-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="c6a91-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c6a91-104">SYNTAX</span></span>

### <span data-ttu-id="c6a91-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c6a91-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6a91-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6a91-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6a91-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6a91-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6a91-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c6a91-108">DESCRIPTION</span></span>
<span data-ttu-id="c6a91-109">Obter configuração de exportação contínua de insights de aplicativos para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c6a91-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="c6a91-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6a91-110">EXAMPLES</span></span>

### <span data-ttu-id="c6a91-111">Exemplo 1 Obter exportação contínua para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c6a91-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="c6a91-112">Obter configurações de exportação contínuas de insights do aplicativo para o recurso chamado "test" no grupo de recursos "testgroup"</span><span class="sxs-lookup"><span data-stu-id="c6a91-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="c6a91-113">Exemplo 2 Obter exportação contínua para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c6a91-113">Example 2 Get continuous export for an application insights resource</span></span>
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

<span data-ttu-id="c6a91-114">Obter informações do aplicativo configuração de exportação contínua com id de exportação "ZJrfffySPdtG3ESn3iRxVIEFuNY=" para o recurso chamado "test" no grupo de recursos "testgroup"</span><span class="sxs-lookup"><span data-stu-id="c6a91-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="c6a91-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c6a91-115">PARAMETERS</span></span>

### <span data-ttu-id="c6a91-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c6a91-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c6a91-117">Objeto Application Insights Component.</span><span class="sxs-lookup"><span data-stu-id="c6a91-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c6a91-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a91-118">-DefaultProfile</span></span>
<span data-ttu-id="c6a91-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c6a91-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6a91-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="c6a91-120">-ExportId</span></span>
<span data-ttu-id="c6a91-121">ID de Exportação Contínua do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c6a91-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="c6a91-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c6a91-122">-Name</span></span>
<span data-ttu-id="c6a91-123">Nome do componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c6a91-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c6a91-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a91-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6a91-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="c6a91-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6a91-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6a91-126">-ResourceId</span></span>
<span data-ttu-id="c6a91-127">ID do Recurso de Componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c6a91-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c6a91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a91-128">CommonParameters</span></span>
<span data-ttu-id="c6a91-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a91-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a91-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a91-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6a91-131">INPUTS</span></span>

### <span data-ttu-id="c6a91-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c6a91-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c6a91-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c6a91-133">System.String</span></span>

## <span data-ttu-id="c6a91-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c6a91-134">OUTPUTS</span></span>

### <span data-ttu-id="c6a91-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6a91-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="c6a91-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="c6a91-136">NOTES</span></span>

## <span data-ttu-id="c6a91-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6a91-137">RELATED LINKS</span></span>
