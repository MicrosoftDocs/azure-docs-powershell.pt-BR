---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3f295d42075054d676852c42028dc2e9fd8b82b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440247"
---
# <span data-ttu-id="7039a-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7039a-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="7039a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7039a-102">SYNOPSIS</span></span>
<span data-ttu-id="7039a-103">Modifica as propriedades de métricas para o serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7039a-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7039a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7039a-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="7039a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7039a-105">DESCRIPTION</span></span>
<span data-ttu-id="7039a-106">O cmdlet **set-AzureStorageServiceMetricsProperty** modifica as propriedades de métricas do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7039a-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="7039a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7039a-107">EXAMPLES</span></span>

### <span data-ttu-id="7039a-108">Exemplo 1: modificar as propriedades de métricas do serviço blob</span><span class="sxs-lookup"><span data-stu-id="7039a-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="7039a-109">Esse comando modifica as métricas da versão 1,0 do armazenamento de BLOB para um nível de serviço.</span><span class="sxs-lookup"><span data-stu-id="7039a-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="7039a-110">As métricas do serviço de armazenamento do Azure mantêm as entradas por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="7039a-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="7039a-111">Como esse comando especifica o parâmetro *PassThru* , o comando exibe as propriedades Metrics modificadas.</span><span class="sxs-lookup"><span data-stu-id="7039a-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="7039a-112">OS</span><span class="sxs-lookup"><span data-stu-id="7039a-112">PARAMETERS</span></span>

### <span data-ttu-id="7039a-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7039a-113">-Context</span></span>
<span data-ttu-id="7039a-114">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7039a-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7039a-115">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7039a-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7039a-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="7039a-116">-MetricsLevel</span></span>
<span data-ttu-id="7039a-117">Especifica o nível de métrica que o armazenamento do Azure usa para o serviço.</span><span class="sxs-lookup"><span data-stu-id="7039a-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="7039a-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7039a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7039a-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7039a-119">None</span></span>
- <span data-ttu-id="7039a-120">Atender</span><span class="sxs-lookup"><span data-stu-id="7039a-120">Service</span></span>
- <span data-ttu-id="7039a-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="7039a-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7039a-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="7039a-122">-MetricsType</span></span>
<span data-ttu-id="7039a-123">Especifica um tipo de métrica.</span><span class="sxs-lookup"><span data-stu-id="7039a-123">Specifies a metrics type.</span></span>
<span data-ttu-id="7039a-124">Esta cmldet define o tipo de métrica do serviço de armazenamento do Azure para o valor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7039a-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="7039a-125">Os valores aceitáveis para esse parâmetro são: Hour e minute.</span><span class="sxs-lookup"><span data-stu-id="7039a-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7039a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7039a-126">-PassThru</span></span>
<span data-ttu-id="7039a-127">Indica que esses cmdlets retornam as propriedades de métricas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="7039a-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="7039a-128">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="7039a-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7039a-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="7039a-129">-RetentionDays</span></span>
<span data-ttu-id="7039a-130">Especifica o número de dias durante os quais o serviço de armazenamento do Azure mantém as informações de métricas.</span><span class="sxs-lookup"><span data-stu-id="7039a-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7039a-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="7039a-131">-ServiceType</span></span>
<span data-ttu-id="7039a-132">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7039a-132">Specifies the storage service type.</span></span>
<span data-ttu-id="7039a-133">Esse cmdlet modifica as propriedades de métricas do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7039a-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="7039a-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7039a-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7039a-135">Irregular</span><span class="sxs-lookup"><span data-stu-id="7039a-135">Blob</span></span> 
- <span data-ttu-id="7039a-136">TableName</span><span class="sxs-lookup"><span data-stu-id="7039a-136">Table</span></span>
- <span data-ttu-id="7039a-137">Coloca</span><span class="sxs-lookup"><span data-stu-id="7039a-137">Queue</span></span>
- <span data-ttu-id="7039a-138">Arquivos</span><span class="sxs-lookup"><span data-stu-id="7039a-138">File</span></span>

<span data-ttu-id="7039a-139">Não há suporte para o valor do arquivo no momento.</span><span class="sxs-lookup"><span data-stu-id="7039a-139">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7039a-140">-Versão</span><span class="sxs-lookup"><span data-stu-id="7039a-140">-Version</span></span>
<span data-ttu-id="7039a-141">Especifica a versão das métricas de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7039a-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="7039a-142">O valor padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="7039a-142">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7039a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7039a-143">CommonParameters</span></span>
<span data-ttu-id="7039a-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7039a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7039a-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7039a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7039a-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7039a-146">INPUTS</span></span>

### <span data-ttu-id="7039a-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7039a-147">IStorageContext</span></span>

<span data-ttu-id="7039a-148">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7039a-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="7039a-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7039a-149">OUTPUTS</span></span>

### <span data-ttu-id="7039a-150">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="7039a-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="7039a-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7039a-151">NOTES</span></span>

## <span data-ttu-id="7039a-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7039a-152">RELATED LINKS</span></span>

[<span data-ttu-id="7039a-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7039a-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="7039a-154">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7039a-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


