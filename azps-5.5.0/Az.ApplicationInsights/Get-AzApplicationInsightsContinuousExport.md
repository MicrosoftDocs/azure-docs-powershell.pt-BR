---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115541"
---
# <span data-ttu-id="38f6b-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="38f6b-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="38f6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="38f6b-103">Obter configuração contínua de exportação de insights de aplicativos para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="38f6b-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="38f6b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38f6b-104">SYNTAX</span></span>

### <span data-ttu-id="38f6b-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38f6b-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38f6b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38f6b-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38f6b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38f6b-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38f6b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="38f6b-108">DESCRIPTION</span></span>
<span data-ttu-id="38f6b-109">Obter configuração contínua de exportação de insights de aplicativos para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="38f6b-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="38f6b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38f6b-110">EXAMPLES</span></span>

### <span data-ttu-id="38f6b-111">Exemplo 1 Obter a exportação contínua para um recurso de informações de aplicativo</span><span class="sxs-lookup"><span data-stu-id="38f6b-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="38f6b-112">Obter configurações contínuas de exportação de insights de aplicativos para o recurso chamado "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="38f6b-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="38f6b-113">Exemplo 2 Obter exportação contínua para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="38f6b-113">Example 2 Get continuous export for an application insights resource</span></span>
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

<span data-ttu-id="38f6b-114">Obter configuração contínua de exportação do insights do aplicativo com a ID de exportação "ZJrfffySPdtG3ESn3iRxVIEFuNY=" para o recurso chamado "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="38f6b-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="38f6b-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38f6b-115">PARAMETERS</span></span>

### <span data-ttu-id="38f6b-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="38f6b-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="38f6b-117">Objeto componente Do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="38f6b-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="38f6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f6b-118">-DefaultProfile</span></span>
<span data-ttu-id="38f6b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="38f6b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38f6b-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="38f6b-120">-ExportId</span></span>
<span data-ttu-id="38f6b-121">ID de Exportação Contínua do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="38f6b-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="38f6b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="38f6b-122">-Name</span></span>
<span data-ttu-id="38f6b-123">Nome do componente Informações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="38f6b-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="38f6b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f6b-124">-ResourceGroupName</span></span>
<span data-ttu-id="38f6b-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38f6b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="38f6b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38f6b-126">-ResourceId</span></span>
<span data-ttu-id="38f6b-127">ID do Recurso de Componentes do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="38f6b-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="38f6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f6b-128">CommonParameters</span></span>
<span data-ttu-id="38f6b-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f6b-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f6b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f6b-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="38f6b-131">INPUTS</span></span>

### <span data-ttu-id="38f6b-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="38f6b-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="38f6b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="38f6b-133">System.String</span></span>

## <span data-ttu-id="38f6b-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="38f6b-134">OUTPUTS</span></span>

### <span data-ttu-id="38f6b-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="38f6b-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="38f6b-136">Notas</span><span class="sxs-lookup"><span data-stu-id="38f6b-136">NOTES</span></span>

## <span data-ttu-id="38f6b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38f6b-137">RELATED LINKS</span></span>
