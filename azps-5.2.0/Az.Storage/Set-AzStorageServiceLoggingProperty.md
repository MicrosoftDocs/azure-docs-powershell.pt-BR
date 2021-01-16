---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260746"
---
# <span data-ttu-id="e087f-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e087f-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="e087f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e087f-102">SYNOPSIS</span></span>
<span data-ttu-id="e087f-103">Modifica o registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e087f-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="e087f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e087f-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e087f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e087f-105">DESCRIPTION</span></span>
<span data-ttu-id="e087f-106">O cmdlet **set-AzStorageServiceLoggingProperty** modifica o registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e087f-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="e087f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e087f-107">EXAMPLES</span></span>

### <span data-ttu-id="e087f-108">Exemplo 1: modificar as propriedades de log do serviço blob</span><span class="sxs-lookup"><span data-stu-id="e087f-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="e087f-109">Esse comando modifica o log da versão 1,0 do armazenamento de BLOB para incluir operações de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="e087f-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="e087f-110">O log do serviço de armazenamento do Azure retém as entradas por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="e087f-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="e087f-111">Como esse comando especifica o parâmetro *PassThru* , o comando exibe as propriedades de registro em log modificadas.</span><span class="sxs-lookup"><span data-stu-id="e087f-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="e087f-112">OS</span><span class="sxs-lookup"><span data-stu-id="e087f-112">PARAMETERS</span></span>

### <span data-ttu-id="e087f-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e087f-113">-Context</span></span>
<span data-ttu-id="e087f-114">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e087f-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e087f-115">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e087f-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e087f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e087f-116">-DefaultProfile</span></span>
<span data-ttu-id="e087f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e087f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e087f-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="e087f-118">-LoggingOperations</span></span>
<span data-ttu-id="e087f-119">Especifica uma matriz de operações do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e087f-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="e087f-120">O Azure Storage Services registra as operações que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e087f-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="e087f-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e087f-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e087f-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e087f-122">None</span></span>
- <span data-ttu-id="e087f-123">Ler</span><span class="sxs-lookup"><span data-stu-id="e087f-123">Read</span></span>
- <span data-ttu-id="e087f-124">Gravação</span><span class="sxs-lookup"><span data-stu-id="e087f-124">Write</span></span>
- <span data-ttu-id="e087f-125">Remover</span><span class="sxs-lookup"><span data-stu-id="e087f-125">Delete</span></span>
- <span data-ttu-id="e087f-126">Todo</span><span class="sxs-lookup"><span data-stu-id="e087f-126">All</span></span>

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

### <span data-ttu-id="e087f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e087f-127">-PassThru</span></span>
<span data-ttu-id="e087f-128">Indica que esse cmdlet retorna as propriedades de log atualizadas.</span><span class="sxs-lookup"><span data-stu-id="e087f-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="e087f-129">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="e087f-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e087f-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="e087f-130">-RetentionDays</span></span>
<span data-ttu-id="e087f-131">Especifica o número de dias durante os quais o serviço de armazenamento do Azure mantém as informações registradas.</span><span class="sxs-lookup"><span data-stu-id="e087f-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="e087f-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e087f-132">-ServiceType</span></span>
<span data-ttu-id="e087f-133">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e087f-133">Specifies the storage service type.</span></span>
<span data-ttu-id="e087f-134">Esse cmdlet modifica as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e087f-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="e087f-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e087f-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e087f-136">Irregular</span><span class="sxs-lookup"><span data-stu-id="e087f-136">Blob</span></span> 
- <span data-ttu-id="e087f-137">TableName</span><span class="sxs-lookup"><span data-stu-id="e087f-137">Table</span></span>
- <span data-ttu-id="e087f-138">Coloca</span><span class="sxs-lookup"><span data-stu-id="e087f-138">Queue</span></span>
- <span data-ttu-id="e087f-139">Arquivo no momento, não há suporte para o valor do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e087f-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="e087f-140">-Versão</span><span class="sxs-lookup"><span data-stu-id="e087f-140">-Version</span></span>
<span data-ttu-id="e087f-141">Especifica a versão do log do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e087f-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="e087f-142">O valor padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="e087f-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="e087f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e087f-143">CommonParameters</span></span>
<span data-ttu-id="e087f-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e087f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e087f-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e087f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e087f-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e087f-146">INPUTS</span></span>

### <span data-ttu-id="e087f-147">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e087f-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e087f-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e087f-148">OUTPUTS</span></span>

### <span data-ttu-id="e087f-149">Microsoft. Azure. Storage. Shared. Protocol. Loggingproperties</span><span class="sxs-lookup"><span data-stu-id="e087f-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="e087f-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e087f-150">NOTES</span></span>

## <span data-ttu-id="e087f-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e087f-151">RELATED LINKS</span></span>

[<span data-ttu-id="e087f-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e087f-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="e087f-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e087f-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


