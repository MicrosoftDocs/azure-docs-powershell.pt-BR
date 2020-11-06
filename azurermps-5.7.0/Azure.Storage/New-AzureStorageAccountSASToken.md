---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: fb0565232410e840ef3e8adbad48e7f622a51d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432533"
---
# <span data-ttu-id="437d9-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="437d9-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="437d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="437d9-102">SYNOPSIS</span></span>
<span data-ttu-id="437d9-103">Cria um token SAS no nível da conta.</span><span class="sxs-lookup"><span data-stu-id="437d9-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="437d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="437d9-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="437d9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="437d9-105">DESCRIPTION</span></span>
<span data-ttu-id="437d9-106">O cmdlet **New-AzureStorageSASToken** cria um token de assinatura de acesso compartilhado (SAS) de conta em nível de conta para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="437d9-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="437d9-107">Você pode usar o token SAS para delegar permissões para vários serviços ou para delegar permissões para serviços que não estão disponíveis com um token de SAS no nível do objeto.</span><span class="sxs-lookup"><span data-stu-id="437d9-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="437d9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="437d9-108">EXAMPLES</span></span>

### <span data-ttu-id="437d9-109">Exemplo 1: criar um token SAS em nível de conta com permissão completa</span><span class="sxs-lookup"><span data-stu-id="437d9-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="437d9-110">Esse comando cria um token SAS no nível da conta com permissão total.</span><span class="sxs-lookup"><span data-stu-id="437d9-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="437d9-111">Exemplo 2: criar um token SAS em nível de conta para um intervalo de endereços IP</span><span class="sxs-lookup"><span data-stu-id="437d9-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="437d9-112">Esse comando cria um token SAS em nível de conta para solicitações somente HTTPS do intervalo de endereços IP especificado.</span><span class="sxs-lookup"><span data-stu-id="437d9-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="437d9-113">OS</span><span class="sxs-lookup"><span data-stu-id="437d9-113">PARAMETERS</span></span>

### <span data-ttu-id="437d9-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="437d9-114">-Context</span></span>
<span data-ttu-id="437d9-115">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="437d9-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="437d9-116">Você pode usar o cmdlet New-AzureStorageContext para obter um objeto **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="437d9-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="437d9-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="437d9-117">-ExpiryTime</span></span>
<span data-ttu-id="437d9-118">Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="437d9-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="437d9-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="437d9-119">-IPAddressOrRange</span></span>
<span data-ttu-id="437d9-120">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="437d9-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="437d9-121">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="437d9-121">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="437d9-122">-Permissão</span><span class="sxs-lookup"><span data-stu-id="437d9-122">-Permission</span></span>
<span data-ttu-id="437d9-123">Especifica as permissões para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="437d9-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="437d9-124">As permissões só serão válidas se corresponderem ao tipo de recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="437d9-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="437d9-125">Para obter mais informações sobre valores de permissão aceitáveis, consulte construindo uma conta SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="437d9-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="437d9-126">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="437d9-126">-Protocol</span></span>
<span data-ttu-id="437d9-127">Especifica o protocolo permitido para uma solicitação feita com a SAS da conta.</span><span class="sxs-lookup"><span data-stu-id="437d9-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="437d9-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="437d9-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="437d9-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="437d9-129">HttpsOnly</span></span>
- <span data-ttu-id="437d9-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="437d9-130">HttpsOrHttp</span></span>

<span data-ttu-id="437d9-131">O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="437d9-131">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="437d9-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="437d9-132">-ResourceType</span></span>
<span data-ttu-id="437d9-133">Especifica os tipos de recursos que estão disponíveis com o token SAS.</span><span class="sxs-lookup"><span data-stu-id="437d9-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="437d9-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="437d9-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="437d9-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="437d9-135">None</span></span>
- <span data-ttu-id="437d9-136">Atender</span><span class="sxs-lookup"><span data-stu-id="437d9-136">Service</span></span>
- <span data-ttu-id="437d9-137">Contêiner</span><span class="sxs-lookup"><span data-stu-id="437d9-137">Container</span></span>
- <span data-ttu-id="437d9-138">Objeto</span><span class="sxs-lookup"><span data-stu-id="437d9-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="437d9-139">-Serviço</span><span class="sxs-lookup"><span data-stu-id="437d9-139">-Service</span></span>
<span data-ttu-id="437d9-140">Especifica o serviço.</span><span class="sxs-lookup"><span data-stu-id="437d9-140">Specifies the service.</span></span>
<span data-ttu-id="437d9-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="437d9-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="437d9-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="437d9-142">None</span></span>
- <span data-ttu-id="437d9-143">Irregular</span><span class="sxs-lookup"><span data-stu-id="437d9-143">Blob</span></span>
- <span data-ttu-id="437d9-144">Arquivos</span><span class="sxs-lookup"><span data-stu-id="437d9-144">File</span></span>
- <span data-ttu-id="437d9-145">Coloca</span><span class="sxs-lookup"><span data-stu-id="437d9-145">Queue</span></span>
- <span data-ttu-id="437d9-146">TableName</span><span class="sxs-lookup"><span data-stu-id="437d9-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="437d9-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="437d9-147">-StartTime</span></span>
<span data-ttu-id="437d9-148">Especifica o tempo, como um objeto **DateTime** , no qual a SAS se torna válida.</span><span class="sxs-lookup"><span data-stu-id="437d9-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="437d9-149">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="437d9-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="437d9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="437d9-150">CommonParameters</span></span>
<span data-ttu-id="437d9-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="437d9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="437d9-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="437d9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="437d9-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="437d9-153">INPUTS</span></span>

### <span data-ttu-id="437d9-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="437d9-154">IStorageContext</span></span>

<span data-ttu-id="437d9-155">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="437d9-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="437d9-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="437d9-156">OUTPUTS</span></span>

### <span data-ttu-id="437d9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="437d9-157">System.String</span></span>

## <span data-ttu-id="437d9-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="437d9-158">NOTES</span></span>

## <span data-ttu-id="437d9-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="437d9-159">RELATED LINKS</span></span>

[<span data-ttu-id="437d9-160">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="437d9-160">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="437d9-161">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="437d9-161">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="437d9-162">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="437d9-162">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="437d9-163">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="437d9-163">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="437d9-164">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="437d9-164">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="437d9-165">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="437d9-165">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


