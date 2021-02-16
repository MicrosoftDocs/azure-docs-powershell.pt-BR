---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113929"
---
# <span data-ttu-id="368d3-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="368d3-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="368d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="368d3-102">SYNOPSIS</span></span>
<span data-ttu-id="368d3-103">Modifica as propriedades das métricas para o serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="368d3-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="368d3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="368d3-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="368d3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="368d3-105">DESCRIPTION</span></span>
<span data-ttu-id="368d3-106">O cmdlet **Set-AzStorageServiceMetricsProperty** modifica as propriedades de métrica do serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="368d3-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="368d3-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="368d3-107">EXAMPLES</span></span>

### <span data-ttu-id="368d3-108">Exemplo 1: Modificar propriedades de métricas para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="368d3-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="368d3-109">Esse comando modifica as métricas da versão 1.0 para armazenamento em blob em um nível de Serviço.</span><span class="sxs-lookup"><span data-stu-id="368d3-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="368d3-110">As métricas de serviço de armazenamento do Azure retêm as entradas por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="368d3-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="368d3-111">Como esse comando especifica o parâmetro *PassThru,* o comando exibe as propriedades de métricas modificadas.</span><span class="sxs-lookup"><span data-stu-id="368d3-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="368d3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="368d3-112">PARAMETERS</span></span>

### <span data-ttu-id="368d3-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="368d3-113">-Context</span></span>
<span data-ttu-id="368d3-114">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="368d3-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="368d3-115">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="368d3-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="368d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="368d3-116">-DefaultProfile</span></span>
<span data-ttu-id="368d3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="368d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="368d3-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="368d3-118">-MetricsLevel</span></span>
<span data-ttu-id="368d3-119">Especifica o nível de métricas que o Armazenamento do Azure usa para o serviço.</span><span class="sxs-lookup"><span data-stu-id="368d3-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="368d3-120">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="368d3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="368d3-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="368d3-121">None</span></span>
- <span data-ttu-id="368d3-122">Serviço</span><span class="sxs-lookup"><span data-stu-id="368d3-122">Service</span></span>
- <span data-ttu-id="368d3-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="368d3-123">ServiceAndApi</span></span>

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

### <span data-ttu-id="368d3-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="368d3-124">-MetricsType</span></span>
<span data-ttu-id="368d3-125">Especifica um tipo de métrica.</span><span class="sxs-lookup"><span data-stu-id="368d3-125">Specifies a metrics type.</span></span>
<span data-ttu-id="368d3-126">Esse cmdlet define o tipo de métricas de serviço de Armazenamento do Azure para o valor especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="368d3-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="368d3-127">Os valores aceitáveis para este parâmetro são: Hora e Minuto.</span><span class="sxs-lookup"><span data-stu-id="368d3-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="368d3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="368d3-128">-PassThru</span></span>
<span data-ttu-id="368d3-129">Indica que esse cmdlets retorna as propriedades de métricas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="368d3-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="368d3-130">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="368d3-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="368d3-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="368d3-131">-RetentionDays</span></span>
<span data-ttu-id="368d3-132">Especifica o número de dias que o serviço de Armazenamento do Azure mantém informações de métricas.</span><span class="sxs-lookup"><span data-stu-id="368d3-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="368d3-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="368d3-133">-ServiceType</span></span>
<span data-ttu-id="368d3-134">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="368d3-134">Specifies the storage service type.</span></span>
<span data-ttu-id="368d3-135">Esse cmdlet modifica as propriedades das métricas para o tipo de serviço especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="368d3-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="368d3-136">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="368d3-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="368d3-137">Blob</span><span class="sxs-lookup"><span data-stu-id="368d3-137">Blob</span></span> 
- <span data-ttu-id="368d3-138">Tabela</span><span class="sxs-lookup"><span data-stu-id="368d3-138">Table</span></span>
- <span data-ttu-id="368d3-139">Fila</span><span class="sxs-lookup"><span data-stu-id="368d3-139">Queue</span></span>
- <span data-ttu-id="368d3-140">Arquivo O valor do Arquivo não tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="368d3-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="368d3-141">-Versão</span><span class="sxs-lookup"><span data-stu-id="368d3-141">-Version</span></span>
<span data-ttu-id="368d3-142">Especifica a versão das métricas de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="368d3-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="368d3-143">O valor padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="368d3-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="368d3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="368d3-144">CommonParameters</span></span>
<span data-ttu-id="368d3-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="368d3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="368d3-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="368d3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="368d3-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="368d3-147">INPUTS</span></span>

### <span data-ttu-id="368d3-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="368d3-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="368d3-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="368d3-149">OUTPUTS</span></span>

### <span data-ttu-id="368d3-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="368d3-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="368d3-151">Notas</span><span class="sxs-lookup"><span data-stu-id="368d3-151">NOTES</span></span>

## <span data-ttu-id="368d3-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="368d3-152">RELATED LINKS</span></span>

[<span data-ttu-id="368d3-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="368d3-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="368d3-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="368d3-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


