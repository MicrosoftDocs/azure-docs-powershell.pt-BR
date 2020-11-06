---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: fbd7c691e2cfbef58bc59429f68740af00288906
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610684"
---
# <span data-ttu-id="6d2ff-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6d2ff-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="6d2ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2ff-103">Modifica o registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d2ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d2ff-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d2ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d2ff-105">DESCRIPTION</span></span>
<span data-ttu-id="6d2ff-106">O cmdlet **set-AzureStorageServiceLoggingProperty** modifica o registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="6d2ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d2ff-107">EXAMPLES</span></span>

### <span data-ttu-id="6d2ff-108">Exemplo 1: modificar as propriedades de log do serviço blob</span><span class="sxs-lookup"><span data-stu-id="6d2ff-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="6d2ff-109">Esse comando modifica o log da versão 1,0 do armazenamento de BLOB para incluir operações de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="6d2ff-110">O log do serviço de armazenamento do Azure retém as entradas por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="6d2ff-111">Como esse comando especifica o parâmetro *PassThru* , o comando exibe as propriedades de registro em log modificadas.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="6d2ff-112">OS</span><span class="sxs-lookup"><span data-stu-id="6d2ff-112">PARAMETERS</span></span>

### <span data-ttu-id="6d2ff-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6d2ff-113">-Context</span></span>
<span data-ttu-id="6d2ff-114">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6d2ff-115">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6d2ff-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="6d2ff-116">-LoggingOperations</span></span>
<span data-ttu-id="6d2ff-117">Especifica uma matriz de operações do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="6d2ff-118">O Azure Storage Services registra as operações que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="6d2ff-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6d2ff-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d2ff-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6d2ff-120">None</span></span>
- <span data-ttu-id="6d2ff-121">Ler</span><span class="sxs-lookup"><span data-stu-id="6d2ff-121">Read</span></span>
- <span data-ttu-id="6d2ff-122">Gravação</span><span class="sxs-lookup"><span data-stu-id="6d2ff-122">Write</span></span>
- <span data-ttu-id="6d2ff-123">Remover</span><span class="sxs-lookup"><span data-stu-id="6d2ff-123">Delete</span></span>
- <span data-ttu-id="6d2ff-124">Todo</span><span class="sxs-lookup"><span data-stu-id="6d2ff-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d2ff-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d2ff-125">-PassThru</span></span>
<span data-ttu-id="6d2ff-126">Indica que esse cmdlet retorna as propriedades de log atualizadas.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="6d2ff-127">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6d2ff-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="6d2ff-128">-RetentionDays</span></span>
<span data-ttu-id="6d2ff-129">Especifica o número de dias durante os quais o serviço de armazenamento do Azure mantém as informações registradas.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="6d2ff-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6d2ff-130">-ServiceType</span></span>
<span data-ttu-id="6d2ff-131">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-131">Specifies the storage service type.</span></span>
<span data-ttu-id="6d2ff-132">Esse cmdlet modifica as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="6d2ff-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6d2ff-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d2ff-134">Irregular</span><span class="sxs-lookup"><span data-stu-id="6d2ff-134">Blob</span></span> 
- <span data-ttu-id="6d2ff-135">TableName</span><span class="sxs-lookup"><span data-stu-id="6d2ff-135">Table</span></span>
- <span data-ttu-id="6d2ff-136">Coloca</span><span class="sxs-lookup"><span data-stu-id="6d2ff-136">Queue</span></span>
- <span data-ttu-id="6d2ff-137">Arquivos</span><span class="sxs-lookup"><span data-stu-id="6d2ff-137">File</span></span>

<span data-ttu-id="6d2ff-138">Não há suporte para o valor do arquivo no momento.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="6d2ff-139">-Versão</span><span class="sxs-lookup"><span data-stu-id="6d2ff-139">-Version</span></span>
<span data-ttu-id="6d2ff-140">Especifica a versão do log do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="6d2ff-141">O valor padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="6d2ff-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2ff-142">CommonParameters</span></span>
<span data-ttu-id="6d2ff-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2ff-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d2ff-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2ff-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d2ff-145">INPUTS</span></span>

### <span data-ttu-id="6d2ff-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6d2ff-146">IStorageContext</span></span>

<span data-ttu-id="6d2ff-147">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6d2ff-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="6d2ff-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d2ff-148">OUTPUTS</span></span>

### <span data-ttu-id="6d2ff-149">Microsoft. WindowsAzure. Storage. Shared. Protocol. Loggingproperties</span><span class="sxs-lookup"><span data-stu-id="6d2ff-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="6d2ff-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d2ff-150">NOTES</span></span>

## <span data-ttu-id="6d2ff-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d2ff-151">RELATED LINKS</span></span>

[<span data-ttu-id="6d2ff-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6d2ff-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="6d2ff-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6d2ff-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


