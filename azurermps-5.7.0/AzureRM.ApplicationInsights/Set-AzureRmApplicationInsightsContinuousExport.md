---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 7b426f7f6b494c92d86a41217000b2d2335c7d91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439902"
---
# <span data-ttu-id="30385-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="30385-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="30385-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30385-102">SYNOPSIS</span></span>
<span data-ttu-id="30385-103">Atualizar uma configuração de exportação contínua em um recurso do applciation insights</span><span class="sxs-lookup"><span data-stu-id="30385-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30385-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30385-104">SYNTAX</span></span>

### <span data-ttu-id="30385-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="30385-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30385-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30385-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30385-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30385-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30385-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30385-108">DESCRIPTION</span></span>
<span data-ttu-id="30385-109">Atualizar uma configuração de exportação contínua em um recurso do applciation insights</span><span class="sxs-lookup"><span data-stu-id="30385-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="30385-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30385-110">EXAMPLES</span></span>

### <span data-ttu-id="30385-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="30385-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -DestinationStorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -DestinationStorageLocationId sourcecentralus
 -DestinationStorageSASUri $sasuri

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

<span data-ttu-id="30385-112">Atualize a configuração de exportação contínua "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" do recurso "teste" no grupo de recursos "grupo de teste" para exportar documentos "solicitação" e "rastreamento" para o contêiner de armazenamento "testcontainer" em "teststorageaccount". O token SAS deve ser válido e ter permissão de gravação para o contêiner, caso contrário, o recurso de exportação Continous não funcionará.</span><span class="sxs-lookup"><span data-stu-id="30385-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="30385-113">Se o token SAS venceu, o recurso de exportação contínua deixará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="30385-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="30385-114">OS</span><span class="sxs-lookup"><span data-stu-id="30385-114">PARAMETERS</span></span>

### <span data-ttu-id="30385-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="30385-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="30385-116">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="30385-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="30385-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="30385-117">-Confirm</span></span>
<span data-ttu-id="30385-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30385-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30385-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30385-119">-DefaultProfile</span></span>
<span data-ttu-id="30385-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30385-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30385-121">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="30385-121">-DisableConfiguration</span></span>
<span data-ttu-id="30385-122">Desabilite a exportação contínua ou não.</span><span class="sxs-lookup"><span data-stu-id="30385-122">Disable continuous export or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30385-123">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="30385-123">-DocumentType</span></span>
<span data-ttu-id="30385-124">Tipos de documento que precisam ser exportados.</span><span class="sxs-lookup"><span data-stu-id="30385-124">Document types that need exported.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30385-125">-Exportid</span><span class="sxs-lookup"><span data-stu-id="30385-125">-ExportId</span></span>
<span data-ttu-id="30385-126">ID de exportação contínua do Application insights.</span><span class="sxs-lookup"><span data-stu-id="30385-126">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30385-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="30385-127">-Name</span></span>
<span data-ttu-id="30385-128">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="30385-128">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="30385-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30385-129">-ResourceGroupName</span></span>
<span data-ttu-id="30385-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="30385-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="30385-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30385-131">-ResourceId</span></span>
<span data-ttu-id="30385-132">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="30385-132">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="30385-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="30385-133">-StorageAccountId</span></span>
<span data-ttu-id="30385-134">ID da conta de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="30385-134">Destination Storage Account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30385-135">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="30385-135">-StorageLocation</span></span>
<span data-ttu-id="30385-136">ID do local de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="30385-136">Destination Storage Location Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30385-137">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="30385-137">-StorageSASUri</span></span>
<span data-ttu-id="30385-138">URI da SAS de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="30385-138">Destination Storage SAS uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30385-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30385-139">-WhatIf</span></span>
<span data-ttu-id="30385-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="30385-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30385-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="30385-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30385-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30385-142">CommonParameters</span></span>
<span data-ttu-id="30385-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30385-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30385-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30385-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30385-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30385-145">INPUTS</span></span>

### <span data-ttu-id="30385-146">System. String</span><span class="sxs-lookup"><span data-stu-id="30385-146">System.String</span></span>
<span data-ttu-id="30385-147">System. String [] System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30385-147">System.String[] System.Boolean</span></span>

## <span data-ttu-id="30385-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30385-148">OUTPUTS</span></span>

### <span data-ttu-id="30385-149">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="30385-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="30385-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30385-150">NOTES</span></span>

## <span data-ttu-id="30385-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30385-151">RELATED LINKS</span></span>

