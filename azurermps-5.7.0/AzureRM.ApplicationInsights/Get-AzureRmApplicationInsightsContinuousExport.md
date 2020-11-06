---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 5e3b2feff3b59df30960856718911a3aeb699c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431747"
---
# <span data-ttu-id="85b6d-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="85b6d-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="85b6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="85b6d-103">Obter configuração de exportação contínua do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="85b6d-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85b6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85b6d-104">SYNTAX</span></span>

### <span data-ttu-id="85b6d-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="85b6d-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85b6d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85b6d-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85b6d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85b6d-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85b6d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85b6d-108">DESCRIPTION</span></span>
<span data-ttu-id="85b6d-109">Obter configuração de exportação contínua do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="85b6d-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="85b6d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85b6d-110">EXAMPLES</span></span>

### <span data-ttu-id="85b6d-111">Exemplo 1 obter uma exportação contínua para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="85b6d-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="85b6d-112">Obter configurações de exportação contínua do Application insights para o recurso chamado "Test" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="85b6d-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="85b6d-113">Exemplo 2 obter uma exportação contínua para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="85b6d-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="85b6d-114">Obter configuração de exportação contínua do Application insights com a ID de exportação "ZJrfffySPdtG3ESn3iRxVIEFuNY =" para o recurso chamado "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="85b6d-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="85b6d-115">OS</span><span class="sxs-lookup"><span data-stu-id="85b6d-115">PARAMETERS</span></span>

### <span data-ttu-id="85b6d-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="85b6d-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="85b6d-117">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="85b6d-117">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85b6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b6d-118">-DefaultProfile</span></span>
<span data-ttu-id="85b6d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85b6d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b6d-120">-Exportid</span><span class="sxs-lookup"><span data-stu-id="85b6d-120">-ExportId</span></span>
<span data-ttu-id="85b6d-121">ID de exportação contínua do Application insights.</span><span class="sxs-lookup"><span data-stu-id="85b6d-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b6d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="85b6d-122">-Name</span></span>
<span data-ttu-id="85b6d-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="85b6d-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85b6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="85b6d-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85b6d-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b6d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85b6d-126">-ResourceId</span></span>
<span data-ttu-id="85b6d-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="85b6d-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b6d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b6d-128">CommonParameters</span></span>
<span data-ttu-id="85b6d-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85b6d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b6d-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b6d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b6d-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85b6d-131">INPUTS</span></span>

### <span data-ttu-id="85b6d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="85b6d-132">System.String</span></span>

## <span data-ttu-id="85b6d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85b6d-133">OUTPUTS</span></span>

### <span data-ttu-id="85b6d-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="85b6d-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="85b6d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85b6d-135">NOTES</span></span>

## <span data-ttu-id="85b6d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85b6d-136">RELATED LINKS</span></span>

