---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: 6a04b038a452d979394ab57d8f3d905a57428051
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888404"
---
# <span data-ttu-id="53316-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="53316-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="53316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53316-102">SYNOPSIS</span></span>
<span data-ttu-id="53316-103">Define as regras do CORS para um tipo de serviço de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="53316-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="53316-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="53316-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="53316-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="53316-105">DESCRIPTION</span></span>
<span data-ttu-id="53316-106">O cmdlet **Set-AzStorageCORSRule** define as regras de Compartilhamento de Recursos entre Origens (CORS) para um tipo de serviço de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="53316-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="53316-107">Os tipos de serviços de armazenamento para este cmdlet são Blob, Table, Queue e File.</span><span class="sxs-lookup"><span data-stu-id="53316-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="53316-108">Esse cmdlet substitui as regras existentes.</span><span class="sxs-lookup"><span data-stu-id="53316-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="53316-109">Para ver as regras atuais, use Get-AzStorageCORSRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53316-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="53316-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53316-110">EXAMPLES</span></span>

### <span data-ttu-id="53316-111">Exemplo 1: Atribuir regras CORS ao serviço blob</span><span class="sxs-lookup"><span data-stu-id="53316-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="53316-112">O primeiro comando atribui uma matriz de regras à variável $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="53316-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="53316-113">Este comando usa o padrão se estende por várias linhas neste bloco de código.</span><span class="sxs-lookup"><span data-stu-id="53316-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="53316-114">O segundo comando atribui as regras em $CorsRules ao tipo de serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="53316-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="53316-115">Exemplo 2: Alterar propriedades de uma regra CORS para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="53316-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="53316-116">O primeiro comando obtém as regras cors atuais do tipo Blob usando o cmdlet **Get-AzStorageCORSRule.**</span><span class="sxs-lookup"><span data-stu-id="53316-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="53316-117">O comando armazena as regras na variável $CorsRules matriz.</span><span class="sxs-lookup"><span data-stu-id="53316-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="53316-118">O segundo e o terceiro comandos modificam a primeira regra no $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="53316-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="53316-119">O comando final atribui as regras em $CorsRules ao tipo de serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="53316-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="53316-120">As regras revisadas sobrescrevem as regras atuais do CORS.</span><span class="sxs-lookup"><span data-stu-id="53316-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="53316-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="53316-121">PARAMETERS</span></span>

### <span data-ttu-id="53316-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="53316-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="53316-123">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="53316-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="53316-124">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="53316-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="53316-125">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="53316-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="53316-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="53316-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="53316-127">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="53316-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="53316-128">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="53316-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="53316-129">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="53316-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="53316-130">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="53316-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="53316-131">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="53316-131">The default value is 10.</span></span>

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

### <span data-ttu-id="53316-132">-Context</span><span class="sxs-lookup"><span data-stu-id="53316-132">-Context</span></span>
<span data-ttu-id="53316-133">Especifica um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="53316-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="53316-134">Para obter um contexto, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53316-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="53316-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="53316-135">-CorsRules</span></span>
<span data-ttu-id="53316-136">Especifica uma matriz de regras CORS.</span><span class="sxs-lookup"><span data-stu-id="53316-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="53316-137">Você pode recuperar as regras existentes usando o Get-AzStorageCORSRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53316-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="53316-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53316-138">-DefaultProfile</span></span>
<span data-ttu-id="53316-139">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53316-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53316-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53316-140">-PassThru</span></span>
<span data-ttu-id="53316-141">Indica que esse cmdlet retorna um Boolean que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="53316-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="53316-142">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="53316-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="53316-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="53316-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="53316-144">Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="53316-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="53316-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="53316-145">-ServiceType</span></span>
<span data-ttu-id="53316-146">Especifica o tipo de serviço de Armazenamento do Azure para o qual este cmdlet atribui regras.</span><span class="sxs-lookup"><span data-stu-id="53316-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="53316-147">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="53316-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53316-148">Blob</span><span class="sxs-lookup"><span data-stu-id="53316-148">Blob</span></span> 
- <span data-ttu-id="53316-149">Tabela</span><span class="sxs-lookup"><span data-stu-id="53316-149">Table</span></span> 
- <span data-ttu-id="53316-150">Fila</span><span class="sxs-lookup"><span data-stu-id="53316-150">Queue</span></span> 
- <span data-ttu-id="53316-151">Arquivo</span><span class="sxs-lookup"><span data-stu-id="53316-151">File</span></span>

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

### <span data-ttu-id="53316-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53316-152">CommonParameters</span></span>
<span data-ttu-id="53316-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53316-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53316-154">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53316-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53316-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53316-155">INPUTS</span></span>

### <span data-ttu-id="53316-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="53316-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="53316-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="53316-157">OUTPUTS</span></span>

### <span data-ttu-id="53316-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="53316-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="53316-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="53316-159">NOTES</span></span>

## <span data-ttu-id="53316-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53316-160">RELATED LINKS</span></span>

[<span data-ttu-id="53316-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="53316-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="53316-162">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="53316-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="53316-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="53316-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


