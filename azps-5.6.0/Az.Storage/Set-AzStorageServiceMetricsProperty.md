---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 715fc15fbafe2f0ba1b4c6782bed607f9878bd55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888152"
---
# <span data-ttu-id="654e0-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="654e0-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="654e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="654e0-102">SYNOPSIS</span></span>
<span data-ttu-id="654e0-103">Modifica propriedades de métricas para o serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="654e0-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="654e0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="654e0-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="654e0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="654e0-105">DESCRIPTION</span></span>
<span data-ttu-id="654e0-106">O cmdlet **Set-AzStorageServiceMetricsProperty** modifica propriedades de métricas para o serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="654e0-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="654e0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="654e0-107">EXAMPLES</span></span>

### <span data-ttu-id="654e0-108">Exemplo 1: Modificar propriedades de métricas para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="654e0-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="654e0-109">Este comando modifica as métricas da versão 1.0 para armazenamento de blob em um nível de Serviço.</span><span class="sxs-lookup"><span data-stu-id="654e0-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="654e0-110">As métricas do serviço de Armazenamento do Azure retêm entradas por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="654e0-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="654e0-111">Como esse comando especifica o parâmetro *PassThru,* o comando exibe as propriedades de métricas modificadas.</span><span class="sxs-lookup"><span data-stu-id="654e0-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="654e0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="654e0-112">PARAMETERS</span></span>

### <span data-ttu-id="654e0-113">-Context</span><span class="sxs-lookup"><span data-stu-id="654e0-113">-Context</span></span>
<span data-ttu-id="654e0-114">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="654e0-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="654e0-115">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="654e0-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="654e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="654e0-116">-DefaultProfile</span></span>
<span data-ttu-id="654e0-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="654e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="654e0-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="654e0-118">-MetricsLevel</span></span>
<span data-ttu-id="654e0-119">Especifica o nível de métrica que o Armazenamento do Azure usa para o serviço.</span><span class="sxs-lookup"><span data-stu-id="654e0-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="654e0-120">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="654e0-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="654e0-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="654e0-121">None</span></span>
- <span data-ttu-id="654e0-122">Serviço</span><span class="sxs-lookup"><span data-stu-id="654e0-122">Service</span></span>
- <span data-ttu-id="654e0-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="654e0-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654e0-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="654e0-124">-MetricsType</span></span>
<span data-ttu-id="654e0-125">Especifica um tipo de métrica.</span><span class="sxs-lookup"><span data-stu-id="654e0-125">Specifies a metrics type.</span></span>
<span data-ttu-id="654e0-126">Este cmdlet define o tipo de métrica do serviço de Armazenamento do Azure como o valor especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="654e0-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="654e0-127">Os valores aceitáveis para este parâmetro são: Hora e Minuto.</span><span class="sxs-lookup"><span data-stu-id="654e0-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="654e0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="654e0-128">-PassThru</span></span>
<span data-ttu-id="654e0-129">Indica que esse cmdlets retorna as propriedades de métricas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="654e0-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="654e0-130">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="654e0-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="654e0-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="654e0-131">-RetentionDays</span></span>
<span data-ttu-id="654e0-132">Especifica o número de dias em que o serviço de Armazenamento do Azure mantém informações de métricas.</span><span class="sxs-lookup"><span data-stu-id="654e0-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="654e0-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="654e0-133">-ServiceType</span></span>
<span data-ttu-id="654e0-134">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="654e0-134">Specifies the storage service type.</span></span>
<span data-ttu-id="654e0-135">Este cmdlet modifica as propriedades de métricas para o tipo de serviço especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="654e0-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="654e0-136">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="654e0-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="654e0-137">Blob</span><span class="sxs-lookup"><span data-stu-id="654e0-137">Blob</span></span> 
- <span data-ttu-id="654e0-138">Tabela</span><span class="sxs-lookup"><span data-stu-id="654e0-138">Table</span></span>
- <span data-ttu-id="654e0-139">Fila</span><span class="sxs-lookup"><span data-stu-id="654e0-139">Queue</span></span>
- <span data-ttu-id="654e0-140">Arquivo O valor de File não é suportado no momento.</span><span class="sxs-lookup"><span data-stu-id="654e0-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="654e0-141">-Version</span><span class="sxs-lookup"><span data-stu-id="654e0-141">-Version</span></span>
<span data-ttu-id="654e0-142">Especifica a versão das métricas de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="654e0-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="654e0-143">O valor padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="654e0-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="654e0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="654e0-144">CommonParameters</span></span>
<span data-ttu-id="654e0-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="654e0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="654e0-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="654e0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="654e0-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="654e0-147">INPUTS</span></span>

### <span data-ttu-id="654e0-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="654e0-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="654e0-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="654e0-149">OUTPUTS</span></span>

### <span data-ttu-id="654e0-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="654e0-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="654e0-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="654e0-151">NOTES</span></span>

## <span data-ttu-id="654e0-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="654e0-152">RELATED LINKS</span></span>

[<span data-ttu-id="654e0-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="654e0-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="654e0-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="654e0-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


