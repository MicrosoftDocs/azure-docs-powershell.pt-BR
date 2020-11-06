---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 17efee05b4d10ce87d327d8b7de26063bfc0cac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602080"
---
# <span data-ttu-id="d245d-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d245d-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="d245d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d245d-102">SYNOPSIS</span></span>
<span data-ttu-id="d245d-103">Gera um token SAS para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d245d-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d245d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d245d-104">SYNTAX</span></span>

### <span data-ttu-id="d245d-105">BlobNameWithPermission (padrão)</span><span class="sxs-lookup"><span data-stu-id="d245d-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d245d-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="d245d-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d245d-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="d245d-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d245d-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="d245d-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d245d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d245d-109">DESCRIPTION</span></span>
<span data-ttu-id="d245d-110">O cmdlet **New-AzureStorageBlobSASToken** gera um token de assinatura de acesso compartilhado (SAS) para um blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d245d-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="d245d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d245d-111">EXAMPLES</span></span>

### <span data-ttu-id="d245d-112">Exemplo 1: gerar um token SAS de blob com permissão completa de BLOB</span><span class="sxs-lookup"><span data-stu-id="d245d-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="d245d-113">Este exemplo gera um token SAS de blob com permissão de blob completo.</span><span class="sxs-lookup"><span data-stu-id="d245d-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="d245d-114">Exemplo 2: gerar um token SAS de blob com tempo de vida</span><span class="sxs-lookup"><span data-stu-id="d245d-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="d245d-115">Este exemplo gera um token SAS de blob com tempo de vida útil.</span><span class="sxs-lookup"><span data-stu-id="d245d-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="d245d-116">OS</span><span class="sxs-lookup"><span data-stu-id="d245d-116">PARAMETERS</span></span>

### <span data-ttu-id="d245d-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="d245d-117">-Blob</span></span>
<span data-ttu-id="d245d-118">Especifica o nome do blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d245d-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d245d-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d245d-119">-CloudBlob</span></span>
<span data-ttu-id="d245d-120">Especifica o objeto **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="d245d-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="d245d-121">Para obter um objeto **CloudBlob** , use o cmdlet [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="d245d-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d245d-122">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="d245d-122">-Container</span></span>
<span data-ttu-id="d245d-123">Especifica o nome do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d245d-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d245d-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d245d-124">-Context</span></span>
<span data-ttu-id="d245d-125">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d245d-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="d245d-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d245d-126">-ExpiryTime</span></span>
<span data-ttu-id="d245d-127">Especifica quando a assinatura de acesso compartilhado expira.</span><span class="sxs-lookup"><span data-stu-id="d245d-127">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="d245d-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d245d-128">-FullUri</span></span>
<span data-ttu-id="d245d-129">Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="d245d-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="d245d-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d245d-130">-IPAddressOrRange</span></span>
<span data-ttu-id="d245d-131">Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="d245d-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d245d-132">O intervalo é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="d245d-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="d245d-133">-Permissão</span><span class="sxs-lookup"><span data-stu-id="d245d-133">-Permission</span></span>
<span data-ttu-id="d245d-134">Especifica as permissões para um blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d245d-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d245d-135">-Política</span><span class="sxs-lookup"><span data-stu-id="d245d-135">-Policy</span></span>
<span data-ttu-id="d245d-136">Especifica uma política de acesso armazenado do Azure.</span><span class="sxs-lookup"><span data-stu-id="d245d-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d245d-137">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="d245d-137">-Protocol</span></span>
<span data-ttu-id="d245d-138">Especifica o protocolo permitido para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="d245d-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d245d-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d245d-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d245d-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d245d-140">HttpsOnly</span></span>
* <span data-ttu-id="d245d-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="d245d-141">HttpsOrHttp</span></span>

<span data-ttu-id="d245d-142">O valor padrão é HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d245d-142">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="d245d-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d245d-143">-StartTime</span></span>
<span data-ttu-id="d245d-144">Especifica a hora em que a assinatura de acesso compartilhado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="d245d-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="d245d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d245d-145">CommonParameters</span></span>
<span data-ttu-id="d245d-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d245d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d245d-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d245d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d245d-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d245d-148">INPUTS</span></span>

### <span data-ttu-id="d245d-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d245d-149">IStorageContext</span></span>

<span data-ttu-id="d245d-150">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d245d-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="d245d-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d245d-151">OUTPUTS</span></span>

### <span data-ttu-id="d245d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d245d-152">System.String</span></span>

## <span data-ttu-id="d245d-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d245d-153">NOTES</span></span>

## <span data-ttu-id="d245d-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d245d-154">RELATED LINKS</span></span>

[<span data-ttu-id="d245d-155">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d245d-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="d245d-156">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d245d-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
