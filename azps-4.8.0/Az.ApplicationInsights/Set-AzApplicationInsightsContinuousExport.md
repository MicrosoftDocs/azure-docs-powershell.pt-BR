---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: fef34358855666d0f407c72831b2973ce95cc7e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955165"
---
# <span data-ttu-id="5441d-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="5441d-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="5441d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5441d-102">SYNOPSIS</span></span>
<span data-ttu-id="5441d-103">Atualizar uma configuração de exportação contínua em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="5441d-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="5441d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5441d-104">SYNTAX</span></span>

### <span data-ttu-id="5441d-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5441d-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5441d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5441d-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5441d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5441d-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5441d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5441d-108">DESCRIPTION</span></span>
<span data-ttu-id="5441d-109">Atualizar uma configuração de exportação contínua em um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="5441d-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="5441d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5441d-110">EXAMPLES</span></span>

### <span data-ttu-id="5441d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5441d-111">Example 1</span></span>
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

<span data-ttu-id="5441d-112">Atualize a configuração de exportação contínua "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" do recurso "teste" no grupo de recursos "grupo de teste" para exportar documentos "solicitação" e "rastreamento" para o contêiner de armazenamento "testcontainer" em "teststorageaccount". O token SAS tem que ser válido e ter permissão de gravação para o contêiner; caso contrário, o recurso de exportação contínua não funcionará.</span><span class="sxs-lookup"><span data-stu-id="5441d-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="5441d-113">Se o token SAS venceu, o recurso de exportação contínua deixará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="5441d-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="5441d-114">OS</span><span class="sxs-lookup"><span data-stu-id="5441d-114">PARAMETERS</span></span>

### <span data-ttu-id="5441d-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5441d-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="5441d-116">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="5441d-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="5441d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5441d-117">-DefaultProfile</span></span>
<span data-ttu-id="5441d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5441d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5441d-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="5441d-119">-DisableConfiguration</span></span>
<span data-ttu-id="5441d-120">Desabilite a exportação contínua ou não.</span><span class="sxs-lookup"><span data-stu-id="5441d-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="5441d-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="5441d-121">-DocumentType</span></span>
<span data-ttu-id="5441d-122">Tipos de documento que precisam ser exportados.</span><span class="sxs-lookup"><span data-stu-id="5441d-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="5441d-123">-Exportid</span><span class="sxs-lookup"><span data-stu-id="5441d-123">-ExportId</span></span>
<span data-ttu-id="5441d-124">ID de exportação contínua do Application insights.</span><span class="sxs-lookup"><span data-stu-id="5441d-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="5441d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5441d-125">-Name</span></span>
<span data-ttu-id="5441d-126">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="5441d-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="5441d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5441d-127">-ResourceGroupName</span></span>
<span data-ttu-id="5441d-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5441d-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="5441d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5441d-129">-ResourceId</span></span>
<span data-ttu-id="5441d-130">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="5441d-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="5441d-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5441d-131">-StorageAccountId</span></span>
<span data-ttu-id="5441d-132">ID da conta de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="5441d-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="5441d-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="5441d-133">-StorageLocation</span></span>
<span data-ttu-id="5441d-134">ID do local de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="5441d-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="5441d-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="5441d-135">-StorageSASUri</span></span>
<span data-ttu-id="5441d-136">URI da SAS de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="5441d-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="5441d-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5441d-137">-Confirm</span></span>
<span data-ttu-id="5441d-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5441d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5441d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5441d-139">-WhatIf</span></span>
<span data-ttu-id="5441d-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5441d-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5441d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5441d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5441d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5441d-142">CommonParameters</span></span>
<span data-ttu-id="5441d-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5441d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5441d-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5441d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5441d-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5441d-145">INPUTS</span></span>

### <span data-ttu-id="5441d-146">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5441d-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="5441d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5441d-147">System.String</span></span>

## <span data-ttu-id="5441d-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5441d-148">OUTPUTS</span></span>

### <span data-ttu-id="5441d-149">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="5441d-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="5441d-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5441d-150">NOTES</span></span>

## <span data-ttu-id="5441d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5441d-151">RELATED LINKS</span></span>
