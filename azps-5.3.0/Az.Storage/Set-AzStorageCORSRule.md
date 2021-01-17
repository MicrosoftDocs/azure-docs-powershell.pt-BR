---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d7951e53c7cbd8c799c7158bb3cc5c3fabb5b039
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427686"
---
# <span data-ttu-id="4908d-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4908d-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="4908d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4908d-102">SYNOPSIS</span></span>
<span data-ttu-id="4908d-103">Define as regras CORS para um tipo de serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4908d-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="4908d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4908d-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4908d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4908d-105">DESCRIPTION</span></span>
<span data-ttu-id="4908d-106">O cmdlet **set-AzStorageCORSRule** define as regras de compartilhamento de recursos entre origens (CORS) para um tipo de serviço de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4908d-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="4908d-107">Os tipos de serviços de armazenamento para esse cmdlet são BLOB, tabela, fila e arquivo.</span><span class="sxs-lookup"><span data-stu-id="4908d-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="4908d-108">Esse cmdlet substitui as regras existentes.</span><span class="sxs-lookup"><span data-stu-id="4908d-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="4908d-109">Para ver as regras atuais, use o cmdlet Get-AzStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="4908d-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="4908d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4908d-110">EXAMPLES</span></span>

### <span data-ttu-id="4908d-111">Exemplo 1: atribuir regras CORS ao serviço blob</span><span class="sxs-lookup"><span data-stu-id="4908d-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="4908d-112">O primeiro comando atribui uma matriz de regras à variável $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="4908d-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="4908d-113">Esse comando usa a extensão padrão em várias linhas nesse bloco de código.</span><span class="sxs-lookup"><span data-stu-id="4908d-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="4908d-114">O segundo comando atribui as regras em $CorsRules ao tipo de serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="4908d-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="4908d-115">Exemplo 2: alterar as propriedades de uma regra CORS para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="4908d-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="4908d-116">O primeiro comando obtém as regras CORS atuais para o tipo de BLOB usando o cmdlet **Get-AzStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="4908d-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="4908d-117">O comando armazena as regras na variável de matriz de $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="4908d-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="4908d-118">O segundo e o terceiro comandos modificam a primeira regra no $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="4908d-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="4908d-119">O comando final atribui as regras em $CorsRules ao tipo de serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="4908d-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="4908d-120">As regras revisadas substituem as regras CORS atuais.</span><span class="sxs-lookup"><span data-stu-id="4908d-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="4908d-121">OS</span><span class="sxs-lookup"><span data-stu-id="4908d-121">PARAMETERS</span></span>

### <span data-ttu-id="4908d-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4908d-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4908d-123">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="4908d-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4908d-124">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4908d-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4908d-125">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="4908d-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4908d-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4908d-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4908d-127">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4908d-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4908d-128">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4908d-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4908d-129">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="4908d-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4908d-130">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4908d-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4908d-131">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="4908d-131">The default value is 10.</span></span>

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

### <span data-ttu-id="4908d-132">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4908d-132">-Context</span></span>
<span data-ttu-id="4908d-133">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4908d-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4908d-134">Para obter um contexto, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4908d-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4908d-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="4908d-135">-CorsRules</span></span>
<span data-ttu-id="4908d-136">Especifica uma matriz de regras CORS.</span><span class="sxs-lookup"><span data-stu-id="4908d-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="4908d-137">Você pode recuperar as regras existentes usando o cmdlet Get-AzStorageCORSRule.</span><span class="sxs-lookup"><span data-stu-id="4908d-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4908d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4908d-138">-DefaultProfile</span></span>
<span data-ttu-id="4908d-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4908d-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4908d-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4908d-140">-PassThru</span></span>
<span data-ttu-id="4908d-141">Indica que esse cmdlet retorna um booliano que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="4908d-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="4908d-142">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4908d-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4908d-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4908d-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4908d-144">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="4908d-144">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4908d-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4908d-145">-ServiceType</span></span>
<span data-ttu-id="4908d-146">Especifica o tipo de serviço de armazenamento do Azure para o qual esse cmdlet atribui regras.</span><span class="sxs-lookup"><span data-stu-id="4908d-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="4908d-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4908d-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4908d-148">Irregular</span><span class="sxs-lookup"><span data-stu-id="4908d-148">Blob</span></span> 
- <span data-ttu-id="4908d-149">TableName</span><span class="sxs-lookup"><span data-stu-id="4908d-149">Table</span></span> 
- <span data-ttu-id="4908d-150">Coloca</span><span class="sxs-lookup"><span data-stu-id="4908d-150">Queue</span></span> 
- <span data-ttu-id="4908d-151">Arquivos</span><span class="sxs-lookup"><span data-stu-id="4908d-151">File</span></span>

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

### <span data-ttu-id="4908d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4908d-152">CommonParameters</span></span>
<span data-ttu-id="4908d-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4908d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4908d-154">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4908d-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4908d-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4908d-155">INPUTS</span></span>

### <span data-ttu-id="4908d-156">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4908d-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4908d-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4908d-157">OUTPUTS</span></span>

### <span data-ttu-id="4908d-158">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="4908d-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="4908d-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4908d-159">NOTES</span></span>

## <span data-ttu-id="4908d-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4908d-160">RELATED LINKS</span></span>

[<span data-ttu-id="4908d-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4908d-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="4908d-162">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4908d-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4908d-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4908d-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


