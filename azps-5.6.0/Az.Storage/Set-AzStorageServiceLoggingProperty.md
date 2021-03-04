---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 84eae2221564d1c1a569ea5469c44cb1cd628b04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888153"
---
# <span data-ttu-id="87a9a-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="87a9a-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="87a9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="87a9a-103">Modifica o log dos serviços de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="87a9a-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="87a9a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="87a9a-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87a9a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="87a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="87a9a-106">O cmdlet **Set-AzStorageServiceLoggingProperty** modifica o log dos serviços de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="87a9a-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="87a9a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87a9a-107">EXAMPLES</span></span>

### <span data-ttu-id="87a9a-108">Exemplo 1: Modificar propriedades de registro em log para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="87a9a-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="87a9a-109">Este comando modifica o registro em log da versão 1.0 para que o armazenamento blob inclua operações de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="87a9a-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="87a9a-110">O registro em log do serviço de Armazenamento do Azure mantém entradas por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="87a9a-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="87a9a-111">Como esse comando especifica o parâmetro *PassThru,* o comando exibe as propriedades de registro em log modificadas.</span><span class="sxs-lookup"><span data-stu-id="87a9a-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="87a9a-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="87a9a-112">PARAMETERS</span></span>

### <span data-ttu-id="87a9a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="87a9a-113">-Context</span></span>
<span data-ttu-id="87a9a-114">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="87a9a-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="87a9a-115">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87a9a-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="87a9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a9a-116">-DefaultProfile</span></span>
<span data-ttu-id="87a9a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87a9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87a9a-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="87a9a-118">-LoggingOperations</span></span>
<span data-ttu-id="87a9a-119">Especifica uma matriz de operações de serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="87a9a-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="87a9a-120">Os serviços de Armazenamento do Azure registram as operações especificadas por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="87a9a-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="87a9a-121">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="87a9a-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87a9a-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="87a9a-122">None</span></span>
- <span data-ttu-id="87a9a-123">Leitura</span><span class="sxs-lookup"><span data-stu-id="87a9a-123">Read</span></span>
- <span data-ttu-id="87a9a-124">Gravar</span><span class="sxs-lookup"><span data-stu-id="87a9a-124">Write</span></span>
- <span data-ttu-id="87a9a-125">Excluir</span><span class="sxs-lookup"><span data-stu-id="87a9a-125">Delete</span></span>
- <span data-ttu-id="87a9a-126">All</span><span class="sxs-lookup"><span data-stu-id="87a9a-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a9a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87a9a-127">-PassThru</span></span>
<span data-ttu-id="87a9a-128">Indica que esse cmdlet retorna as propriedades de registro em log atualizadas.</span><span class="sxs-lookup"><span data-stu-id="87a9a-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="87a9a-129">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="87a9a-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="87a9a-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="87a9a-130">-RetentionDays</span></span>
<span data-ttu-id="87a9a-131">Especifica o número de dias em que o serviço de Armazenamento do Azure mantém informações registradas.</span><span class="sxs-lookup"><span data-stu-id="87a9a-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="87a9a-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="87a9a-132">-ServiceType</span></span>
<span data-ttu-id="87a9a-133">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="87a9a-133">Specifies the storage service type.</span></span>
<span data-ttu-id="87a9a-134">Este cmdlet modifica as propriedades de registro em log para o tipo de serviço especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="87a9a-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="87a9a-135">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="87a9a-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87a9a-136">Blob</span><span class="sxs-lookup"><span data-stu-id="87a9a-136">Blob</span></span> 
- <span data-ttu-id="87a9a-137">Tabela</span><span class="sxs-lookup"><span data-stu-id="87a9a-137">Table</span></span>
- <span data-ttu-id="87a9a-138">Fila</span><span class="sxs-lookup"><span data-stu-id="87a9a-138">Queue</span></span>
- <span data-ttu-id="87a9a-139">Arquivo O valor de File não é suportado no momento.</span><span class="sxs-lookup"><span data-stu-id="87a9a-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="87a9a-140">-Version</span><span class="sxs-lookup"><span data-stu-id="87a9a-140">-Version</span></span>
<span data-ttu-id="87a9a-141">Especifica a versão do log do serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="87a9a-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="87a9a-142">O valor padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="87a9a-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="87a9a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a9a-143">CommonParameters</span></span>
<span data-ttu-id="87a9a-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a9a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a9a-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a9a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a9a-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87a9a-146">INPUTS</span></span>

### <span data-ttu-id="87a9a-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="87a9a-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="87a9a-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="87a9a-148">OUTPUTS</span></span>

### <span data-ttu-id="87a9a-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="87a9a-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="87a9a-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="87a9a-150">NOTES</span></span>

## <span data-ttu-id="87a9a-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87a9a-151">RELATED LINKS</span></span>

[<span data-ttu-id="87a9a-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="87a9a-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="87a9a-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="87a9a-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


