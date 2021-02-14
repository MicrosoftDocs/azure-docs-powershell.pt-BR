---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: fef34358855666d0f407c72831b2973ce95cc7e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117029"
---
# <span data-ttu-id="cec23-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="cec23-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="cec23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cec23-102">SYNOPSIS</span></span>
<span data-ttu-id="cec23-103">Atualizar uma configuração de exportação contínua em um recurso de informações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cec23-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="cec23-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cec23-104">SYNTAX</span></span>

### <span data-ttu-id="cec23-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cec23-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cec23-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cec23-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cec23-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cec23-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cec23-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cec23-108">DESCRIPTION</span></span>
<span data-ttu-id="cec23-109">Atualizar uma configuração de exportação contínua em um recurso de informações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cec23-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="cec23-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cec23-110">EXAMPLES</span></span>

### <span data-ttu-id="cec23-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cec23-111">Example 1</span></span>
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

<span data-ttu-id="cec23-112">Atualize a configuração contínua de exportação "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" de "teste" do recurso no grupo de recursos "grupo de teste" para exportar documentos "Solicitar" e "Rastrear" para o contêiner de armazenamento "testcontainer" em "teststorageaccount". O token SAS deve ser válido e ter permissão de gravação para o contêiner, caso contrário, o recurso de exportação contínua não funcionará.</span><span class="sxs-lookup"><span data-stu-id="cec23-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="cec23-113">Se o token SAS tiver expirado, o recurso de exportação contínua não funcionará mais.</span><span class="sxs-lookup"><span data-stu-id="cec23-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="cec23-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cec23-114">PARAMETERS</span></span>

### <span data-ttu-id="cec23-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="cec23-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="cec23-116">Objeto componente Do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cec23-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="cec23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec23-117">-DefaultProfile</span></span>
<span data-ttu-id="cec23-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cec23-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cec23-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="cec23-119">-DisableConfiguration</span></span>
<span data-ttu-id="cec23-120">Desabilitar a exportação contínua ou não.</span><span class="sxs-lookup"><span data-stu-id="cec23-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="cec23-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="cec23-121">-DocumentType</span></span>
<span data-ttu-id="cec23-122">Tipos de documentos que precisam ser exportados.</span><span class="sxs-lookup"><span data-stu-id="cec23-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="cec23-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="cec23-123">-ExportId</span></span>
<span data-ttu-id="cec23-124">ID de Exportação Contínua do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cec23-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="cec23-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cec23-125">-Name</span></span>
<span data-ttu-id="cec23-126">Nome do componente Informações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cec23-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="cec23-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cec23-127">-ResourceGroupName</span></span>
<span data-ttu-id="cec23-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cec23-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="cec23-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cec23-129">-ResourceId</span></span>
<span data-ttu-id="cec23-130">ID do Recurso de Componentes do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cec23-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="cec23-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cec23-131">-StorageAccountId</span></span>
<span data-ttu-id="cec23-132">ID da Conta de Armazenamento de Destino.</span><span class="sxs-lookup"><span data-stu-id="cec23-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="cec23-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="cec23-133">-StorageLocation</span></span>
<span data-ttu-id="cec23-134">ID do Local de Armazenamento de Destino.</span><span class="sxs-lookup"><span data-stu-id="cec23-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="cec23-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="cec23-135">-StorageSASUri</span></span>
<span data-ttu-id="cec23-136">uri SAS de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="cec23-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="cec23-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cec23-137">-Confirm</span></span>
<span data-ttu-id="cec23-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cec23-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cec23-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cec23-139">-WhatIf</span></span>
<span data-ttu-id="cec23-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cec23-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cec23-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cec23-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cec23-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec23-142">CommonParameters</span></span>
<span data-ttu-id="cec23-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cec23-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec23-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cec23-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec23-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="cec23-145">INPUTS</span></span>

### <span data-ttu-id="cec23-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="cec23-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="cec23-147">System.String</span><span class="sxs-lookup"><span data-stu-id="cec23-147">System.String</span></span>

## <span data-ttu-id="cec23-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="cec23-148">OUTPUTS</span></span>

### <span data-ttu-id="cec23-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="cec23-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="cec23-150">Notas</span><span class="sxs-lookup"><span data-stu-id="cec23-150">NOTES</span></span>

## <span data-ttu-id="cec23-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cec23-151">RELATED LINKS</span></span>
