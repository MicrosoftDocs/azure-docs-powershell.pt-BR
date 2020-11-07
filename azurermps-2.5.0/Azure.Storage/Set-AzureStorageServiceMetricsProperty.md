---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
ms.openlocfilehash: 45192b6b24719bb793e3f443cf2a8cb42abd78ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786591"
---
# <span data-ttu-id="c50e7-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c50e7-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="c50e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c50e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c50e7-103">Modifica as propriedades de métricas para o serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c50e7-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c50e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c50e7-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c50e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c50e7-105">DESCRIPTION</span></span>
<span data-ttu-id="c50e7-106">O cmdlet **set-AzureStorageServiceMetricsProperty** modifica as propriedades de métricas do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c50e7-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c50e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c50e7-107">EXAMPLES</span></span>

### <span data-ttu-id="c50e7-108">Exemplo 1: modificar as propriedades de métricas do serviço blob</span><span class="sxs-lookup"><span data-stu-id="c50e7-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="c50e7-109">Esse comando modifica as métricas da versão 1,0 do armazenamento de BLOB para um nível de serviço.</span><span class="sxs-lookup"><span data-stu-id="c50e7-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="c50e7-110">As métricas do serviço de armazenamento do Azure mantêm as entradas por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="c50e7-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="c50e7-111">Como esse comando especifica o parâmetro *PassThru* , o comando exibe as propriedades Metrics modificadas.</span><span class="sxs-lookup"><span data-stu-id="c50e7-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="c50e7-112">OS</span><span class="sxs-lookup"><span data-stu-id="c50e7-112">PARAMETERS</span></span>

### <span data-ttu-id="c50e7-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c50e7-113">-Context</span></span>
<span data-ttu-id="c50e7-114">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c50e7-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c50e7-115">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c50e7-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c50e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c50e7-116">-DefaultProfile</span></span>
<span data-ttu-id="c50e7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c50e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50e7-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="c50e7-118">-MetricsLevel</span></span>
<span data-ttu-id="c50e7-119">Especifica o nível de métrica que o armazenamento do Azure usa para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c50e7-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="c50e7-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c50e7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c50e7-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c50e7-121">None</span></span>
- <span data-ttu-id="c50e7-122">Atender</span><span class="sxs-lookup"><span data-stu-id="c50e7-122">Service</span></span>
- <span data-ttu-id="c50e7-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="c50e7-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50e7-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="c50e7-124">-MetricsType</span></span>
<span data-ttu-id="c50e7-125">Especifica um tipo de métrica.</span><span class="sxs-lookup"><span data-stu-id="c50e7-125">Specifies a metrics type.</span></span>
<span data-ttu-id="c50e7-126">Esta cmldet define o tipo de métrica do serviço de armazenamento do Azure para o valor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c50e7-126">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="c50e7-127">Os valores aceitáveis para esse parâmetro são: Hour e minute.</span><span class="sxs-lookup"><span data-stu-id="c50e7-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="c50e7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c50e7-128">-PassThru</span></span>
<span data-ttu-id="c50e7-129">Indica que esses cmdlets retornam as propriedades de métricas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="c50e7-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="c50e7-130">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="c50e7-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c50e7-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c50e7-131">-RetentionDays</span></span>
<span data-ttu-id="c50e7-132">Especifica o número de dias durante os quais o serviço de armazenamento do Azure mantém as informações de métricas.</span><span class="sxs-lookup"><span data-stu-id="c50e7-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50e7-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c50e7-133">-ServiceType</span></span>
<span data-ttu-id="c50e7-134">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c50e7-134">Specifies the storage service type.</span></span>
<span data-ttu-id="c50e7-135">Esse cmdlet modifica as propriedades de métricas do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c50e7-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c50e7-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c50e7-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c50e7-137">Irregular</span><span class="sxs-lookup"><span data-stu-id="c50e7-137">Blob</span></span> 
- <span data-ttu-id="c50e7-138">TableName</span><span class="sxs-lookup"><span data-stu-id="c50e7-138">Table</span></span>
- <span data-ttu-id="c50e7-139">Coloca</span><span class="sxs-lookup"><span data-stu-id="c50e7-139">Queue</span></span>
- <span data-ttu-id="c50e7-140">Arquivo no momento, não há suporte para o valor do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c50e7-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="c50e7-141">-Versão</span><span class="sxs-lookup"><span data-stu-id="c50e7-141">-Version</span></span>
<span data-ttu-id="c50e7-142">Especifica a versão das métricas de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c50e7-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="c50e7-143">O valor padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="c50e7-143">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50e7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c50e7-144">CommonParameters</span></span>
<span data-ttu-id="c50e7-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c50e7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c50e7-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c50e7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c50e7-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c50e7-147">INPUTS</span></span>

### <span data-ttu-id="c50e7-148">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c50e7-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c50e7-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c50e7-149">OUTPUTS</span></span>

### <span data-ttu-id="c50e7-150">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="c50e7-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="c50e7-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c50e7-151">NOTES</span></span>

## <span data-ttu-id="c50e7-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c50e7-152">RELATED LINKS</span></span>

[<span data-ttu-id="c50e7-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c50e7-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="c50e7-154">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c50e7-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


