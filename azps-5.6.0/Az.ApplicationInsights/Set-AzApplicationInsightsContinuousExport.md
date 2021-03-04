---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 144200f95ca7cff8b4fa541666912d62ba6bd0b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887238"
---
# <span data-ttu-id="0b066-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="0b066-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="0b066-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b066-102">SYNOPSIS</span></span>
<span data-ttu-id="0b066-103">Atualizar uma configuração de exportação contínua em um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="0b066-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="0b066-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0b066-104">SYNTAX</span></span>

### <span data-ttu-id="0b066-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b066-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b066-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b066-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b066-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b066-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b066-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b066-108">DESCRIPTION</span></span>
<span data-ttu-id="0b066-109">Atualizar uma configuração de exportação contínua em um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="0b066-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="0b066-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b066-110">EXAMPLES</span></span>

### <span data-ttu-id="0b066-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b066-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="0b066-112">Atualize a configuração de exportação contínua "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" do recurso "test" no grupo de recursos "testgroup" para exportar documentos "Request" e "Trace" para o contêiner de armazenamento "testcontainer" em "teststorageaccount". O token SAS precisa ser válido e ter permissão de gravação para o contêiner, caso contrário, o recurso de exportação contínua não funcionará.</span><span class="sxs-lookup"><span data-stu-id="0b066-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="0b066-113">Se o token SAS expirou, o recurso de exportação contínua para de funcionar.</span><span class="sxs-lookup"><span data-stu-id="0b066-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="0b066-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0b066-114">PARAMETERS</span></span>

### <span data-ttu-id="0b066-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0b066-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0b066-116">Objeto Application Insights Component.</span><span class="sxs-lookup"><span data-stu-id="0b066-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0b066-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b066-117">-DefaultProfile</span></span>
<span data-ttu-id="0b066-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0b066-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b066-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b066-119">-DisableConfiguration</span></span>
<span data-ttu-id="0b066-120">Desabilite a exportação contínua ou não.</span><span class="sxs-lookup"><span data-stu-id="0b066-120">Disable continuous export or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b066-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="0b066-121">-DocumentType</span></span>
<span data-ttu-id="0b066-122">Tipos de documento que precisam ser exportados.</span><span class="sxs-lookup"><span data-stu-id="0b066-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="0b066-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="0b066-123">-ExportId</span></span>
<span data-ttu-id="0b066-124">ID de Exportação Contínua do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0b066-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="0b066-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0b066-125">-Name</span></span>
<span data-ttu-id="0b066-126">Nome do componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0b066-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="0b066-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b066-127">-ResourceGroupName</span></span>
<span data-ttu-id="0b066-128">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="0b066-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="0b066-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b066-129">-ResourceId</span></span>
<span data-ttu-id="0b066-130">ID do Recurso de Componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0b066-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0b066-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0b066-131">-StorageAccountId</span></span>
<span data-ttu-id="0b066-132">ID da Conta de Armazenamento de Destino.</span><span class="sxs-lookup"><span data-stu-id="0b066-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="0b066-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="0b066-133">-StorageLocation</span></span>
<span data-ttu-id="0b066-134">ID do Local de Armazenamento de Destino.</span><span class="sxs-lookup"><span data-stu-id="0b066-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="0b066-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="0b066-135">-StorageSASUri</span></span>
<span data-ttu-id="0b066-136">Uri SAS de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="0b066-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="0b066-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b066-137">-Confirm</span></span>
<span data-ttu-id="0b066-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b066-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b066-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b066-139">-WhatIf</span></span>
<span data-ttu-id="0b066-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b066-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b066-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b066-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b066-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b066-142">CommonParameters</span></span>
<span data-ttu-id="0b066-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b066-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b066-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b066-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b066-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b066-145">INPUTS</span></span>

### <span data-ttu-id="0b066-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0b066-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0b066-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0b066-147">System.String</span></span>

## <span data-ttu-id="0b066-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0b066-148">OUTPUTS</span></span>

### <span data-ttu-id="0b066-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b066-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="0b066-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="0b066-150">NOTES</span></span>

## <span data-ttu-id="0b066-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b066-151">RELATED LINKS</span></span>
