---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: 8b0eb67808bf4148d93006b24273d55b737adfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431523"
---
# <span data-ttu-id="caf5f-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="caf5f-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="caf5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="caf5f-102">SYNOPSIS</span></span>
<span data-ttu-id="caf5f-103">Cria um token SAS no nível da conta.</span><span class="sxs-lookup"><span data-stu-id="caf5f-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caf5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="caf5f-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caf5f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="caf5f-105">DESCRIPTION</span></span>
<span data-ttu-id="caf5f-106">O cmdlet **New-AzureStorageSASToken** cria um token de assinatura de acesso compartilhado (SAS) de conta em nível de conta para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="caf5f-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="caf5f-107">Você pode usar o token SAS para delegar permissões para vários serviços ou para delegar permissões para serviços que não estão disponíveis com um token de SAS no nível do objeto.</span><span class="sxs-lookup"><span data-stu-id="caf5f-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="caf5f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="caf5f-108">EXAMPLES</span></span>

### <span data-ttu-id="caf5f-109">Exemplo 1: criar um token SAS em nível de conta com permissão completa</span><span class="sxs-lookup"><span data-stu-id="caf5f-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="caf5f-110">Esse comando cria um token SAS no nível da conta com permissão total.</span><span class="sxs-lookup"><span data-stu-id="caf5f-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="caf5f-111">Exemplo 2: criar um token SAS em nível de conta para um intervalo de endereços IP</span><span class="sxs-lookup"><span data-stu-id="caf5f-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="caf5f-112">Esse comando cria um token SAS em nível de conta para solicitações somente HTTPS do intervalo de endereços IP especificado.</span><span class="sxs-lookup"><span data-stu-id="caf5f-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="caf5f-113">OS</span><span class="sxs-lookup"><span data-stu-id="caf5f-113">PARAMETERS</span></span>

### <span data-ttu-id="caf5f-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="caf5f-114">-Context</span></span>
<span data-ttu-id="caf5f-115">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="caf5f-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="caf5f-116">Você pode usar o cmdlet New-AzureStorageContext para obter um objeto **AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="caf5f-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="caf5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf5f-117">-DefaultProfile</span></span>
<span data-ttu-id="caf5f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="caf5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caf5f-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="caf5f-119">-ExpiryTime</span></span>
<span data-ttu-id="caf5f-120">Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="caf5f-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf5f-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="caf5f-121">-IPAddressOrRange</span></span>
<span data-ttu-id="caf5f-122">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="caf5f-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="caf5f-123">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="caf5f-123">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf5f-124">-Permissão</span><span class="sxs-lookup"><span data-stu-id="caf5f-124">-Permission</span></span>
<span data-ttu-id="caf5f-125">Especifica as permissões para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="caf5f-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="caf5f-126">As permissões só serão válidas se corresponderem ao tipo de recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="caf5f-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="caf5f-127">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="caf5f-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="caf5f-128">Para obter mais informações sobre valores de permissão aceitáveis, consulte construindo uma conta SAS https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="caf5f-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf5f-129">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="caf5f-129">-Protocol</span></span>
<span data-ttu-id="caf5f-130">Especifica o protocolo permitido para uma solicitação feita com a SAS da conta.</span><span class="sxs-lookup"><span data-stu-id="caf5f-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="caf5f-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="caf5f-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="caf5f-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="caf5f-132">HttpsOnly</span></span>
- <span data-ttu-id="caf5f-133">HttpsOrHttp o valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="caf5f-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf5f-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="caf5f-134">-ResourceType</span></span>
<span data-ttu-id="caf5f-135">Especifica os tipos de recursos que estão disponíveis com o token SAS.</span><span class="sxs-lookup"><span data-stu-id="caf5f-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="caf5f-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="caf5f-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="caf5f-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="caf5f-137">None</span></span>
- <span data-ttu-id="caf5f-138">Atender</span><span class="sxs-lookup"><span data-stu-id="caf5f-138">Service</span></span>
- <span data-ttu-id="caf5f-139">Contêiner</span><span class="sxs-lookup"><span data-stu-id="caf5f-139">Container</span></span>
- <span data-ttu-id="caf5f-140">Objeto</span><span class="sxs-lookup"><span data-stu-id="caf5f-140">Object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf5f-141">-Serviço</span><span class="sxs-lookup"><span data-stu-id="caf5f-141">-Service</span></span>
<span data-ttu-id="caf5f-142">Especifica o serviço.</span><span class="sxs-lookup"><span data-stu-id="caf5f-142">Specifies the service.</span></span>
<span data-ttu-id="caf5f-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="caf5f-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="caf5f-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="caf5f-144">None</span></span>
- <span data-ttu-id="caf5f-145">Irregular</span><span class="sxs-lookup"><span data-stu-id="caf5f-145">Blob</span></span>
- <span data-ttu-id="caf5f-146">Arquivos</span><span class="sxs-lookup"><span data-stu-id="caf5f-146">File</span></span>
- <span data-ttu-id="caf5f-147">Coloca</span><span class="sxs-lookup"><span data-stu-id="caf5f-147">Queue</span></span>
- <span data-ttu-id="caf5f-148">TableName</span><span class="sxs-lookup"><span data-stu-id="caf5f-148">Table</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf5f-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="caf5f-149">-StartTime</span></span>
<span data-ttu-id="caf5f-150">Especifica o tempo, como um objeto **DateTime** , no qual a SAS se torna válida.</span><span class="sxs-lookup"><span data-stu-id="caf5f-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="caf5f-151">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="caf5f-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf5f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf5f-152">CommonParameters</span></span>
<span data-ttu-id="caf5f-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caf5f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf5f-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf5f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf5f-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="caf5f-155">INPUTS</span></span>

### <span data-ttu-id="caf5f-156">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="caf5f-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="caf5f-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="caf5f-157">OUTPUTS</span></span>

### <span data-ttu-id="caf5f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="caf5f-158">System.String</span></span>

## <span data-ttu-id="caf5f-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="caf5f-159">NOTES</span></span>

## <span data-ttu-id="caf5f-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="caf5f-160">RELATED LINKS</span></span>

[<span data-ttu-id="caf5f-161">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="caf5f-161">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="caf5f-162">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="caf5f-162">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="caf5f-163">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="caf5f-163">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="caf5f-164">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="caf5f-164">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="caf5f-165">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="caf5f-165">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="caf5f-166">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="caf5f-166">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)

