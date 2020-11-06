---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 1e4dd5f65789751f9a28deb9e10c37221f45b97b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609533"
---
# <span data-ttu-id="cfb05-101">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="cfb05-101">New-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="cfb05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfb05-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb05-103">Criar uma nova configuração de exportação contínua do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="cfb05-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfb05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfb05-104">SYNTAX</span></span>

### <span data-ttu-id="cfb05-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cfb05-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfb05-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfb05-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfb05-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfb05-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfb05-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfb05-108">DESCRIPTION</span></span>
<span data-ttu-id="cfb05-109">Criar uma nova configuração de exportação contínua do Application insights para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="cfb05-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="cfb05-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfb05-110">EXAMPLES</span></span>

### <span data-ttu-id="cfb05-111">Exemplo 1 criar uma nova configuração de exportação contínua para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="cfb05-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="cfb05-112">Criar uma nova configuração de exportação contínua do Application insights para exportar tipos de documento "solicitação" e "rastreamento" para armazenamento contêm "testcontainer" na conta de armazenamento "teststorageaccount" no grupo de recursos "grupo de teste".</span><span class="sxs-lookup"><span data-stu-id="cfb05-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="cfb05-113">O token SAS deve ser válido e ter permissão de gravação para o contêiner, caso contrário, o recurso de exportação Continous não funcionará. Se o token SAS venceu, o recurso de exportação contínua deixará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="cfb05-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="cfb05-114">OS</span><span class="sxs-lookup"><span data-stu-id="cfb05-114">PARAMETERS</span></span>

### <span data-ttu-id="cfb05-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="cfb05-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="cfb05-116">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="cfb05-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="cfb05-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cfb05-117">-Confirm</span></span>
<span data-ttu-id="cfb05-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfb05-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfb05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb05-119">-DefaultProfile</span></span>
<span data-ttu-id="cfb05-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb05-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfb05-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="cfb05-121">-DocumentType</span></span>
<span data-ttu-id="cfb05-122">Tipos de documento que precisam ser exportados.</span><span class="sxs-lookup"><span data-stu-id="cfb05-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="cfb05-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfb05-123">-Name</span></span>
<span data-ttu-id="cfb05-124">Nome do componente.</span><span class="sxs-lookup"><span data-stu-id="cfb05-124">Component Name.</span></span>

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

### <span data-ttu-id="cfb05-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfb05-125">-ResourceGroupName</span></span>
<span data-ttu-id="cfb05-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cfb05-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="cfb05-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfb05-127">-ResourceId</span></span>
<span data-ttu-id="cfb05-128">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="cfb05-128">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="cfb05-129">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cfb05-129">-StorageAccountId</span></span>
<span data-ttu-id="cfb05-130">ID da conta de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="cfb05-130">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="cfb05-131">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="cfb05-131">-StorageLocation</span></span>
<span data-ttu-id="cfb05-132">ID do local de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="cfb05-132">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="cfb05-133">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="cfb05-133">-StorageSASUri</span></span>
<span data-ttu-id="cfb05-134">URI da SAS de armazenamento de destino.</span><span class="sxs-lookup"><span data-stu-id="cfb05-134">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="cfb05-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfb05-135">-WhatIf</span></span>
<span data-ttu-id="cfb05-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cfb05-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfb05-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cfb05-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfb05-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb05-138">CommonParameters</span></span>
<span data-ttu-id="cfb05-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfb05-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb05-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfb05-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb05-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfb05-141">INPUTS</span></span>

### <span data-ttu-id="cfb05-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cfb05-142">System.String</span></span>
<span data-ttu-id="cfb05-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="cfb05-143">System.String[]</span></span>

## <span data-ttu-id="cfb05-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfb05-144">OUTPUTS</span></span>

### <span data-ttu-id="cfb05-145">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfb05-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="cfb05-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfb05-146">NOTES</span></span>

## <span data-ttu-id="cfb05-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfb05-147">RELATED LINKS</span></span>

