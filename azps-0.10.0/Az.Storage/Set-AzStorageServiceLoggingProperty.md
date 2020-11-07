---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 70f2a9a426ab5e2cb9a2083e6e645973c9ee743a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776155"
---
# <span data-ttu-id="b492c-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b492c-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="b492c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b492c-102">SYNOPSIS</span></span>
<span data-ttu-id="b492c-103">Modifica o registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b492c-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="b492c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b492c-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b492c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b492c-105">DESCRIPTION</span></span>
<span data-ttu-id="b492c-106">O cmdlet **set-AzStorageServiceLoggingProperty** modifica o registro em log dos serviços de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b492c-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="b492c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b492c-107">EXAMPLES</span></span>

### <span data-ttu-id="b492c-108">Exemplo 1: modificar as propriedades de log do serviço blob</span><span class="sxs-lookup"><span data-stu-id="b492c-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="b492c-109">Esse comando modifica o log da versão 1,0 do armazenamento de BLOB para incluir operações de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="b492c-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="b492c-110">O log do serviço de armazenamento do Azure retém as entradas por 10 dias.</span><span class="sxs-lookup"><span data-stu-id="b492c-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="b492c-111">Como esse comando especifica o parâmetro *PassThru* , o comando exibe as propriedades de registro em log modificadas.</span><span class="sxs-lookup"><span data-stu-id="b492c-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="b492c-112">OS</span><span class="sxs-lookup"><span data-stu-id="b492c-112">PARAMETERS</span></span>

### <span data-ttu-id="b492c-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b492c-113">-Context</span></span>
<span data-ttu-id="b492c-114">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b492c-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b492c-115">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b492c-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b492c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b492c-116">-DefaultProfile</span></span>
<span data-ttu-id="b492c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b492c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b492c-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="b492c-118">-LoggingOperations</span></span>
<span data-ttu-id="b492c-119">Especifica uma matriz de operações do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b492c-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="b492c-120">O Azure Storage Services registra as operações que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b492c-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="b492c-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b492c-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b492c-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b492c-122">None</span></span>
- <span data-ttu-id="b492c-123">Ler</span><span class="sxs-lookup"><span data-stu-id="b492c-123">Read</span></span>
- <span data-ttu-id="b492c-124">Gravação</span><span class="sxs-lookup"><span data-stu-id="b492c-124">Write</span></span>
- <span data-ttu-id="b492c-125">Remover</span><span class="sxs-lookup"><span data-stu-id="b492c-125">Delete</span></span>
- <span data-ttu-id="b492c-126">Todo</span><span class="sxs-lookup"><span data-stu-id="b492c-126">All</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b492c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b492c-127">-PassThru</span></span>
<span data-ttu-id="b492c-128">Indica que esse cmdlet retorna as propriedades de log atualizadas.</span><span class="sxs-lookup"><span data-stu-id="b492c-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="b492c-129">Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.</span><span class="sxs-lookup"><span data-stu-id="b492c-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b492c-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="b492c-130">-RetentionDays</span></span>
<span data-ttu-id="b492c-131">Especifica o número de dias durante os quais o serviço de armazenamento do Azure mantém as informações registradas.</span><span class="sxs-lookup"><span data-stu-id="b492c-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="b492c-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b492c-132">-ServiceType</span></span>
<span data-ttu-id="b492c-133">Especifica o tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b492c-133">Specifies the storage service type.</span></span>
<span data-ttu-id="b492c-134">Esse cmdlet modifica as propriedades de log do tipo de serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b492c-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="b492c-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b492c-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b492c-136">Irregular</span><span class="sxs-lookup"><span data-stu-id="b492c-136">Blob</span></span> 
- <span data-ttu-id="b492c-137">TableName</span><span class="sxs-lookup"><span data-stu-id="b492c-137">Table</span></span>
- <span data-ttu-id="b492c-138">Coloca</span><span class="sxs-lookup"><span data-stu-id="b492c-138">Queue</span></span>
- <span data-ttu-id="b492c-139">Arquivo no momento, não há suporte para o valor do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b492c-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="b492c-140">-Versão</span><span class="sxs-lookup"><span data-stu-id="b492c-140">-Version</span></span>
<span data-ttu-id="b492c-141">Especifica a versão do log do serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b492c-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="b492c-142">O valor padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="b492c-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="b492c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b492c-143">CommonParameters</span></span>
<span data-ttu-id="b492c-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b492c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b492c-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b492c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b492c-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b492c-146">INPUTS</span></span>

### <span data-ttu-id="b492c-147">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b492c-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b492c-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b492c-148">OUTPUTS</span></span>

### <span data-ttu-id="b492c-149">Microsoft. WindowsAz. Storage. Shared. Protocol. Loggingproperties</span><span class="sxs-lookup"><span data-stu-id="b492c-149">Microsoft.WindowsAz.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="b492c-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b492c-150">NOTES</span></span>

## <span data-ttu-id="b492c-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b492c-151">RELATED LINKS</span></span>

[<span data-ttu-id="b492c-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b492c-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="b492c-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b492c-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

