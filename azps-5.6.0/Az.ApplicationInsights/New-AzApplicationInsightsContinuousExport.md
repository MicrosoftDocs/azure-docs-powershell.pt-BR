---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 4c00bfec7ab026478c4b05b55ce27b812af37486
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886108"
---
# <span data-ttu-id="7050e-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7050e-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="7050e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7050e-102">SYNOPSIS</span></span>
<span data-ttu-id="7050e-103">Criar uma nova configuração de exportação contínua de insights de aplicativo para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7050e-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="7050e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7050e-104">SYNTAX</span></span>

### <span data-ttu-id="7050e-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7050e-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7050e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7050e-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7050e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7050e-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7050e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7050e-108">DESCRIPTION</span></span>
<span data-ttu-id="7050e-109">Criar uma nova configuração de exportação contínua de insights de aplicativo para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7050e-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="7050e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7050e-110">EXAMPLES</span></span>

### <span data-ttu-id="7050e-111">Exemplo 1 Criar uma nova configuração de exportação contínua para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7050e-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="7050e-112">Crie uma nova configuração de exportação contínua de insights de aplicativos para exportar tipos de documento "Request" e "Trace" para o armazenamento contêm "testcontainer" na conta de armazenamento "teststorageaccount" no grupo de recursos "testgroup".</span><span class="sxs-lookup"><span data-stu-id="7050e-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="7050e-113">O token SAS precisa ser válido e ter permissão de gravação para o contêiner, caso contrário, o recurso de exportação contínua não funcionará. Se o token SAS expirou, o recurso de exportação contínua para de funcionar.</span><span class="sxs-lookup"><span data-stu-id="7050e-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="7050e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7050e-114">PARAMETERS</span></span>

### <span data-ttu-id="7050e-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7050e-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7050e-116">Objeto Application Insights Component.</span><span class="sxs-lookup"><span data-stu-id="7050e-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="7050e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7050e-117">-DefaultProfile</span></span>
<span data-ttu-id="7050e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7050e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7050e-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="7050e-119">-DocumentType</span></span>
<span data-ttu-id="7050e-120">Tipos de documento que precisam ser exportados.</span><span class="sxs-lookup"><span data-stu-id="7050e-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7050e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7050e-121">-Name</span></span>
<span data-ttu-id="7050e-122">Nome do componente.</span><span class="sxs-lookup"><span data-stu-id="7050e-122">Component Name.</span></span>

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

### <span data-ttu-id="7050e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7050e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7050e-124">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="7050e-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="7050e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7050e-125">-ResourceId</span></span>
<span data-ttu-id="7050e-126">ID do Recurso de Componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7050e-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="7050e-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7050e-127">-StorageAccountId</span></span>
<span data-ttu-id="7050e-128">ID da Conta de Armazenamento de Destino.</span><span class="sxs-lookup"><span data-stu-id="7050e-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="7050e-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="7050e-129">-StorageLocation</span></span>
<span data-ttu-id="7050e-130">ID do Local de Armazenamento de Destino.</span><span class="sxs-lookup"><span data-stu-id="7050e-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="7050e-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="7050e-131">-StorageSASUri</span></span>
<span data-ttu-id="7050e-132">Uri do SAS de Armazenamento de Destino.</span><span class="sxs-lookup"><span data-stu-id="7050e-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="7050e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7050e-133">-Confirm</span></span>
<span data-ttu-id="7050e-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7050e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7050e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7050e-135">-WhatIf</span></span>
<span data-ttu-id="7050e-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7050e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7050e-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7050e-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7050e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7050e-138">CommonParameters</span></span>
<span data-ttu-id="7050e-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7050e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7050e-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7050e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7050e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7050e-141">INPUTS</span></span>

### <span data-ttu-id="7050e-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7050e-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="7050e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7050e-143">System.String</span></span>

## <span data-ttu-id="7050e-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7050e-144">OUTPUTS</span></span>

### <span data-ttu-id="7050e-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="7050e-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="7050e-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="7050e-146">NOTES</span></span>

## <span data-ttu-id="7050e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7050e-147">RELATED LINKS</span></span>
