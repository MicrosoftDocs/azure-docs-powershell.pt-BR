---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110869"
---
# <span data-ttu-id="0b889-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0b889-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="0b889-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b889-102">SYNOPSIS</span></span>
<span data-ttu-id="0b889-103">Obtém propriedades de métricas para o serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b889-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="0b889-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b889-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b889-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b889-105">DESCRIPTION</span></span>
<span data-ttu-id="0b889-106">O cmdlet **Get-AzStorageServiceMetricsProperty** obtém propriedades de métricas para o serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b889-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="0b889-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b889-107">EXAMPLES</span></span>

### <span data-ttu-id="0b889-108">Exemplo 1: Obter propriedades de métricas para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="0b889-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="0b889-109">Esse comando obtém propriedades de métricas para armazenamento de blob para o tipo de métricas hora.</span><span class="sxs-lookup"><span data-stu-id="0b889-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="0b889-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b889-110">PARAMETERS</span></span>

### <span data-ttu-id="0b889-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0b889-111">-Context</span></span>
<span data-ttu-id="0b889-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b889-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0b889-113">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b889-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b889-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b889-114">-DefaultProfile</span></span>
<span data-ttu-id="0b889-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b889-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b889-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="0b889-116">-MetricsType</span></span>
<span data-ttu-id="0b889-117">Especifica um tipo de métrica.</span><span class="sxs-lookup"><span data-stu-id="0b889-117">Specifies a metrics type.</span></span>
<span data-ttu-id="0b889-118">Este cmdlet obtém as propriedades de métricas do serviço de Armazenamento do Azure para o tipo de métrica especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0b889-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="0b889-119">Os valores aceitáveis para este parâmetro são: Hora e Minuto.</span><span class="sxs-lookup"><span data-stu-id="0b889-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b889-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="0b889-120">-ServiceType</span></span>
<span data-ttu-id="0b889-121">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b889-121">Specifies the storage service type.</span></span>
<span data-ttu-id="0b889-122">Este cmdlet obtém as propriedades das métricas do tipo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0b889-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="0b889-123">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0b889-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b889-124">Blob</span><span class="sxs-lookup"><span data-stu-id="0b889-124">Blob</span></span> 
- <span data-ttu-id="0b889-125">Tabela</span><span class="sxs-lookup"><span data-stu-id="0b889-125">Table</span></span>
- <span data-ttu-id="0b889-126">Fila</span><span class="sxs-lookup"><span data-stu-id="0b889-126">Queue</span></span>
- <span data-ttu-id="0b889-127">Arquivo O valor do Arquivo não tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="0b889-127">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b889-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b889-128">CommonParameters</span></span>
<span data-ttu-id="0b889-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b889-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b889-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b889-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b889-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="0b889-131">INPUTS</span></span>

### <span data-ttu-id="0b889-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b889-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0b889-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="0b889-133">OUTPUTS</span></span>

### <span data-ttu-id="0b889-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="0b889-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="0b889-135">Notas</span><span class="sxs-lookup"><span data-stu-id="0b889-135">NOTES</span></span>

## <span data-ttu-id="0b889-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b889-136">RELATED LINKS</span></span>

[<span data-ttu-id="0b889-137">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b889-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0b889-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0b889-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


